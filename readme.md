# Automating creation of IAM Resources LAB

## Overview

In this lab, students learn how to create IAM users and other resources via AWS CloudFormation and assign relevant permission using IAM User Group permissions.

## Task 1: Create an IAM User and Attach an S3 Policy

Create a CloudFormation template that generate the ff resources:

- One-Time Password: Auto-generated and stored in Secrets Manager to be used for all users

- S3 User Group with read access to S3
- Two IAM users with console access, (ec2-user assigned to EC2 Group, s3-user assigned to S3 Group)

  - User must be assigned temporary password created above
  - User must have an email attribute stored in Parameter store

- EventBridge Rule to detect new user creation, triggering a Lambda function that retrieves the user email and temporary password and log the email and the temporary password.

## Screenshots

### Infrastructure Composer

<img width="958" alt="Image" src="https://github.com/user-attachments/assets/85dc1b66-36d4-46de-a7d0-2420c1e11546" />

## CloudWatch Logs

<img width="959" alt="Image" src="https://github.com/user-attachments/assets/f40be8f5-7787-4116-8868-93a9bb803a29" />

<img width="959" alt="Image" src="https://github.com/user-attachments/assets/ef0aaa25-f870-4bc8-ab4e-106eee5fa12a" />

<img width="959" alt="Image" src="https://github.com/user-attachments/assets/2cb3ed33-d033-4170-81a8-4068576d862a" />
