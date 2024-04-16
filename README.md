# Serverless AWS Terraform API for Point Cloud Retrieval with Entwine
This repository contains infrastructure-as-code using Terraform to deploy a serverless API on AWS. Features are simple and minimal: send GeoJSON polygons and recieve bounded point cloud data from the 3DEP database. The repo leverages Entwine to index point cloud data, PDAL for point cloud processing, and AWS Fargate for scalable, serverless execution of PDAL tasks.

The initial motivation for this repo was AI/ML feature extraction at scale, but geospatial developers and researchers looking to leverage cloud computing for point cloud processing might also find it useful. 

## Overview

The API serves as an interface to post GeoJSON polygons and retrieve point cloud data processed from the 3DEP database. AWS Fargate is utilized to run containerized PDAL operations, ensuring on-demand processing that scales automatically with the load. Entwine is employed to organize large point cloud datasets into a readily accessible format, and Terraform automates the creation and management of the necessary AWS resources.

![serverless-aws-terraform-entwine-api](https://github.com/skogsmonster/serverless-aws-terraform-entwine-api/assets/137440075/f91d2604-6d54-4cd7-91e4-3d4fd3a0fa67)

## Contributing

See `dev` branch for latest.

