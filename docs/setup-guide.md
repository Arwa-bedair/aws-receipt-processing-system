# Setup Guide

## 1. Create S3 Bucket
- Create bucket
- Add folder: incoming/

## 2. Create DynamoDB Table
- Table name: receipts
- Partition key: receipt_id
- Sort key: date

## 3. Setup SES
- Verify email

## 4. Create IAM Role
Attach:
- S3 ReadOnly
- Textract FullAccess
- DynamoDB FullAccess
- SES FullAccess
- Lambda Basic Execution

## 5. Create Lambda
- Runtime: Python 11
- Attach role
- Add environment variables

## 6. Add S3 Trigger
- Prefix: incoming/

## 7. Test
- Upload receipt
