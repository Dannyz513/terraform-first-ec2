# Terraform First EC2 Project

A simple Terraform configuration that provisions a single EC2 instance on AWS, demonstrating core Terraform workflow: providers, data sources, variables, and outputs.

## What it does
- Looks up the latest Amazon Linux 2023 AMI dynamically
- Launches a t2.micro EC2 instance
- Outputs the instance ID and public IP after creation

## Usage
\`\`\`bash
terraform init
terraform plan
terraform apply
\`\`\`

Tear down with `terraform destroy` when done.

## Tech
- Terraform
- AWS (EC2)