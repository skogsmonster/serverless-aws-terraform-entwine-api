# Serverless AWS Terraform API for Point Cloud Retrieval with Entwine
This repository aims to provide a robust and straightforward way to access bounded 3DEP point cloud data using serverless technologies, bringing geospatial analysis capabilities to a broader audience with ease.

Use the Terraform configurations and necessary code to deploy a serverless API on AWS, leveraging Entwine for processing 3DEP point cloud data. The API allows users to `POST` GeoJSON polygons and receive corresponding point cloud data, enabling users to seamlessly interact with large geospatial datasets in an efficient and scalable manner.

## Features

- **Serverless Architecture**: Built on AWS, the infrastructure scales automatically with usage, ensuring cost-effective and performant operation.
- **Terraform Automation**: The entire AWS infrastructure is defined as code using Terraform, allowing for reproducible deployments and easy versioning.
- **GeoJSON Input**: Users can submit GeoJSON polygons via a `POST` request, specifying the area for which they require point cloud data.
- **Entwine Point Cloud Processing**: Integrates with Entwine to index and tile the 3DEP LiDAR data, enabling efficient querying and retrieval of point cloud data.
- **AWS Lambda**: Processes the `POST` request and manages the interaction with Entwine and the retrieval of point cloud data.
- **Amazon S3**: Serves as the storage solution for both the raw 3DEP data and the processed Entwine point cloud data.
- **API Gateway**: Provides a RESTful endpoint for client interactions, handling `POST` requests and returning the point cloud data.
- **IAM Security**: Ensures that permissions and access are tightly controlled, granting only necessary privileges to each component within the architecture.

## Getting Started

To utilize this repository:

1. Clone the repo to your local machine.
2. Ensure you have Terraform and AWS CLI installed and configured.
3. Navigate to the Terraform directory and initialize the Terraform environment with `terraform init`.
4. Apply the Terraform configurations with `terraform apply`.

## Usage

- Send a `POST` request to the deployed API endpoint with your GeoJSON payload.
- The API will return a link to the processed point cloud data stored in S3 or stream it directly to your client, depending on your preference and setup.

## Contributing

We welcome contributions and suggestions! Please fork the repository and submit a pull request with your proposed changes or enhancements. Be sure to follow the project's code style and include tests for any new features or fixes.

## License

This project is released under the [MIT License](LICENSE).


