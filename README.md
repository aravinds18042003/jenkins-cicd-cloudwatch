# Jenkins CI/CD Pipeline with CloudWatch Monitoring | EC2, Jenkins, Git, GitHub, CloudWatch, SNS

## Overview
Deployed Jenkins on AWS EC2 to automate build pipelines with GitHub integration, real-time CloudWatch monitoring, and SNS alerting — reducing manual deployment effort by ~80%.

## Architecture
```
GitHub Push → Poll SCM (Jenkins) → Build Pipeline → EC2
                                                      ↓
                                   CloudWatch → SNS Email Alert
```

## Features
- **~80% reduction** in manual deployment effort via automated Jenkins pipelines
- **Auto-triggered builds** — Poll SCM detects GitHub commits and initiates builds within 1 minute
- **CloudWatch CPU alarm** — triggers SNS email alert when CPU exceeds 70% threshold
- **Mean alert response time under 2 minutes** via SNS email notifications
- **Zero open inbound ports** — EC2 locked down using IAM roles and Security Groups

## Tech Stack
| Service | Purpose |
|---|---|
| AWS EC2 | Jenkins server hosting |
| Jenkins | CI/CD automation |
| Git & GitHub | Source code management |
| Poll SCM | Auto-trigger builds on commit |
| AWS CloudWatch | CPU monitoring & alarms |
| AWS SNS | Email alert notifications |
| IAM Roles & Security Groups | Least-privilege access control |

## Project Highlights
- Deployed Jenkins on EC2 and automated build pipelines, reducing manual deployment effort by ~80%
- Configured Poll SCM triggers to detect GitHub commits and initiate builds within 1 minute
- Set up CloudWatch CPU alarm (>70% threshold) with SNS email alerts — mean alert response time under 2 minutes
- Locked down EC2 access using IAM roles and Security Groups with zero open inbound ports

## CI/CD Pipeline Flow
```
Developer pushes code → GitHub
→ Jenkins Poll SCM detects commit (within 1 min)
→ Build triggered automatically
→ Pipeline executes → Deploy ✅
→ CloudWatch monitors EC2 CPU
→ CPU > 70% → SNS Email Alert 📧
```

## Security
- IAM roles assigned to EC2 — no hardcoded credentials
- Security Groups configured with zero open inbound ports
- Least-privilege principle enforced throughout
