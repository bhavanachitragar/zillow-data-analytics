# Zillow Data Analytics using AWS

![zillow](https://github.com/bhavanachitragar/zillow-data-analytics/assets/91766461/5df89f71-65d6-4345-842a-43dad0aeaa90)

1. Python Script: Extracts data from Zillow in JSON format and stores it in an S3 bucket.
2. S3 Bucket (Staging): Stores the initial extracted JSON data.
3. AWS Lambda Function 1 (Data Transfer): Triggers upon new data in the staging S3 bucket and copies the JSON data to a destination S3 bucket.
4. S3 Bucket (Processing): Holds the JSON data ready for further processing.
5. AWS Lambda Function 2 (Data Transformation): Triggers upon new data in the processing S3 bucket, reads the JSON data, converts it to CSV format, and stores the CSV data in a designated S3 bucket.
6. S3 Bucket (Transformed Data): Stores the final processed data in CSV format.
7. Amazon Redshift: Stores the CSV data from the transformed data S3 bucket for efficient data warehousing and analytics.
8. Amazon QuickSight: Connects to the Redshift data warehouse to visualize and analyze the Zillow data.


