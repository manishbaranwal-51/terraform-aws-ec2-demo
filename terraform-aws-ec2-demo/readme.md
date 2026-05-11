# Terraform AWS EC2 Deployment Demo

## Project Overview

This project demonstrates Infrastructure as Code (IaC) using Terraform to provision and manage an AWS EC2 instance. The objective of this project is to automate cloud infrastructure deployment using Terraform and AWS CLI.

This repository showcases a complete Terraform deployment lifecycle including provider initialization, AWS authentication, infrastructure provisioning, and infrastructure management.

---

## Technologies Used

- Terraform
- AWS CLI
- AWS EC2
- Ubuntu Linux
- Git & GitHub
- Visual Studio Code

---

## Project Architecture

```text
Terraform Configuration
        ↓
Terraform CLI
        ↓
AWS Provider
        ↓
AWS EC2 Instance
```

---

## Features

- Configure AWS Provider
- Deploy EC2 Instance using Terraform
- Infrastructure as Code (IaC)
- AWS CLI Authentication
- Terraform State Management
- Reusable Terraform Configuration
- Automated Infrastructure Provisioning

---

## Project Structure

```text
terraform-aws-ec2-demo/
│
├── provider.tf
├── main.tf
├── variables.tf
├── outputs.tf
├── terraform.tfvars
├── .gitignore
├── README.md
└── screenshots/
    ├── terraform-init.png
    ├── terraform-apply.png
    ├── ec2-running.png
    └── terraform-destroy.png
```

---

## Prerequisites

Before running this project, ensure the following tools are installed:

- Terraform
- AWS CLI
- Git
- Visual Studio Code

---

## AWS CLI Configuration

Configure AWS credentials using:

```bash
aws configure
```

Provide:
- AWS Access Key ID
- AWS Secret Access Key
- AWS Region
- Output Format

---

## Terraform Workflow

### 1. Initialize Terraform

```bash
terraform init
```

### 2. Validate Configuration

```bash
terraform validate
```

### 3. Preview Infrastructure Changes

```bash
terraform plan
```

### 4. Deploy Infrastructure

```bash
terraform apply
```

### 5. Destroy Infrastructure

```bash
terraform destroy
```

---

## Terraform Configuration Example

### Provider Configuration

```hcl
provider "aws" {
  region = "ap-south-1"
}
```

### EC2 Resource Configuration

```hcl
resource "aws_instance" "manish_ec2" {
  ami           = "ami-07a00cf47dbbc844c"
  instance_type = "t3.micro"
  key_name = var.key_name
  vpc_security_group_ids = [var.ecurity_group_id]
  tags = {
    Name = "TerraformDemo-EC2"
  }
}
```

---

## Learning Outcomes

This project helped in understanding:

- Infrastructure as Code (IaC)
- Terraform Providers & Resources
- AWS EC2 Provisioning
- Terraform Workflow
- AWS Authentication using AWS CLI
- State File Management
- Infrastructure Automation

---


## Security Best Practices

- Sensitive files are excluded using `.gitignore`
- AWS credentials are not stored in the repository

---

## Future Enhancements

- Add Security Groups
- Add VPC and Networking
- Use Terraform Variables & Modules
- Configure Remote Backend (S3 + DynamoDB)
- Implement CI/CD using GitHub Actions or Jenkins
- Add Load Balancer & Auto Scaling

---

## Author

Manish Baranwal

Cloud & DevOps Enthusiast | IT Infrastructure Engineer | AWS & Terraform Learner

---

## License

This project is for learning and demonstration purposes.