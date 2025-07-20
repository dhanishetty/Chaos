# Using Service-Direct and Agent-Based Faults in a Single Chaos Experiment

Yes, absolutely. You can target the same VM with both service-direct and agent-based faults within a single Chaos experiment. This is a common and powerful pattern for creating more realistic failure scenarios.

Here’s the breakdown of how it works and how to set it up:

### The Concept: Targets vs. Faults

The key is to understand that you are onboarding one resource (the VM) as a target, but enabling it for two different *types* of capabilities:

1.  **Service-Direct Faults:** These are actions executed by Chaos Studio *against* the Azure resource itself, via the Azure control plane. You don't need an agent on the VM for these.
    *   **Example:** `VM Shutdown (version 1.0)`. Chaos Studio tells the Azure Compute service to deallocate your VM.

2.  **Agent-Based Faults:** These are actions executed *inside* the VM's operating system by the Chaos Studio agent. You must install the agent on the VM for these.
    *   **Example:** `CPU Pressure (version 2.0)`. The agent runs a process on the VM to consume CPU resources.

### How to Set It Up

To use both types of faults on the same VM, you must enable both capabilities on the target resource.

1.  **Onboard the VM as a Target:**
    *   Navigate to your VM in the Azure Portal.
    *   In the left-hand menu, find **Chaos Studio**.
    *   First, enable the target for **service-direct** faults.
    *   Second, enable the target for **agent-based** faults. This will involve installing the agent on the VM. The portal will give you instructions and the necessary commands to run on your VM to install and configure the agent.

2.  **Design Your Experiment:**
    *   In your Chaos experiment, you design the sequence using **Steps** and **Branches**. Steps run sequentially, one after the other. Branches within a step run in parallel.
    *   You can add a fault to each step and select the appropriate capability.

### Example Experiment: Stress and then Shut Down

Here is how you would design an experiment to first stress the VM's CPU (agent-based) and then shut it down (service-direct):

*   **Step 1: Agent-Based Fault**
    *   **Branch 1:**
        *   **Fault:** Add the `CPU Pressure` fault.
        *   **Target:** Select your VM. Because you enabled the agent, it will be available for this fault.
        *   **Parameters:** Set the duration (e.g., 5 minutes) and pressure level.

*   **Step 2: Service-Direct Fault**
    *   **Branch 1:**
        *   **Fault:** Add the `VM Shutdown` fault.
        *   **Target:** Select the *same* VM.
        *   **Parameters:** Set the `abruptShutdown` parameter to `true` or `false`.

### **Very Important Consideration: The Order Matters**

The sequence of your faults is critical.

*   **Correct Order:** Agent-based fault first, then service-direct shutdown.
    *   This works because the agent is running and can execute the CPU pressure fault. After it completes, the VM is shut down.

*   **Incorrect Order:** Service-direct shutdown first, then agent-based fault.
    *   This **will fail**. Once the `VM Shutdown` fault executes in Step 1, the VM is deallocated. The agent inside it stops running and cannot communicate with Chaos Studio. The agent-based fault in Step 2 will time out and fail because its target is offline.

By combining these fault types, you can simulate complex scenarios like an application struggling under load (CPU/memory pressure) before a sudden infrastructure failure (VM shutdown), allowing you to test your system's resilience more thoroughly.
