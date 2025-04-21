##  API Overview

 **Folder**: [`src/api`](https://github.com/microsoft/Conversation-Knowledge-Mining-Solution-Accelerator/tree/main/src/api)

###  Key Endpoints

####  Chart & Filters

- `GET /api/fetchChartData`
- `POST /api/fetchChartDataWithFilters`
- `GET /api/fetchFilterData`

####  Chatbot

- `POST /api/chat`

####  Conversation History

- `POST /history/generate`
- `POST /history/update`
- `GET /history/list`
- `POST /history/read`
- `DELETE /history/delete`

###  Workflow (API Layer)

| Step | Description | Maps to Architecture |
|------|-------------|----------------------|
| 1. **Receive Request** | From frontend. | 🌐 Web Frontend |
| 2. **Route Request** | To processing service. | ⚙️ App Service |
| 3. **Return Response** | JSON for frontend. | 🔁 Feedback Loop |

###  Tools & Libraries

- **Quart**
- **Azure OpenAI**
- **CosmosDB SDK**

---

##  Architecture to Code Mapping

| Component                          | Location                        |
|-----------------------------------|----------------------------------|
| Web Front-End                     | `src/web-app`                    |
| API Layer                         | `src/api`                        |
| Azure OpenAI + Semantic Kernel    | `src/api/conversationInsightsProcessor` |
| Chart Data Processing             | `src/api/chartProcessor/`        |
| Vector Search + SQL               | `src/api/vectorIndexer/`        |
| Cosmos DB for History             | Handled in `history` endpoints   |

---