# Automating Selenium Tests in Azure Pipelines

The lab is available at [ADO Lab - Selenium | Microsoft GitHub](https://github.com/microsoft/azuredevopslabs/tree/master/labs/vstsextend/selenium) as well as at [Automating Selenium Tests in Azure Pipelines](https://www.azuredevopslabs.com/labs/vstsextend/selenium/).

## Things to be considered for this lab (not covered in the Microsoft documentation)
* The lab uses the VM name while creating other resources including storage account. To avoid naming constraints, use VM Name as `vmabhi`.
* The lab runs `SQL Server 2017 Express` on the VM which doesn't allow remote connections. Hence, you cannot use hosted agents to run this lab.
![alt txt](/images/sql-express-on-vm.jpg)
* The self hosted agent is installed on the VM containing SQL Server. 
* The agent requires the following to be installed to run the build successfully:
    * Visual Studio
    * [.NET Framework 4.6.1](https://dotnet.microsoft.com/en-us/download/dotnet-framework/thank-you/net461-developer-pack-offline-installer)
    * [.NET Framework 4.5.2](https://dotnet.microsoft.com/en-us/download/dotnet-framework/thank-you/net452-developer-pack-offline-installer)
    * [.NET Framework 4.5.1](https://dotnet.microsoft.com/en-us/download/dotnet-framework/thank-you/net451-developer-pack-offline-installer)
* Selenium test result shows 5 failed after the run whereas the lab has all of them run successfully. This is still alright as it shows Selenium execution partially successful.
![alt txt](/images/selenium-test-result.jpg)
