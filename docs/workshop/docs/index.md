# Introduction

This guide serves as both a solution accelerator and a learning tool for developers who want to build AI-powered solutions built on top of Azure Database for PostgreSQL and Azure AI Services. The **Woodgrove Bank** solution is an actively updated project that will reflect the latest features and best practices for development of AI-enabled applications and RAG-based copilots on the Azure AI platform.

To deploy this solution accelerator, ensure you have access to an [Azure subscription](https://azure.microsoft.com/en-us/pricing/purchase-options/azure-account?icid=azurefreeaccount) with the necessary permissions to create resource groups and resources. Follow the steps in [Azure Account Set Up](https://github.com/microsoft/document-generation-solution-accelerator/blob/main/docs/AzureAccountSetUp.md)

Check the [Azure Products by Region](https://azure.microsoft.com/en-us/explore/global-infrastructure/products-by-region/?products=all&regions=all) page and select a **region** where the following services are available:  

- Azure AI Foundry 
- Azure OpenAI Service 
- Azure AI Search
- Azure AI Content Understanding
- Embedding Deployment Capacity  
- GPT Model Capacity
- [Azure Semantic Search](./docs/AzureSemanticSearchRegion.md)  

Here are some example regions where the services are available: East US, East US2, Australia East, UK South, France Central.

### ⚠️ Important: Check Azure OpenAI Quota Availability  

➡️ To ensure sufficient quota is available in your subscription, please follow **[Quota check instructions guide](./docs/quota_check.md)** before you deploy the solution.

| [![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/microsoft/Conversation-Knowledge-Mining-Solution-Accelerator) | [![Open in Dev Containers](https://img.shields.io/static/v1?style=for-the-badge&label=Dev%20Containers&message=Open&color=blue&logo=visualstudiocode)](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/microsoft/Conversation-Knowledge-Mining-Solution-Accelerator) |
|---|---|
        
### **Configurable Deployment Settings**  

When you start the deployment, most parameters will have **default values**, but you can update the following settings:  

| **Setting** | **Description** | **Default value** |
|------------|----------------|------------|
| **Azure Region** | The region where resources will be created. | eastus | 
| **Environment Name** | A **3-20 character alphanumeric value** used to generate a unique ID to prefix the resources. | kmtemplate |
| **Azure AI Content Understanding Location** | Select from a drop-down list of values. | swedencentral |
| **Secondary Location** | A **less busy** region for **Azure SQL and Azure Cosmos DB**, useful in case of availability constraints. | eastus2 |
| **Deployment Type** | Select from a drop-down list. | GlobalStandard |
| **GPT Model** | Choose from **gpt-4, gpt-4o, gpt-4o-mini** | gpt-4o-mini |  
| **GPT Model Deployment Capacity** | Configure capacity for **GPT models**. | 30k |
| **Embedding Model** | Default: **text-embedding-ada-002**. | text-embedding-ada-002 |
| **Embedding Model Capacity** | Set the capacity for **embedding models**. | 80k |


### [Optional] Quota Recommendations  
By default, the **GPT model capacity** in deployment is set to **30k tokens**.  
> **We recommend increasing the capacity to 100k tokens for optimal performance.** 

To adjust quota settings, follow these [steps](./docs/AzureGPTQuotaSettings.md)  

