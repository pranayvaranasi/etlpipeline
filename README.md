# 🚀 Build an ETL Pipeline using AWS Lambda, S3, Glue & DynamoDB

## 📌 Introduction

This project demonstrates the design and implementation of a
**serverless ETL (Extract, Transform, Load) pipeline** using core AWS
services including AWS Lambda, Amazon S3, AWS Glue, and Amazon DynamoDB.

The pipeline automatically processes incoming data, transforms it using
AWS Glue, and stores structured results in DynamoDB --- showcasing
modern cloud-native, event-driven architecture patterns.

This project is designed as a **portfolio showcase** to demonstrate
hands-on experience with:

-   Serverless architecture
-   Data engineering workflows
-   Event-driven processing
-   Cloud-native ETL design
-   AWS integration patterns

------------------------------------------------------------------------

## 🏗️ Architecture Overview

### High-Level Flow

1.  Raw data is uploaded to Amazon S3
2.  An event trigger invokes AWS Lambda
3.  Lambda initiates a transformation process
4.  AWS Glue performs data transformation
5.  Transformed data is stored in Amazon DynamoDB

### Architecture Pattern

-   Event-driven
-   Fully serverless
-   Scalable & fault-tolerant
-   Cost-optimized (pay-per-use services)

------------------------------------------------------------------------

## 📚 Table of Contents

-   Introduction
-   Architecture Overview
-   Technologies Used
-   Project Structure
-   Installation
-   Configuration
-   Usage
-   Features
-   Example Workflow
-   Troubleshooting
-   Future Improvements
-   Contributors
-   License

------------------------------------------------------------------------

## 🛠️ Technologies Used

-   AWS Lambda -- Serverless compute
-   Amazon S3 -- Object storage for raw data
-   AWS Glue -- Managed ETL service
-   Amazon DynamoDB -- NoSQL database
-   Python
-   IAM

------------------------------------------------------------------------

## 📁 Project Structure

    Build-an-ETL-Pipeline-using-AWS-Lambda-S3-Glue-AWS-DynamoDB/
    │
    ├── lambda/
    │   └── lambda_function.py
    │
    ├── glue/
    │   └── glue_script.py
    │
    ├── data/
    │   └── sample_data.csv
    │
    ├── requirements.txt
    └── README.md

------------------------------------------------------------------------

## ⚙️ Installation

### Prerequisites

-   AWS Account
-   IAM user with permissions for Lambda, S3, Glue, DynamoDB
-   Python 3.8+

### Steps

1.  Clone the repository
2.  Create an S3 bucket
3.  Create a DynamoDB table
4.  Create IAM roles for Lambda and Glue
5.  Deploy Lambda function and Glue job
6.  Configure S3 event trigger

------------------------------------------------------------------------

## 🔧 Configuration

Update the following variables in the scripts:

### Lambda

-   S3 bucket name
-   Glue job name
-   DynamoDB table name

### Glue Script

-   Input S3 path
-   Output transformation logic
-   DynamoDB connection settings

Ensure IAM roles have appropriate policies attached.

------------------------------------------------------------------------

## ▶️ Usage

1.  Upload a CSV (or structured file) to the configured S3 bucket.
2.  S3 triggers Lambda automatically.
3.  Lambda initiates the Glue job.
4.  Glue transforms the data.
5.  Processed data is inserted into DynamoDB.

------------------------------------------------------------------------

## ✨ Features

-   Fully serverless ETL pipeline
-   Automatic event-driven processing
-   Scalable architecture
-   Managed transformation service
-   No infrastructure provisioning required
-   Real-world data engineering workflow

------------------------------------------------------------------------

## 🔄 Example Workflow

**Input:** Raw CSV file uploaded to S3

**Processing:** - Schema inference - Data cleansing - Transformation
logic - Record formatting

**Output:** Structured records stored in DynamoDB

------------------------------------------------------------------------

## 🛑 Troubleshooting

  ------------------------------------------------------------------------
  Issue           Possible Cause                    Solution
  --------------- --------------------------------- ----------------------
  Lambda not      S3 event not configured           Verify bucket
  triggering                                        notification settings

  Glue job fails  IAM role permissions              Check Glue execution
                                                    role

  No records in   Mapping issue                     Validate
  DynamoDB                                          transformation logic

  Access Denied   Incorrect IAM policies            Review IAM role
  errors                                            attachments
  ------------------------------------------------------------------------

------------------------------------------------------------------------

## 🚀 Future Improvements

-   Add infrastructure-as-code (CloudFormation/Terraform)
-   Add monitoring with CloudWatch dashboards
-   Implement dead-letter queue for failures
-   Add data validation layer
-   CI/CD pipeline integration

------------------------------------------------------------------------

## 👤 Contributors

-   Pranay Varanasi

------------------------------------------------------------------------

## 📄 License

This project is licensed under the MIT License.
