# Modular-AWS-Infrastructure-with-Terraform

 A modular Terraform project to provision AWS resources such as VPC, Subnet, and EC2 instances. By organizing the infrastructure into reusable modules!

# Project Folder Structure:

terraform-project/ │ ├── modules/ │ ├── vpc/ # The VPC Module is responsible for creating a Virtual Private Cloud (VPC) in AWS. │ ├── subnet/ # The Subnet Module is responsible for creating a subnet inside the VPC. It will associate the subnet with the VPC ID provided. │ └── ec2/ # The EC2 Module launches an EC2 instance in the provided subnet, with specified instance type and AMI ID. │ ├── main/ # Root module that integrates all child modules │ ├── main.tf # This is the entry point for your configuration. Here, the modules are called and linked together to create the entire infrastructure. │ ├── variables.tf # Defines the input variables that can be customized. │ ├── outputs.tf # This file declares the outputs from the root module. It will show the VPC ID, Subnet ID, and EC2 details once Terraform finishes applying the configuration. │ ├── provider.tf # Sets up the AWS provider to connect to your AWS account and define the region for resources. │ └── terraform.tfvars # Contains the actual values for variables.
