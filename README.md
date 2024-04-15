# Serverless AWS Terraform API for Point Cloud Retrieval with Entwine
This repository contains infrastructure-as-code using Terraform to deploy a serverless API on AWS. Features are simple and minimal: send GeoJSON polygons and recieve bounded point cloud data from the 3DEP database. The repo leverages Entwine to index point cloud data, PDAL for point cloud processing, and AWS Fargate for scalable, serverless execution of PDAL tasks.

I created this repo for AI/ML feature extraction at scale, but geospatial developers and researchers looking to leverage cloud computing for point cloud processing might also find it useful. 

## Overview

The API serves as an interface to post GeoJSON polygons and retrieve point cloud data processed from the 3DEP database. AWS Fargate is utilized to run containerized PDAL operations, ensuring on-demand processing that scales automatically with the load. Entwine is employed to organize large point cloud datasets into a readily accessible format, and Terraform automates the creation and management of the necessary AWS resources.

![serverless-aws-terraform-entwine-api](https://github.com/skogsmonster/serverless-aws-terraform-entwine-api/assets/137440075/f91d2604-6d54-4cd7-91e4-3d4fd3a0fa67)

## Features

- **Serverless Infrastructure**: Automated scaling and management of the infrastructure to ensure cost-effective and performant operation.
- **Terraform Automation**: Streamlined deployment with Terraform to manage AWS resources as code, providing consistency and ease of replication.
- **GeoJSON to Point Cloud**: Users can POST GeoJSON data to specify the area for which point cloud data is needed.
- **Entwine Indexing**: Efficient querying and handling of massive point cloud datasets using Entwine for data indexing.
- **PDAL Processing**: Advanced point cloud processing with PDAL, executed in AWS Fargate for handling compute-intensive tasks.
- **API Gateway & AWS Lambda**: A RESTful API interface managed by API Gateway, with backend processing powered by AWS Lambda functions.
- **Amazon S3 Storage**: Integration with S3 for storing raw and processed point cloud data, ensuring durability and security.
- **IAM Roles and Policies**: Fine-grained access control using AWS IAM to maintain security best practices.

## Architecture

The system is comprised of the following components:
- API Gateway to receive GeoJSON via POST requests.
- Lambda functions to trigger Fargate tasks running PDAL for point cloud cropping based on the GeoJSON input.
- Fargate tasks that process the point cloud data using PDAL and store the results in an S3 bucket.
- An S3 bucket to hold the incoming GeoJSON, intermediate files, and the final cropped point cloud data.
- IAM roles and policies to securely orchestrate access between services.

## Getting Started

To deploy the API:

1. Clone the repository.
2. Install Terraform and configure AWS CLI with appropriate credentials.
3. Navigate to the `terraform` directory and initialize Terraform with `terraform init`.
4. Apply the configuration using `terraform apply`.

## Usage

- Send a `POST` request to the deployed API endpoint with your GeoJSON payload.
- The API will return a link to the processed point cloud data stored in S3 or stream it directly to your client, depending on your preference and setup.

## Contributing

We welcome contributions and suggestions! Please fork the repository and submit a pull request with your proposed changes or enhancements. Be sure to follow the project's code style and include tests for any new features or fixes.

## License

This project is released under the [MIT License](LICENSE).


