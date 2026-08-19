# 🚀 Terraform First EC2 Instance

A minimal but complete Terraform project that provisions a single EC2 instance on AWS — built to demonstrate core Terraform fundamentals: providers, data sources, variables, and outputs.

![Terraform](https://img.shields.io/badge/Terraform-1.15-623CE4?logo=terraform&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-EC2-FF9900?logo=amazonaws&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-blue)

## Overview

This project provisions an EC2 instance using Infrastructure as Code instead of manual console clicks. It dynamically looks up the latest Amazon Linux 2023 AMI rather than hardcoding one, so the config stays current without edits.

## What This Demonstrates

- Terraform core workflow (`init` → `plan` → `apply` → `destroy`)
- Use of **data sources** to dynamically fetch the latest AMI
- Parameterized configuration with **variables** (region, instance type)
- **Outputs** for retrieving resource attributes after provisioning
- Clean project structure (`main.tf`, `variables.tf`, `outputs.tf`)

## Usage

\`\`\`bash
terraform init
terraform plan
terraform apply
\`\`\`

Retrieve the instance's public IP and ID directly from the output, or via:
\`\`\`bash
terraform output
\`\`\`

Tear down when finished:
\`\`\`bash
terraform destroy
\`\`\`

## Cost

Uses a `t2.micro` instance — covered under the AWS Free Tier (750 hrs/month for new accounts). Outside free tier, costs approximately $0.0116/hour.

## Tech Stack

- **Terraform** 1.15
- **AWS** (EC2)