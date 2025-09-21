# 🔗 **Learning Resources & Links for Azure Chaos Engineering Roadmap**

*Comprehensive collection of documentation, tutorials, and learning materials*

---

## **🔥 CRITICAL SKILLS RESOURCES (Priority 1)**

### **1. Azure Resource Manager (ARM) SDK**

#### **Official Documentation:**
- **Azure SDK for .NET Overview**: https://docs.microsoft.com/en-us/dotnet/azure/
- **Azure Resource Manager Client Library**: https://docs.microsoft.com/en-us/dotnet/api/overview/azure/resourcemanager-readme
- **Azure SDK Design Guidelines**: https://azure.github.io/azure-sdk/dotnet_introduction.html
- **ARM Template Reference**: https://docs.microsoft.com/en-us/azure/templates/

#### **Specific Service SDKs:**
- **Azure.ResourceManager.Chaos**: https://docs.microsoft.com/en-us/dotnet/api/azure.resourcemanager.chaos
- **Azure.ResourceManager.AppService**: https://docs.microsoft.com/en-us/dotnet/api/azure.resourcemanager.appservice
- **Azure.ResourceManager.CosmosDB**: https://docs.microsoft.com/en-us/dotnet/api/azure.resourcemanager.cosmosdb
- **Azure.ResourceManager.KeyVault**: https://docs.microsoft.com/en-us/dotnet/api/azure.resourcemanager.keyvault
- **Azure.ResourceManager.Compute**: https://docs.microsoft.com/en-us/dotnet/api/azure.resourcemanager.compute
- **Azure.ResourceManager.Network**: https://docs.microsoft.com/en-us/dotnet/api/azure.resourcemanager.network

#### **Tutorials & Samples:**
- **Azure SDK Samples Repository**: https://github.com/Azure/azure-sdk-for-net/tree/main/samples
- **ARM Client Quickstart**: https://github.com/Azure/azure-sdk-for-net/blob/main/sdk/resourcemanager/Azure.ResourceManager/samples/README.md
- **Azure Resource Management with .NET**: https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/manage-resources-dotnet

### **2. Polly Resilience Library**

#### **Official Documentation:**
- **Polly Main Documentation**: https://www.thepollyproject.org/
- **Polly GitHub Repository**: https://github.com/App-vNext/Polly
- **Polly Wiki**: https://github.com/App-vNext/Polly/wiki

#### **Specific Policy Types:**
- **Retry Policies**: https://github.com/App-vNext/Polly/wiki/Retry
- **Timeout Policies**: https://github.com/App-vNext/Polly/wiki/Timeout
- **Circuit Breaker**: https://github.com/App-vNext/Polly/wiki/Circuit-Breaker
- **Policy Wrapping**: https://github.com/App-vNext/Polly/wiki/PolicyWrap

#### **Learning Resources:**
- **Polly Best Practices**: https://docs.microsoft.com/en-us/dotnet/architecture/microservices/implement-resilient-applications/implement-http-call-retries-exponential-backoff-polly
- **Polly with HttpClient**: https://docs.microsoft.com/en-us/aspnet/core/fundamentals/http-requests?view=aspnetcore-6.0#polly-based-handlers
- **Polly Samples**: https://github.com/App-vNext/Polly-Samples

### **3. Advanced C# Async Patterns**

#### **Official Documentation:**
- **Async Programming Guide**: https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/async/
- **Task-based Asynchronous Pattern (TAP)**: https://docs.microsoft.com/en-us/dotnet/standard/asynchronous-programming-patterns/task-based-asynchronous-pattern-tap
- **ConfigureAwait Best Practices**: https://devblogs.microsoft.com/dotnet/configureawait-faq/

#### **Advanced Topics:**
- **CancellationToken Deep Dive**: https://docs.microsoft.com/en-us/dotnet/standard/threading/cancellation-in-managed-threads
- **ValueTask Performance**: https://devblogs.microsoft.com/dotnet/understanding-the-whys-whats-and-whens-of-valuetask/
- **Async Streams**: https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/tutorials/generate-consume-asynchronous-stream

