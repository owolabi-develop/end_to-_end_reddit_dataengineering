
##  End to end reddit data engineering project

The pipeline is designed to:

1. Extract data from Reddit using its API.
2. Store the raw data into an landing zone S3 bucket from Airflow.
3. tigger lambda function to copy the data from landing zone to a rawdata bucket
4. Transform the data using AWS Glue and Amazon Athena.
5. Load the transformed data into Amazon Redshift for analytics.

## Architecture

<img width="4285" alt="project_sample_6" src="https://github.com/owolabi-develop/end_to-_end_reddit_dataengineering/assets/94055941/111cafd2-5047-4e98-b34d-531d5b9cc36c">

1. **Reddit API**: Source of the data.
2. **Apache Airflow** : Orchestrates the ETL process and manages task distribution.
3. **PostgreSQL**: Temporary storage and metadata management.
4. **Amazon S3**: landing zone and Raw data storage.
5. **lambda function** tigger to copy data to rawbucket
6. **AWS Glue**: Data cataloging and ETL jobs.
7. **Amazon Athena**: SQL-based data transformation.
8. **Amazon Redshift**: Data warehousing and analytics.
