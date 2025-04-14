# Frontend Overview

## Key Features
1. **Dynamic Chart Rendering**:
      - Displays charts (e.g., Donut, Bar, Word Cloud) using Chart.js.
      - Updates dynamically based on user-selected filters.

2. **Chatbot Integration**:
      - Provides a conversational interface for users.
      - Supports queries for insights, dynamic chart generation, and structured data retrieval.

3. **Filter Management**:
      - Allows users to refine data displayed in charts using filters (e.g., Sentiment, Topics).

4. **Responsive Design**:
      - Adapts layout and components to different screen sizes.

5. **Error Handling**:
      - Displays fallback messages for failed API calls.

---

## Workflow
1. **Data Fetching**:
      - Calls APIs like `/api/fetchChartData` and `/api/fetchFilterData` to retrieve chart data and filters.

2. **Chatbot Interaction**:
      - Sends user queries to `/api/chat` for processing.
      - Displays responses, including dynamically generated charts.

3. **Filter Application**:
      - Sends filter data to `/api/fetchChartDataWithFilters` and updates charts.

---

## Tools and Libraries
   - **React**: For building the user interface.
   - **Chart.js**: For rendering charts.
   - **Axios/Fetch**: For API communication.

---

## How It Works
The frontend provides a user-friendly interface for exploring insights, interacting with the chatbot, and visualizing data dynamically.