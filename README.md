# Jenkins CI/CD Pipeline with CloudWatch Monitoring

## Overview
End-to-end CI/CD pipeline using Jenkins on AWS EC2 
with CloudWatch monitoring and SNS alerting.

## Architecture
GitHub → Jenkins (EC2) → Build → Deploy
EC2 → CloudWatch → SNS Alert → Email

## Tools & Services
- Jenkins — CI/CD pipeline
- AWS EC2 — Jenkins hosting
- GitHub — Source control + webhook
- CloudWatch — CPU monitoring
- SNS — Email notifications
- Bash — Automation

## Key Features
- Automated build triggers via Poll SCM
- CPU threshold alarm (>70%)
- Real-time email alerts via SNS
- IAM roles for secure access

## Skills
Jenkins · AWS EC2 · CloudWatch · SNS · CI/CD · DevOps
