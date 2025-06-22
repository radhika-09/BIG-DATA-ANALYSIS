#BIG DATA ANALYSIS

*COMPANY*: CODTECH IT SOLUTIONS

*NAME*: RADHIKA

*INTERN ID*: CT04DF1997

*DOMAIN*: DATA ANALYTICS

*DURATION*: 4 WEEKS

*MENTOR*: NEELA SANTOSH

<b>COVID-19 Data Analysis and Visualization<br></b>
<b>Introduction</b><br>
The global outbreak of COVID-19 led to a wealth of publicly available data that can be analyzed to uncover trends and insights. This project aimed to analyze and visualize COVID-19 data using PySpark, a big data processing framework, and Plotly, a powerful visualization library. The analysis covers the entire data pipeline—from loading the raw dataset to presenting rich visual summaries of global and country-level COVID-19 trends.

1. Setup and Library Installation
To begin, the working environment was set up by installing PySpark using the command !pip install pyspark. This step is essential for enabling large-scale data processing within a distributed computing framework. After PySpark was successfully installed, key libraries and modules from PySpark SQL were imported, such as SparkSession, functions, and Window, which allow for SQL-like operations and windowed transformations on data.

For data visualization, the Plotly libraries plotly.express and plotly.graph_objects were imported. Plotly is well-suited for generating interactive charts and dashboards, making it ideal for visualizing time-series and geographical data associated with the spread of COVID-19.

2. Loading and Inspecting the Dataset
The next step was loading the COVID-19 dataset in CSV format into a PySpark DataFrame. The dataset contains daily reports of confirmed, death, and recovered cases across various countries and regions. Initial exploration was done using df.show() to display sample records, df.printSchema() to examine data types, and df.describe() to get statistical summaries.

Missing or inconsistent data entries were identified, including null values and misformatted dates. These were handled appropriately to ensure the quality and integrity of subsequent analysis.

3. Data Cleaning and Feature Engineering
Data preparation is crucial for meaningful analysis. In this project, the Date column was first converted from string format to DateType using the to_date() function. This conversion enabled accurate sorting and filtering based on dates.

To understand the daily spread of the virus, the lag() function in combination with PySpark’s window functions was used to calculate new daily confirmed cases. A window was defined partitioned by Country/Region and ordered by Date. The difference between the current and previous day’s confirmed cases gave the number of new cases for each country on each day. Any null values resulting from this operation (e.g., the first record per country) were replaced with 0 using na.fill().

4. Exploratory Data Analysis (EDA)
Exploratory Data Analysis was carried out to derive initial insights. The number of rows and columns in the dataset was determined to assess the scale of data. Aggregations were performed to compute total confirmed, deaths, and recovered cases grouped by Country/Region and by Date.

Time-series analysis was done by grouping data daily to study global trends over time. Country-wise aggregations helped identify the most and least affected regions, as well as how the pandemic evolved across borders.

5. Data Visualization Using Plotly
To bring the insights to life, several interactive visualizations were created:

Line Plot: Displayed global daily new COVID-19 cases over time, helping identify waves and spikes.

Bar Chart: Visualized the top 10 countries with the highest number of deaths, providing a comparative view of mortality impact.

Multi-line Chart: Illustrated global trends of confirmed, recovered, and death cases, showcasing the pandemic’s trajectory.

Pie Chart: Showed the share of recovered cases among the top 5 countries with the highest recovery numbers.

Box Plot: Highlighted the distribution of daily new cases in the top 5 countries by total confirmed cases, helping identify outliers and variation in daily case counts.

Each visualization was made using Plotly’s interactive features like hover tooltips, zoom, and filtering, making the analysis more intuitive and insightful.

6. Enhancements
To further enhance the analysis, several advanced visualization and filtering techniques were suggested:

Heatmap: Could be used to show correlations between different variables like deaths vs recoveries.

Geographical Maps: To show the global spread with bubble or choropleth maps.

Animated Charts: To visualize how cases grew over time dynamically.

Interactive Filters: By region or date to focus on specific insights.

These additions would provide even deeper understanding and more user engagement.

7. Tools and Technologies Used
PySpark: Provided the foundation for big data processing, efficient aggregations, and windowed operations.

pandas: Spark DataFrames were converted to pandas for compatibility with Plotly.

Plotly: Enabled the creation of rich, interactive, and publication-quality charts suitable for web and report use.

<b>Conclusion<br></b>
This project successfully demonstrated the use of PySpark and Plotly to perform end-to-end data analysis and visualization of a real-world COVID-19 dataset. By combining powerful big data tools with interactive plotting libraries, valuable insights into the progression of the pandemic were uncovered, setting a strong foundation for further epidemiological modeling or dashboard development.
