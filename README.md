# aws-s3-least-privilege-demo
## Project Overview

This project demonstrates how to securely configure Amazon S3 using the principle of least privilege.

The goal is to:
- Prevent unauthorized access
- Protect against accidental deletion
- Enable encryption by default
- Block public access
- Ensure auditability of operations

---

## Architecture Diagram

![Architecture Diagram](architecture-diagram.png)
This diagram illustrates the least privilege access flow and bucket-level security controls.
- Amazon S3 bucket
- Default encryption: SSE-S3
- Block Public Access: Enabled (All ON)
- IAM user with limited S3 permissions
- Bucket policy restricting unwanted actions
- Versioning enabled for recovery

---

## Security Design

### 1. Encryption
Server-side encryption (SSE-S3) is enabled to protect data at rest.

### 2. Public Access Blocking
All public access is blocked at bucket level.

### 3. Least Privilege IAM
IAM user is granted only the minimum required S3 actions.

### 4. Deletion Protection
Versioning is enabled to recover accidentally deleted objects.

---

## Why This Matters

Social welfare organizations handle sensitive personal data.
This design reduces:
- Data leakage risk
- Accidental deletion risk
- Unauthorized access
- Operational mistakes

---

## Author

Kenta Ino  
AWS Certified  
Focus: Cloud Security for Social Welfare Organizations
---

## Improvement Plan

Future enhancements:
- Implement CloudTrail for audit logging
- Add AWS Config rules for compliance monitoring
- Introduce S3 Object Lock for stronger deletion protection
- Automate setup using Infrastructure as Code (Terraform / CloudFormation)

---

## Business Impact

This design can help social welfare organizations:

- Reduce operational risk
- Improve compliance posture
- Increase trust with stakeholders
- Prevent costly security incidents
