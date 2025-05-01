# Modular-AWS-Infrastructure-with-Terraform

 A modular Terraform project to provision AWS resources such as VPC, Subnet, and EC2 instances. By organizing the infrastructure into reusable modules!

# Project Folder Structure:

terraform-project/
├── modules/
│   ├── vpc/        # Module for creating a VPC
│   ├── subnet/     # Module for creating a subnet inside the VPC
│   └── ec2/        # Module for launching an EC2 instance
├── main/
│   ├── main.tf     # Root module that calls the VPC, Subnet, EC2 modules
│   ├── variables.tf # Defines the variables used in the root configuration
│   ├── outputs.tf  # Outputs information such as VPC ID, Subnet ID, etc.
│   ├── provider.tf # AWS provider and region configuration
│   └── terraform.tfvars # Variable values (like CIDR blocks, instance types, etc.)
