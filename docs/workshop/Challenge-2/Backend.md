
## Backend Overview

**Folder**: [`src/api`](https://github.com/microsoft/Conversation-Knowledge-Mining-Solution-Accelerator/tree/main/src/api)

The backend is a **Python Quart app** that processes queries, generates insights, and communicates with databases and AI services.

### Key Features

1. ** Azure OpenAI Integration**

- Natural language processing and chart generation.

2. ** Data Access**

- SQL for structured data.
- Azure Cognitive Search for transcripts.

3. ** Chat History**

- Cosmos DB for storing user conversations.

4. ** Chart Processing**

- Converts results to chart-ready JSON.

###  Workflow (Backend)

| Step | Description | Maps to Architecture |
|------|-------------|----------------------|
| 1. **Service Init** | Load AI and data sources. |  App Service |
| 2. **Handle Queries** | Interpret and act on requests. |  Azure OpenAI |
| 3. **Generate Insights** | Return results for chat/charts. |  Semantic Kernel |
| 4. **Store History** | Save chats to Cosmos DB. |  Cosmos DB |

###  Tools & Libraries

- **Quart**
- **Azure OpenAI**
- **CosmosDB SDK**
- **SQLAlchemy**

---