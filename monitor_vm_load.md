Excellent question. Monitoring the VM's load is the whole point of running the experiment! You need to see the impact in real-time to know if your fault injection is working and how your system behaves under stress.

Here are the best ways to monitor your VM's load during a Chaos Experiment, ordered from the simplest real-time view to the most powerful.

### Method 1: The "Right Now" Live View (VM Overview)

This is the quickest and easiest way to get a live pulse on your VM.

1.  In a separate browser tab, navigate to your **Virtual Machine** in the Azure Portal.
2.  Stay on the **Overview** tab.
3.  You will see several key performance charts right on this page, typically for **CPU (Average)**, **Network In/Out**, and **Disk Bytes/sec**.
4.  Keep this page open while your Chaos Experiment is running. These charts refresh automatically every few minutes.

*   **Best for:** A quick, simple confirmation that *something* is happening (e.g., seeing the CPU spike during a CPU stress test).
*   **Limitation:** The data is aggregated and refreshes a bit slowly. It's great for a basic check but not for detailed analysis.



---

### Method 2: The "Detailed Live Chart" (Azure Monitor Metrics)

This is the standard, most flexible way to watch performance metrics in detail. You can build your own monitoring chart.

1.  Navigate to your **Virtual Machine**.
2.  On the left menu, under the **Monitoring** section, click on **Metrics**.
3.  This will open a blank chart. Now, you can configure it:
    *   **Metric Namespace:** Ensure it's `Virtual Machine Host`.
    *   **Metric:** Select the metric you want to watch. The most common ones are:
        *   **Percentage CPU:** The most important one for CPU stress.
        *   **Available Memory Bytes:** For memory pressure experiments.
        *   **OS Disk IOPS Consumed Percentage:** For disk stress.
        *   **Network In/Out Total:** For network faults.
    *   **Aggregation:** Choose `Avg` (Average) or `Max` (Maximum) to see the peaks.
4.  **Crucially, adjust the time range.** At the top-right of the chart, change the time to **"Last 30 minutes"**. This gives you a near-real-time view. You can also set the **Time granularity** to **1 minute** for more detail.
5.  Click **"Add metric"** to plot multiple metrics (like CPU and Memory) on the same chart.

*   **Best for:** Actively watching specific, high-granularity metrics during an experiment. This is the go-to method for focused monitoring.

---

### Method 3: The "Pro Dashboard" (VM Insights)

This is the most powerful and recommended approach. VM Insights gives you a pre-built, rich dashboard that consolidates all key performance data.

**Prerequisite:** You must have enabled VM Insights on your VM. If you haven't, it will prompt you to. It works by deploying the Azure Monitor Agent to your VM.

1.  Navigate to your **Virtual Machine**.
2.  On the left menu, under **Monitoring**, click on **Insights**.
3.  Click on the **Performance** tab.
4.  You will now see detailed, pre-configured charts for CPU Utilization, Available Memory, Disk IOPS, Disk Latency, and more. This is a comprehensive health dashboard.
5.  The **Map** tab is also incredibly useful for network-based chaos experiments. It shows you live network traffic between your VM and any other resources it's talking to, and it will highlight failed connections.

*   **Best for:** A complete, professional view of your VM's health. It's the best way to understand the overall impact of an experiment on all system resources.

---

### Method 4: The "Application Impact" View (Application Insights)

If your VM is running an application (like a web server or an API), monitoring the VM's CPU is only half the story. You need to know how that CPU stress is affecting your *application*.

1.  Navigate to your **Application Insights** resource.
2.  On the left menu, click on **Live Metrics**.
3.  This will open a live-streaming dashboard showing:
    *   **Incoming Requests/sec:** Is your app still able to serve traffic?
    *   **Request Duration:** Are your users experiencing slowdowns? This is a critical metric.
    *   **Request Failures/sec:** Is the chaos experiment causing errors in your application?
    *   **Overall CPU and Memory:** Correlated with the application metrics.

*   **Best for:** Understanding the **end-user impact** of a chaos experiment, not just the infrastructure load.

### Summary: Which One to Use?

| Monitoring Tool | Best For... | Setup Required |
| :--- | :--- | :--- |
| **VM Overview** | A quick, simple "is it working?" check. | None |
| **Azure Monitor Metrics** | Detailed, custom, real-time charting of specific metrics. | None |
| **VM Insights** | A complete, pre-built performance dashboard. The recommended standard. | Enable Insights (deploys an agent) |
| **App Insights Live Metrics** | Seeing the real-time impact on your application's performance and reliability. | Instrument your app with the App Insights SDK |

For your first experiment, start with **Azure Monitor Metrics** (Method 2). It gives you the perfect balance of detail and ease of use. As you get more advanced, graduate to using **VM Insights** and **Application Insights** for a complete picture.