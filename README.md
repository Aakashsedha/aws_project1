# AWS Project 1

This project demonstrates an end-to-end data engineering workflow using AWS services. The following AWS services are utilized in this project:
1. IAM (Identity and Access Management)
2. S3 (Simple Storage Service)
3. AWS Glue
4. AWS Athena
5. Amazon QuickSight

![Architecture Diagram](https://github.com/Aakashsedha/aws_project1/assets/92659794/bd56942b-3604-4afa-ac8a-e79371d246e8)

## Project Overview

This repository contains a basic project demonstrating how to build a data pipeline using AWS services. The pipeline enables an IAM user to upload data to an S3 bucket, process and catalog the data using AWS Glue, query the data with AWS Athena, and visualize the results in Amazon QuickSight.

## Architecture Overview

- **IAM User**: Provides secure access to the S3 bucket for uploading data.
- **Amazon S3**: Stores raw data files.
- **AWS Glue**: Catalogs and processes the data stored in S3.
- **AWS Glue Data Catalog**: Stores metadata about the data processed by AWS Glue.
- **AWS Athena**: Allows querying of the data cataloged by AWS Glue.
- **Amazon QuickSight**: Visualizes the query results from Athena.

## Prerequisites

Before you start, make sure you have the following:

- An AWS account with appropriate permissions to create and manage IAM roles, S3 buckets, AWS Glue jobs, AWS Athena queries, and Amazon QuickSight dashboards.
- AWS CLI installed and configured on your local machine.
- Basic knowledge of AWS services.

## Setup Instructions

### Step 1: Create an S3 Bucket

1. Sign in to the AWS Management Console.
2. Open the S3 console at [S3 Console](https://console.aws.amazon.com/s3/).
   ![S3 Console](https://github.com/Aakashsedha/aws_project1/assets/92659794/752ade59-5931-46ec-b8cc-afbf87d4734a)
3. Choose "Create bucket".
4. Follow the prompts to create a new bucket. Note the bucket name as it will be used in later steps.

### Step 2: Configure IAM User

1. Open the IAM console at [IAM Console](https://console.aws.amazon.com/iam/).
2. Create a new IAM user with programmatic access.
3. Attach policies to the user to allow access to S3, AWS Glue, Athena, and QuickSight.

### Step 3: Upload Data to S3

1. Use the AWS CLI or S3 console to upload your data files to the S3 bucket created in Step 1.

### Step 4: Set Up AWS Glue

1. Open the AWS Glue console at [AWS Glue Console](https://console.aws.amazon.com/glue/).
   ![AWS Glue Console](https://github.com/Aakashsedha/aws_project1/assets/92659794/69045ba5-4cd3-4293-b168-fae30518ef26)
2. Create a new Glue Crawler to catalog the data in your S3 bucket.
3. Create a Glue job to process the data if necessary.
4. Run the crawler to populate the Glue Data Catalog.

### Step 5: Query Data with AWS Athena

1. Open the Athena console at [AWS Athena Console](https://console.aws.amazon.com/athena/).
   ![AWS Athena Console](https://github.com/Aakashsedha/aws_project1/assets/92659794/71c3372c-81d5-41e8-9c1d-c095c23a112a)
2. Set up a query result location in the S3 bucket.
3. Use the Athena query editor to run SQL queries on the data cataloged by AWS Glue.

### Step 6: Visualize Data with Amazon QuickSight

1. Open the QuickSight console at [Amazon QuickSight Console](https://quicksight.aws.amazon.com/).
   ![Amazon QuickSight Console](https://github.com/Aakashsedha/aws_project1/assets/92659794/a2ea5b5d-fc82-4d84-bcf4-373f4b00417b)
2. Create a new analysis and connect to the Athena data source.
3. Build visualizations and dashboards based on your Athena queries.



## Contributing

Contributions are welcome! Please fork this repository and submit pull requests for any improvements or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any questions or issues, please open an issue in this repository or contact the project maintainers.
