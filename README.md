# AWS Learning & CLI Examples

This repository contains my hands-on AWS CLI practice, examples, scripts, and notes while preparing for the **AWS Solutions Architect Associate (SAA-C03)** exam.

The repo runs inside **Gitpod/ONA cloud workspaces**, which simulate a Linux environment even if the local machine is macOS.

---

## 🚀 Features

- AWS CLI installed automatically via `.gitpod.yml`
- Never commits temporary installer files (`awscliv2.zip`, `aws/`)
- Organized examples for IAM, S3, EC2, STS, DynamoDB, Lambda, and more
- Script folder for automation
- Clean environment every time the workspace starts

---

## ⚙️ Gitpod/ONA Auto-Setup

The AWS CLI is installed automatically at workspace startup using the Linux installer:

```yaml
tasks:
  - name: aws-cli
    before: |
      cd /workspaces/${GITPOD_REPO_ROOT##*/}
      curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
      unzip awscliv2.zip
      sudo ./aws/install

      
