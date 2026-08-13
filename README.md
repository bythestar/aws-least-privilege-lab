# AWS Least Privilege Lab

Hands-on project demonstrating the principle of least privilege using three IAM users with different permission levels.

## Users Created

| User | Policies Attached | Access Level |
|------|-------------------|--------------|
| `admin-test` | AdministratorAccess | Full admin |
| `developer-test` | AmazonEC2FullAccess + AmazonS3FullAccess | Limited (EC2 + S3 only) |
| `readonly-test` | ReadOnlyAccess | View only |

## Test Results

### readonly-test
- Can view resources
- Cannot create or modify resources
- Expected behavior

### developer-test
- Can manage EC2 and S3
- **Cannot** manage IAM (permission denied)
- Expected behavior (least privilege working)

### admin-test
- Full access (not fully tested in this lab)

## What this demonstrates
- **Least Privilege**: each user only has the permissions required for their role
- **Defense in Depth**: limiting IAM access reduces risk even if a user account is compromised
- Practical IAM skills: creating users, attaching policies, and testing access

## Skills practiced
- IAM users and policies
- Least privilege design
- Permission testing
- Security documentation
