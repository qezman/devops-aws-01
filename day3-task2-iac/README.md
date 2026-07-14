# Day 3 - Task 2: Infrastructure as Code (Terraform)

## Objective

Create Terraform configurations to provision an S3 bucket and a
DynamoDB table safely.

## Resources

- S3 bucket: devops-intern-bucket-<random-suffix> - versioning enabled, public access fully blocked
- DynamoDB table: devops-intern-table - on-demand (PAY_PER_REQUEST) billing

## Commands

```bash
terraform init
terraform plan
terraform apply
```

## Verification

```bash
terraform state list
aws dynamodb list-tables
aws s3 ls | grep "devops-intern"
```

Confirmed live via CLI and AWS Console.

## Screenshots

See `/screenshots` folder.

## Key Takeaway

Safe-by-default IaC (versioning, blocked public access, on-demand
billing) adds real protection with minimal extra code.