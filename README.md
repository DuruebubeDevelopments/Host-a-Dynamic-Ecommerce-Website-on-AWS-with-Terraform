https://github.com/DuruebubeDevelopments/Host-a-Dynamic-Ecommerce-Website-on-AWS-with-Terraform/blob/main/1.Terraform-Ecommerce%20(1).jpg?raw=true

# Host-a-Dynamic-Ecommerce-Website-on-AWS-with-Terraform
Deploy a dynamic website on AWS with Terraform
# Host a Dynamic Ecommerce Website on AWS with Terraform

## Introduction
This repository contains the Infrastructure-as-Code (IaC) resources for deploying a high-availability e-commerce platform on AWS. By leveraging Terraform, we orchestrate the creation of a secure, scalable, and resilient architecture that supports an online retail application.

## Architecture
Our architecture ensures optimal security, scalability, and fault tolerance by spreading resources across multiple Availability Zones (AZs) in the AWS US East (N. Virginia) region. Key infrastructure components include:

### VPC Configuration
A custom Virtual Private Cloud (VPC) with public and private subnets in two AZs for network segmentation and control.

### NAT Gateways
Situated in each public subnet to provide secure internet access to instances in private subnets without exposing them to incoming traffic.

### Application Load Balancer (ALB)
Distributes incoming web traffic across multiple EC2 instances within the Auto Scaling group to ensure consistent performance and availability.

### Auto Scaling
Automatically adjusts the number of Amazon EC2 instances based on traffic, keeping the application responsive at all times.

### Amazon RDS
A managed Relational Database Service with a primary instance in one AZ and a standby in another for robust availability and failover support.

### Amazon SNS
A Simple Notification Service topic to alert administrators about scaling events and other significant system incidents.

### Route 53
Manages DNS, directing traffic to the ALB and performing health checks to route users to the best available server.

## Project Setup Instructions
To set up the infrastructure, follow these steps:

1. Install Terraform for infrastructure management.
2. Create and configure a GitHub account for code management.
3. Establish a GitHub repository to store Terraform configurations.
4. Install and configure Git for version control.
5. Generate key pairs and link the public SSH key to GitHub for secure operations.
6. Clone the repository locally to manage Terraform files.
7. Install Visual Studio Code or another code editor of your choice.
8. Install and configure the AWS CLI for interacting with AWS services.
9. Deploy AWS resources using the `main.tf` Terraform configuration.

## Security
Configured security groups strictly adhere to the principle of least privilege:

- Inbound rules allow only essential traffic to each resource.
- Outbound rules are configured to reduce the risk of data leaks.

## Repository Structure
- `main.tf`: Terraform configuration for all AWS resources.
- `variables.tf`: Variable definitions for Terraform configurations.
- `outputs.tf`: Output details post Terraform application.
- `README.md`: Project overview and setup instructions.

## Prerequisites
Before beginning deployment, ensure you have:

- An AWS account with the necessary permissions.
- Terraform installed on your machine.
- The AWS CLI installed and configured.
