# Backend Overview

## Key Features
1. **Azure OpenAI Integration**:
    - Processes natural language queries and generates responses.
    - Supports dynamic chart generation based on user queries.

2. **Structured Data Integration**:
    - Queries SQL databases for structured data (e.g., customer interactions, complaints).
    - Uses Azure Cognitive Search for retrieving indexed call transcripts.

3. **Conversation History Management**:
    - Stores and retrieves conversation history using CosmosDB.
    - Supports feedback and message updates.

4. **Chart Data Processing**:
    - Processes RAG (Retrieval-Augmented Generation) responses to generate chart-compatible JSON data.

---

## Workflow
1. **Initialize Services**:
    - Sets up Azure OpenAI, CosmosDB, and other integrations.

2. **Process Requests**:
    - Handles API requests for fetching chart data, filters, and conversation history.

3. **Generate Insights**:
    - Uses Azure OpenAI for unstructured queries.
    - Executes SQL queries or Cognitive Search for structured data.

4. **Chatbot Interaction**:
    - Processes user queries and generates responses or charts.

---

## Tools and Libraries
- **Quart**: For building the backend application.
- **Azure OpenAI**: For natural language processing.
- **CosmosDB**: For managing conversation history.
- **Azure Cognitive Search**: For retrieving indexed data.

---

## How It Works
The backend acts as the core processing engine, handling API requests, generating insights, and managing data storage.