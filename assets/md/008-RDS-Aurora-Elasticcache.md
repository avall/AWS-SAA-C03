* [Return to table of contents](../../README.md)
# RDS (Relational Database Service)
## Amazon RDS Introduction
## RDS versus deploying DB on EC2
## RDS – Storage Auto Scaling
## RDS Read Replicas
### For read scalability
### Use cases
### Network cost
## RDS Backups
- Automated backups:
  - Daily full backup of the database (during the backup window)
  - Transaction logs are backed-up by RDS every 5 minutes
  - => ability to restore to any point in time (from oldest backup to 5 minutes ago) 
  - 1 to 35 days of retention, set 0 to disable automated backups
- Manual DB Snapshots
  - Manually triggered by the user
  - Retention of backup for as long as you want
- Trick: in a stopped RDS database, you will still pay for storage. If you plan on stopping it for a long time, you should snapshot & restore instead

## RDS Restore options
- Restoring a RDS backup or a snapshot creates a new database.
- Restoring MySQL RDS database from S3 
  - Create a backup of your on-premises database
  - Store it on Amazon S3 (object storage)
  - Restore the backup file onto a new RDS instance running MySQL

## RDS Multi AZ (Disaster Recovery)
## RDS From Single-AZ to Multi-AZ
## RDS Custom
## RDS Security
- At-rest encryption:
  - Database master & replicas encryption using AWS KMS – must be defined as launch time 
  - If the master is not encrypted, the read replicas cannot be encrypted
  - To encrypt an un-encrypted database, go through a DB snapshot & restore as encrypted
- In-flight encryption: TLS-ready by default, use the AWS TLS root certificates client-side
- IAM Authentication: IAM roles to connect to your database (instead of username/pw) 
- Security Groups: Control Network access to your RDS DB.
- No SSH available except on RDS Custom
- Audit Logs can be enabled and sent to CloudWatch Logs for longer retention

## RDS Proxy


# Amazon Aurora
## Introduction
## High Availability and Read Scaling
## DB Cluster
## Features
## Replicas - Auto Scaling
## Custom Endpoints
## Serverless
## Global Aurora
## Machine Learning
## Backups
- Automated backups
  - 1 to 35 days (cannot be disabled)
  - point-in-time recovery in that timeframe
- Manual DB Snapshots
  - Manually triggered by the user
  - Retention of backup for as long as you want
## Aurora Restore options
- Restoring an Aurora backup or a snapshot creates a new database.
- Restoring MySQL Aurora cluster from S3
  - Create a backup of your on-premises database using Percona XtraBackup
  - Store the backup file on Amazon S3
  - Restore the backup file onto a new Aurora cluster running MySQL

## Database Cloning
## Aurora Security
- At-rest encryption:
    - Database master & replicas encryption using AWS KMS – must be defined as launch time
    - If the master is not encrypted, the read replicas cannot be encrypted
    - To encrypt an un-encrypted database, go through a DB snapshot & restore as encrypted
- In-flight encryption: TLS-ready by default, use the AWS TLS root certificates client-side
- IAM Authentication: IAM roles to connect to your database (instead of username/pw)
- Security Groups: Control Network access to your Aurora DB
- Audit Logs can be enabled and sent to CloudWatch Logs for longer retention

# Amazon ElastiCache
## Introduction
## Solution Architecture
### DB Cache
### User Session Store
## Redis vs Memcached
## Cache Security
## Patterns
## Redis Use Case

