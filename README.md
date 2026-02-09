# Jobbernaut Infrastructure (Infra)

This repository contains the **Terraform** configuration for the entire Jobbernaut Ecosystem. It manages the lifecycle of all AWS resources, networking, and security policies.

## 🏗 Logical Components Managed
* **Jobbernaut ReDirector:** The AWS HTTP API Gateway acting as the entry point.
* **Jobbernaut Director:** The AWS Step Functions State Machine that orchestrates the async tailoring workflow.
* **Jobbernaut Warehouse:** The S3 Buckets for storing raw job descriptions, generated PDFs, and Terraform state.
* **Jobbernaut Tabs Database:** The DynamoDB table (Single-Table Design) storing User and Job state.

## 🛠 Tech Stack
* **Terraform (HCL):** Infrastructure as Code.
* **AWS IAM:** OIDC Provider for GitHub Actions (Keyless authentication).
* **AWS SSM:** Parameter Store for managing environment variables across services.

## 🚀 Deployment
Merging to `main` triggers the `terraform apply` workflow via GitHub Actions.
