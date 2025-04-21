
---

## Frontend Overview

📁 **Folder**: [`src/web-app`](https://github.com/microsoft/Conversation-Knowledge-Mining-Solution-Accelerator/tree/main/src/web-app)

The frontend is a **React-based web interface** that allows users to explore insights from conversations, interact with an AI-powered chatbot, and view dynamic visualizations.

### ✅ Key Features

1. ** Dynamic Chart Rendering**
   - Charts like Donut, Bar, and Word Cloud using **Chart.js**.
   - Visualizes insights such as sentiment, topics, and keywords.

2. ** Chatbot Interface**
   - Allows users to query via natural language.
   - Auto-generates insights and charts.

3. ** Filter Management**
   - Filters such as **Sentiment**, **Entity**, **Topic**.
   - Updates chart views dynamically.

4. ** Responsive UI**
   - Optimized for multiple screen sizes.

5. ** Error Handling**
   - User-friendly error messages for API failures.

### Workflow (Frontend)

| Step | Description | Maps to Architecture |
|------|-------------|----------------------|
| 1. **Data Fetching** | Fetch chart/filter data. | 🎯 API Layer |
| 2. **Chatbot Queries** | Send messages to backend. | 🤖 Azure OpenAI |
| 3. **Chart Rendering** | Render chart components. | 📊 Web Front-end |
| 4. **History Sync** | Display chat history. | 🗃 Cosmos DB |

###  Tools & Libraries

- **React**
- **Chart.js**
- **Axios**

---
