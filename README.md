Spotify Data Pipeline Project

**Overview**
This project demonstrates a data pipeline for extracting, transforming, and loading Spotify's top 50 songs data into Snowflake for analysis. 
The pipeline uses AWS services including Lambda, S3, and CloudWatch, alongside Snowflake for data warehousing.

**Data Extraction**
The data extraction process is handled by an AWS Lambda function which:
Logs into the Spotify API using the provided Client ID and Secret Key.
Extracts the top 50 songs data in JSON format.
Stores the extracted data into the S3 raw folder.

**Data Transformation**
Once the data is available in the raw folder, another Lambda function:
Extracts album, song, and artist information from the JSON data.
Transforms and stores the data in CSV format in the S3 transformed folder.
Data Loading

**Analysis**
The transformed data is then:
Loaded into Snowflake tables using Snowpipe.
Analyzed for insights and reporting.

**Technologies/Languages/Tools**: Python, PostgreSQL, AWS(S3, CloudWatch, Lambda), Snow-pipe, Snowflake

Reference: Darshil Parmar
