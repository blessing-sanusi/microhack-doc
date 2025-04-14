# API Overview

## Key Endpoints

### **Chart Data**
1. **`GET /api/fetchChartData`**:
    - Fetches default chart data.

2. **`POST /api/fetchChartDataWithFilters`**:
    - Fetches chart data based on user-selected filters.

3. **`GET /api/fetchFilterData`**:
    - Retrieves available filter options.

---

### **Chatbot**
1. **`POST /api/chat`**:
    - Processes user queries and generates responses.
    - Supports dynamic chart generation.

---

### **Conversation History**
1. **`POST /history/generate`**:
    - Creates a new conversation or appends messages to an existing one.

2. **`POST /history/update`**:
    - Updates an existing conversation with new messages or feedback.

3. **`GET /history/list`**:
    - Lists all conversations for a user.

4. **`POST /history/read`**:
    - Retrieves a specific conversation and its messages.

5. **`DELETE /history/delete`**:
    - Deletes a specific conversation.

---

## Tools and Libraries
- **Quart**: For building API endpoints.
- **Azure OpenAI**: For generating insights.
- **CosmosDB**: For managing conversation history.

---

## How It Fits
The API layer connects the frontend and backend, enabling seamless communication and data exchange.