#### **Learning Resources:**
- **Stephen Cleary's Async/Await Best Practices**: https://docs.microsoft.com/en-us/archive/msdn-magazine/2013/march/async-await-best-practices-in-asynchronous-programming
- **Async/Await FAQ**: https://devblogs.microsoft.com/dotnet/async-await-faq/
- **Parallel Programming in .NET**: https://docs.microsoft.com/en-us/dotnet/standard/parallel-programming/

---

## **🛠️ INTERMEDIATE SKILLS RESOURCES (Priority 2)**

### **4. OpenTelemetry & Monitoring**

#### **Official Documentation:**
- **OpenTelemetry .NET**: https://opentelemetry.io/docs/instrumentation/net/
- **OpenTelemetry GitHub**: https://github.com/open-telemetry/opentelemetry-dotnet
- **System.Diagnostics.Metrics**: https://docs.microsoft.com/en-us/dotnet/core/diagnostics/metrics

#### **Microsoft-specific Monitoring:**
- **Application Insights for .NET**: https://docs.microsoft.com/en-us/azure/azure-monitor/app/asp-net-core
- **Azure Monitor**: https://docs.microsoft.com/en-us/azure/azure-monitor/
- **Geneva Monitoring (Internal)**: https://aka.ms/geneva-docs

#### **Learning Resources:**
- **OpenTelemetry Getting Started**: https://opentelemetry.io/docs/instrumentation/net/getting-started/
- **Custom Metrics in .NET**: https://docs.microsoft.com/en-us/dotnet/core/diagnostics/metrics-instrumentation
- **Distributed Tracing**: https://docs.microsoft.com/en-us/azure/azure-monitor/app/distributed-tracing

### **5. Dependency Injection & Factory Patterns**

#### **Official Documentation:**
- **Dependency Injection in .NET**: https://docs.microsoft.com/en-us/dotnet/core/extensions/dependency-injection
- **Service Container**: https://docs.microsoft.com/en-us/dotnet/core/extensions/dependency-injection-usage
- **Configuration in .NET**: https://docs.microsoft.com/en-us/dotnet/core/extensions/configuration

#### **Design Patterns:**
- **Factory Pattern**: https://docs.microsoft.com/en-us/dotnet/standard/design-guidelines/factory
- **Service Locator Pattern**: https://docs.microsoft.com/en-us/dotnet/architecture/microservices/implement-resilient-applications/use-httpclientfactory-to-implement-resilient-http-requests

#### **Learning Resources:**
- **DI Best Practices**: https://docs.microsoft.com/en-us/dotnet/core/extensions/dependency-injection-guidelines
- **ASP.NET Core DI**: https://docs.microsoft.com/en-us/aspnet/core/fundamentals/dependency-injection

### **6. Regular Expressions**

#### **Official Documentation:**
- **.NET Regex Guide**: https://docs.microsoft.com/en-us/dotnet/standard/base-types/regular-expressions
- **Regex Class**: https://docs.microsoft.com/en-us/dotnet/api/system.text.regularexpressions.regex
- **Regex Best Practices**: https://docs.microsoft.com/en-us/dotnet/standard/base-types/best-practices

#### **Learning Resources:**
- **Regex Tutorial**: https://regexone.com/
- **Regex Testing**: https://regex101.com/
- **Azure Resource ID Patterns**: https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/resource-name-rules

---

## **🔧 SPECIALIZED AREAS RESOURCES (Priority 3)**

### **7. Application Insights & Telemetry**

#### **Official Documentation:**
- **Application Insights Overview**: https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-insights-overview
- **TelemetryClient API**: https://docs.microsoft.com/en-us/dotnet/api/microsoft.applicationinsights.telemetryclient
- **Custom Telemetry**: https://docs.microsoft.com/en-us/azure/azure-monitor/app/api-custom-events-metrics

#### **Learning Resources:**
- **Application Insights for .NET**: https://docs.microsoft.com/en-us/azure/azure-monitor/app/asp-net-core
- **Telemetry Correlation**: https://docs.microsoft.com/en-us/azure/azure-monitor/app/correlation
- **Performance Monitoring**: https://docs.microsoft.com/en-us/azure/azure-monitor/app/performance-counters

### **8. Geneva Synthetics Framework**

