# Serverless AWS Terraform API for Point Cloud Retrieval with Entwine
This repository contains infrastructure-as-code using Terraform to deploy a serverless API on AWS. Features are simple and minimal: send GeoJSON polygons and recieve bounded point cloud data from the 3DEP database. The repo leverages Entwine to index point cloud data, PDAL for point cloud processing, and AWS Fargate for scalable, serverless execution of PDAL tasks.

The initial motivation for this repo was AI/ML feature extraction at scale, but geospatial developers and researchers looking to leverage cloud computing for point cloud processing might also find it useful. 
