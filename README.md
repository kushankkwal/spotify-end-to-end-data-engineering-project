# Spotify End-to-End Data Engineering Project 

### Introduction 
In this project, we will build an ETL (Extract, Transform, Load) pipeline using the Spotify API on AWS. 
The pipeline will retrieve data from the Spotify API, transform it to the desired format, and then load it to the AWS Data Store.

### Architecture Diagram
![Architecture Diagram](https://github.com/kushankkwal/spotify-end-to-end-data-engineering-project/blob/main/Spotify_Data_Pipeline%20.jpeg)

### About Dataset/API
This API contains information about music artists, albums, and songs - [Spotify API](https://developer.spotify.com/documentation/web-api)

### Services Used
1. **S3 (Simple, Storage, Service):** Amazon S3 (Simple Storage Service) is a highly scalable object storage service that can store and retrieve any amount of data from anywhere on the web. It is commonly used to store and distribute large media files, data backups, and static website files.
2. **AWS Lambda:** AWS Lambda is a serverless computing service that lets you run your code without managing servers. You can use lambda to run the code in response to events like changes in S3, DynamoDB, or other Amazon Web Services.
3. **CloudWatch:** Amazon CloudWatch is a monitoring service for AWS resources and the applications you run on them. You can use ClooudWatch to collect and track metrics, collect and monitor log files, and set alarms.
4. **Glue Crawler:** AWS Glue Crawler is a fully managed service that automatically crawls your data sources, identifies the data format, and infers schemas to create an AWS Glue Data Catalog.
5. **Data Catalog:** AWS Glue Data Catalog is a fully managed service that automatically crawls your data sources, identifies the data formats, and infers schemas to create an AWS Glue Data Catalog with other Amazon Web Services, such as Athena.
6. **Amazon Athena:** Amazon Athena is an Interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL. You can use Athena to analyze data in your Gllue Catalog or other S3 Buckets.

### Install Packages
```
pip install pandas
pip install numpy
pip install spotipy
```

### Project Execution Flow
Extract Data from API -> Lambda Trigger (Every 1 Hour) -> Run extract Code -> Store Raw Data -> Trigger Transformation Function -> Transform Data and Load it -> Query using Athena.