#### **Microsoft Internal Resources:**
- **Geneva Documentation**: https://aka.ms/geneva-docs
- **Geneva Synthetics Guide**: https://aka.ms/geneva-synthetics
- **MDM Documentation**: https://aka.ms/mdm-docs
- **Geneva Metrics**: https://genevametrics.azurewebsites.net/

### **9. Azure Authentication & Security**

#### **Official Documentation:**
- **Azure Identity Library**: https://docs.microsoft.com/en-us/dotnet/api/overview/azure/identity-readme
- **Managed Identity**: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/
- **Key Vault .NET SDK**: https://docs.microsoft.com/en-us/dotnet/api/overview/azure/key-vault

#### **Security Best Practices:**
- **Azure Security Best Practices**: https://docs.microsoft.com/en-us/azure/security/fundamentals/best-practices-and-patterns
- **Service Principal Authentication**: https://docs.microsoft.com/en-us/azure/active-directory/develop/app-objects-and-service-principals
- **Certificate Authentication**: https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-certificate-credentials

---

## **📚 ADDITIONAL LEARNING RESOURCES**

### **Microsoft Learn Paths:**
- **Azure Fundamentals**: https://docs.microsoft.com/en-us/learn/paths/azure-fundamentals/
- **Azure Developer**: https://docs.microsoft.com/en-us/learn/paths/azure-developer/
- **Chaos Engineering**: https://docs.microsoft.com/en-us/learn/modules/intro-to-chaos-engineering/

### **Books & In-Depth Resources:**
- **C# in Depth (Jon Skeet)**: https://csharpindepth.com/
- **Pro .NET 5 Platform**: https://www.apress.com/gp/book/9781484272373
- **Azure Architecture Guide**: https://docs.microsoft.com/en-us/azure/architecture/

### **GitHub Repositories & Samples:**
- **Azure Samples**: https://github.com/Azure-Samples
- **Azure SDK Samples**: https://github.com/Azure/azure-sdk-for-net/tree/main/samples
- **Chaos Engineering Samples**: https://github.com/Azure/azure-chaos-engineering

### **Community & Forums:**
- **Stack Overflow - Azure**: https://stackoverflow.com/questions/tagged/azure
- **Microsoft Q&A**: https://docs.microsoft.com/en-us/answers/
- **Azure DevOps Community**: https://developercommunity.visualstudio.com/spaces/21/index.html

### **Blogs & Articles:**
- **Azure Developer Blog**: https://devblogs.microsoft.com/azure-sdk/
- **Azure Architecture Blog**: https://techcommunity.microsoft.com/t5/azure-architecture-blog/bg-p/AzureArchitectureBlog
- **Chaos Engineering Blog**: https://principlesofchaos.org/

### **Video Learning:**
- **Microsoft Learn Videos**: https://docs.microsoft.com/en-us/shows/
- **Azure Friday**: https://docs.microsoft.com/en-us/shows/azure-friday/
- **Channel 9 Azure**: https://channel9.msdn.com/Search?term=azure

### **Hands-on Labs:**
- **Azure Learn Sandbox**: https://docs.microsoft.com/en-us/learn/
- **Microsoft Hands-on Labs**: https://www.microsoft.com/handsonlabs/
- **Azure DevTest Labs**: https://azure.microsoft.com/en-us/services/devtest-lab/

---

## **🎯 QUICK START CHECKLIST**

### **Week 1 Focus:**
1. ✅ Set up Azure SDK development environment
2. ✅ Complete Azure Resource Manager quickstart
3. ✅ Practice basic Polly retry policies
4. ✅ Review async/await fundamentals

### **Week 2-3 Focus:**
1. ✅ Build simple chaos experiment
2. ✅ Add basic monitoring with OpenTelemetry
3. ✅ Implement dependency injection patterns
4. ✅ Practice Azure authentication

### **Week 4+ Focus:**
1. ✅ Advanced monitoring configurations
2. ✅ Complex resilience patterns
3. ✅ Production-ready implementations
4. ✅ Performance optimization

---

*This comprehensive resource list provides direct access to all the technologies and patterns identified in your Azure Chaos Engineering codebase!* 🚀