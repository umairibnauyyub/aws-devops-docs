# AWS Transfer Family SFTP Setup

## 📌 Overview
Configured AWS Transfer Family with SFTP for secure file uploads integrated with IAM, CloudWatch logs, and home directory S3 mapping.

## 🛠️ Configuration Steps
1. Created a Transfer Family server (SFTP protocol).
2. Enabled logging to CloudWatch.
3. Created IAM role with S3 access.
4. Mapped user to S3 bucket `/ftp-prod-bucket/username/`.
5. Attached correct trust policy and added inline role policy.

## 🔐 Security Setup
- VPC and Subnet attached
- Security Group opened for SFTP (port 22)
- Static IP assigned for client-side whitelisting

## 📂 Logging
- CloudWatch LogGroup used: `/aws/transfer/ftp-prod-logs`
- Enabled structured logging via IAM Role

## ✅ Tested Using
- FileZilla (SFTP connection)
- Custom IAM users

---

**Maintainer**: Umair Khan  
**Date**: May 2025  
**Project**: PCI DSS Compliance  
