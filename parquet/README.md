# anomaliesdetection
Anomalies Detection In API-logs

### Project Structures

This project includes following files:

```
$ tree .
.
├── PySparkParquet.ipynb
├── README.md
└── apache_logs.parquet

1 directory, 3 files
```
- PySparkParquet.ipynb: Notebook to analyze the Anomalies
- apache_logs.parquet: Log data in parquet format
- README: Project Description

### Project Description
The Apache Access Log Analyzer is a tool for analyzing Apache web server access log data. It provides insights into various aspects of web server activity, including request methods, response codes, popular endpoints, and peak traffic times.

### Installation and Usage
1. Clone this repository to the local machine.
2. Ensure you have Python and Apache Spark installed.
3. Install the required Python packages using pip:
4. Generate sample Apache access log data using the provided Python script.
5. Run the log analyzer script to perform analysis on the generated log data.
6. View the analysis results displayed in notebook/console.


## Project analysis
The Apache Access Log Analyzer is a tool designed to provide insights into Apache web server activity by analyzing access log data. The project includes functionalities to generate sample Apache access logs, process them using Apache Spark, and derive meaningful insights from the data.

Key Features:
1. Log Generation: Utilizes Python script to generate sample Apache access log data with configurable parameters such as IP addresses, HTTP methods, response codes, and content sizes.
2. Data Processing: Utilizes Apache Spark for efficient processing of large log files, including data transformation and aggregation tasks.
3. Analysis: The analysis of the Apache access log data revealed several key insights:
- Distribution of requests by HTTP method.
- Frequency of different response codes, indicating server status and potential errors.
- Popular endpoints accessed by users, providing insights into the most requested content.
- Peak traffic times, highlighting periods of high activity on the web server.

###Project Summary/Explanation

The Spark application is designed to ingest Apache Access logs stored in semi-structured parquet format. It preprocesses the logs to extract relevant information such as IP addresses, response codes, endpoints, content size, and timestamps. Feature extraction is then performed to calculate statistics for different aspects of the logs, including response code frequencies, traffic patterns by IP address, and content size distributions across endpoints.

Anomaly detection algorithms are applied to the extracted features to identify anomalies. These algorithms may involve setting thresholds for certain statistics or using more sophisticated machine learning techniques to detect unusual patterns in the data. Detected anomalies are flagged and highlighted in the output for further investigation.

### Findings and Insights
- **HTTP Methods**: The majority of requests were `GET` requests, followed by `POST` and `PUT`.
- **Response Codes**: The analysis showed a high percentage of successful requests (`200` status code), but also a notable number of error responses (`4xx` and `5xx` status codes), indicating potential issues with some requests.
- **Popular Endpoints**: Certain endpoints, such as `/index.html` and `/about`, were accessed more frequently than others, suggesting popular content or pages.
- **Peak Traffic Times**: Traffic tended to peak during specific hours of the day, indicating periods of high user activity.

### Future Work
- Incorporate visualizations to present analysis results in a more visually appealing format.
- Expand analysis capabilities to include additional metrics such as user agents, referral sources, and geographic locations.
- Implement advanced analytics techniques such as anomaly detection and predictive modeling for deeper insights into web server behavior.

###Final Output

The final output of the Spark application includes:

- Summary statistics for response codes, traffic patterns, and content size distributions.
- Detected anomalies, along with relevant information such as timestamps, IP addresses, and endpoints.

###Reference

- Apache Spark Documentation - For detailed information on using Spark for data processing and analysis.
- Apache Logging Services - For understanding Apache logging formats and conventions.
