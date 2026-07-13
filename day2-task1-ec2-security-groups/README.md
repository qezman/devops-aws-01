# Day 2 - Task 1: EC2 & Security Groups

## Objective
Provision an EC2 instance with custom security group rules and an SSH key pair.

## Setup
- Key pair: devops-intern-key (RSA, .pem)
- Security group: devops-intern-sg - SSH (22) restricted to My IP only
- Instance: devops-intern-ec2, Amazon Linux 2023, t3.micro (free tier)
- VPC/Subnet: devops-intern-vpc / public-subnet-1 (from Day 1)

## Verification
Connected successfully via:
ssh -i devops-intern-key.pem ec2-user@<public-ip>

## Screenshots
See `/screenshots` folder.

## Key Takeaway
Restricting SSH ingress to a known IP instead of 0.0.0.0/0 removes the
instance from constant internet-wide SSH scanning - basic but important
hardening.