<!-- ## Chart Component

The Chart component is a dynamic and responsive charting module that:

    - Fetches chart data and filter metadata from APIs.
    - Dynamically renders various chart types based on configuration.
    - Supports filtering to update chart data in real-time.
    - Manages layout and responsiveness for a seamless user experience.


### Key Functionalities
Data Fetching
    Chart Data:
        The getChartData function fetches chart data from the backend.
            - If filters are applied, it uses fetchChartDataWithFilters to fetch filtered data.
            - If no filters are applied, it uses fetchChartData to fetch default data.
Chart Rendering
    The renderChart function dynamically renders charts based on their type:
            - Card: Displays a single value with a description.
            - Donut Chart: Displays data as a donut chart.
            - Bar Chart: Displays data as a horizontal bar chart.
            - Table: Displays data in a tabular format.
            - Word Cloud: Displays data as a word cloud.

4. Filtering
    Applying Filters:
        - The applyFilters function is triggered when the user applies new filters via the ChartFilter component.
        - It calls getChartData with the updated filters to fetch filtered chart data.

 -->
# Chart Component Walkthrough

This document provides a comprehensive overview of the `Chart` component in the **Conversation Knowledge Mining Solution Accelerator**. It explains how the component works, its interaction with other parts of the application, and its relevance to both technical and non-technical users.

---

## **Overview of the Chart Component**

The `Chart` component is a dynamic and interactive visualization module that displays insights derived from conversation data. It supports multiple chart types (e.g., Donut Chart, Bar Chart, Word Cloud, etc.) and allows users to filter and explore data interactively.

---

## **Key Features**

1. **Dynamic Chart Rendering**:
   - Supports multiple chart types such as Donut Charts, Bar Charts, Word Clouds, and Tables.
   - Automatically adjusts layout and size based on the window dimensions.

2. **Interactive Filtering**:
   - Users can apply filters (e.g., Topics, Sentiments, Satisfaction levels) to refine the data displayed in the charts.

3. **Real-Time Data Updates**:
   - Fetches data dynamically from the backend based on user interactions and updates the charts in real-time.

4. **Responsive Design**:
   - Automatically adjusts chart layouts and dimensions to fit the screen size.

5. **Error Handling**:
   - Gracefully handles errors during data fetching and displays fallback messages when necessary.

---

## **How It Works**

### **1. Data Flow**

The `Chart` component interacts with the backend and other frontend modules to fetch, process, and display data:

1. **Frontend (`Chart` Component)**:
   - Fetches chart data and filter options using API utility functions (`api.ts`).
   - Dynamically renders charts based on the data and configuration.

2. **Backend (`function_app.py`)**:
   - Provides APIs (`/api/fetchChartData`, `/api/fetchChartDataWithFilters`, `/api/fetchFilterData`) to serve chart data and filter options.
   - Dynamically generates SQL queries based on user-selected filters.

3. **API Utility (`api.ts`)**:
   - Acts as a bridge between the frontend and backend.
   - Provides reusable functions to fetch chart data, filter data, and layout configurations.

---

### **2. Key Components**

#### **Frontend: Chart Component**
**Responsibilities**:
- Fetches chart data using `getChartData` and `fetchChartDataWithFilters`.
- Dynamically renders charts based on their type (e.g., Donut Chart, Word Cloud).
- Handles user interactions such as applying filters and resizing the window.

#### **Backend: Azure Function**
**Responsibilities**:
- Connects to the SQL database using secure credentials.
- Provides APIs to fetch chart data and filter options.
- Dynamically builds SQL queries based on user-selected filters.

#### **API Utility**
**Responsibilities**:
- Provides reusable functions to interact with backend APIs.
- Handles API calls for fetching chart data, filter data, and layout configurations.
- Manages error handling and response parsing.

---

### **3. Technical Details**

#### **Dynamic Chart Rendering**
The `Chart` component uses the `renderChart` function to render different chart types dynamically:
```tsx
const renderChart = (chart: ChartConfigItem, heightInPixes: number) => {
  switch (chart.type) {
    case "card":
      return <Card ... />;
    case "donutchart":
      return <DonutChart ... />;
    case "bar":
      return <BarChart ... />;
    case "table":
      return <TopicTable ... />;
    case "wordcloud":
      return <WordCloudChart ... />;
    default:
      console.warn(`Unknown chart type: ${chart.type}`);
      return null;
  }
};