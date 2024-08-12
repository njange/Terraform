# Terraform VPC Configuration
## Overview
This Terraform project sets up a Virtual Private Cloud (VPC) on [AWS]. The configuration is modular, with each .tf file handling different components of the VPC, such as subnets, route tables, and gateways. This structure ensures that the VPC is scalable, secure, and easy to manage.

## Prerequisites
Before using this Terraform configuration, ensure you have the following installed:

## Terraform v1.0 or later
AWS CLI configured with appropriate credentials (for AWS)
An active account with [AWS]


## Project Structure
The project is organized into multiple .tf files, each responsible for a specific aspect of the VPC:

provider.tf: This file defines the cloud provider (AWS) and the necessary credentials. It ensures that Terraform knows where to deploy the infrastructure.

regionVariable.tf: Contains the variables related to the region where the VPC will be created. It allows you to specify and change the region easily.

vpc.tf: This file contains the main configuration for creating the VPC, including the CIDR block and DNS settings.

vpc_variable.tf: Defines variables related to the VPC, such as the CIDR block and whether DNS support is enabled.

subnets.tf: Manages the creation of public and private subnets within the VPC. It allows for the division of the VPC into multiple subnets for different purposes.

route_table.tf: Configures the route tables for the VPC, defining how traffic is routed between subnets and to external networks.

gateways.tf: Sets up internet gateways or NAT gateways for the VPC, allowing instances in public subnets to communicate with the internet.

nacls.tf: Configures Network ACLs (Access Control Lists) to provide an additional layer of security by controlling inbound and outbound traffic at the subnet level.

terraform.tfstate & terraform.tfstate.backup: These files track the state of the deployed infrastructure, ensuring that Terraform can manage updates and changes over time.
![init](https://github.com/user-attachments/assets/963ea353-baea-4deb-b3c5-5cadb313c69c)
![plan1](https://github.com/user-attachments/assets/507bbfde-1b94-4537-8393-8aadb00cb213)
![plan2](https://github.com/user-attachments/assets/d8f34491-3a86-4c9e-878b-0faf04f28638)
![apply1](https://github.com/user-attachments/assets/c209bc8a-51dd-4cdc-abbc-c5a8a29a0ea6)
![terraformapply2](https://github.com/user-attachments/assets/87d7ad18-56a7-4efe-913d-f89716fed802)
![destroy1](https://github.com/user-attachments/assets/ef4e0206-e855-452b-9fff-490c7d8e1041)
![destroy2](https://github.com/user-attachments/assets/c85caa26-8960-412f-b432-82b669a9a84b)
![destroy3](https://github.com/user-attachments/assets/a02d24bb-88b1-46a1-a328-c174fdd05194)
