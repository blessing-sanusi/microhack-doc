## Chart Component

The Chart component is a dynamic and responsive charting module that:

    •	Fetches chart data and filter metadata from APIs.
    •	Dynamically renders various chart types based on configuration.
    •	Supports filtering to update chart data in real-time.
    •	Manages layout and responsiveness for a seamless user experience.


### Key Functionalities
Data Fetching
    Chart Data:
        The getChartData function fetches chart data from the backend.
        o	If filters are applied, it uses fetchChartDataWithFilters to fetch filtered data.
        o	If no filters are applied, it uses fetchChartData to fetch default data.
Chart Rendering
    The renderChart function dynamically renders charts based on their type:
        o	Card: Displays a single value with a description.
        o	Donut Chart: Displays data as a donut chart.
        o	Bar Chart: Displays data as a horizontal bar chart.
        o	Table: Displays data in a tabular format.
        o	Word Cloud: Displays data as a word cloud.

4. Filtering
•	Applying Filters:
o	The applyFilters function is triggered when the user applies new filters via the ChartFilter component.
o	It calls getChartData with the updated filters to fetch filtered chart data.


