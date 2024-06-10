# Zillow Data Analytics using AWS

![Architecture drawio (1)](https://github.com/bhavanachitragar/zillow-data-analytics/assets/91766461/d36ab26a-5f22-4866-8e1b-ddea2ed2bd98)

## This architecture leverages:
- Airflow: For scheduling and orchestration of the data pipeline tasks.
- EC2: For running the Python scripts for data extraction and transformation.
- Lambda Functions: For serverless, triggered processing of data transfer between S3 buckets.
- S3: For storing data at various stages of the pipeline.
- Redshift: For efficient data warehousing and analytics.
- QuickSight: For data visualization and exploration.

## Steps included:
1. Python Script: Extracts data from Zillow in JSON format and stores it in an S3 bucket.
2. S3 Bucket (Staging): Stores the initial extracted JSON data.
3. AWS Lambda Function 1 (Data Transfer): Triggers upon new data in the staging S3 bucket and copies the JSON data to a destination S3 bucket.
4. S3 Bucket (Processing): Holds the JSON data ready for further processing.
5. AWS Lambda Function 2 (Data Transformation): Triggers upon new data in the processing S3 bucket, reads the JSON data, converts it to CSV format, and stores the CSV data in a designated S3 bucket.
6. S3 Bucket (Transformed Data): Stores the final processed data in CSV format.
7. Amazon Redshift: Stores the CSV data from the transformed data S3 bucket for efficient data warehousing and analytics.
8. Amazon QuickSight: Connects to the Redshift data warehouse to visualize and analyze the Zillow data.

## Redshift
### Transformed data is loaded into Amazon Redshift
![Screenshot 2024-06-10 105008](https://github.com/bhavanachitragar/zillow-data-analytics/assets/91766461/4c4cd696-5982-4b7c-9c9a-bb5552eb87eb)
