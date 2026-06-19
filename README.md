# Encrypting DynamoDB with AWS KMS

## Overview
This project demonstrates how to secure data stored in Amazon DynamoDB using AWS Key Management Service (AWS KMS).
A Customer Managed Key (CMK) was created and attached to a DynamoDB table to provide encryption at rest.
IAM permissions were then tested using a dedicated IAM user to validate access control and data protection.
The project demonstrates how AWS KMS, DynamoDB, and IAM work together to protect sensitive data.

## Architecture Diagram

![Architecture Diagram](image/Diagram.png)

## Service Used

- AWS KMS ( Key Management Service )
- DynamoDB
- IAM ( Identity Access Management )

## Objectives

- Create a Customer Managed KMS Key
- Encrypt a DynamoDB table using AWS KMS
- Store and retrieve data securely
- Test IAM user access permissions
- Validate encryption and access controls

## Implementation Steps

1. Create encryption keys with AWS KMS
2. Encrypt a DynamoDB database with a KMS key.
3. Add and retrieve data from database to test our encryption.
4. Create IAM user and test accessing the data.
5. Verify access control using an IAM test user.

## KMS Key

A Customer Managed Key (CMK) was created in AWS KMS to provide encryption for the DynamoDB table.
This key allows organizations to manage encryption settings and access permissions more securely.
![KMS Key](image/KMS-Key.png)

## DynamoDB Encryption

The DynamoDB table was configured to use the Customer Managed KMS Key for encryption at rest.
This ensures that all stored data is automatically encrypted and protected by AWS KMS.
![DynamoDB Encryption](image/DynamoDB-Encryption.png)

## DynamoDB Item
![DynamoDB Item](image/DynamoDB-Item.png)

## IAM Test User

A dedicated IAM test-user1 was created to validate access permissions against the encrypted DynamoDB table.
![IAM Test User](image/IAM-Test-User.png)

## Validation

An IAM test user without the required KMS permissions attempted to access the encrypted DynamoDB table.
The request was denied, confirming that AWS KMS and IAM policies were correctly enforcing access control.
![Validation](image/Validation.png)

## Lesson Learned

✔ Created and managed encryption keys using AWS KMS
✔ Encrypted a DynamoDB table with a Customer Managed Key
✔ Added and stored data securely in an encrypted table
✔ Validated encryption controls using an IAM test user
✔ Learned how KMS, DynamoDB, and IAM work together to protect data

## Skills Demonstrated

- AWS KMS
- Amazon DynamoDB
- IAM User Management
- Encryption at Rest
- Access Control Validation
- Cloud Security Fundamentals
