# Serverless-Architecture

## Overall Serverless Workflow

```text
                +-------------------+
                |    AWS Lambda     |
                |   Python + Boto3  |
                +----------+--------+
                           |
        -----------------------------------------
        |                  |                    |
        v                  v                    v
+---------------+  +---------------+  +----------------+
| EC2 Instances |  |  S3 Buckets   |  |  EBS Volumes   |
+---------------+  +---------------+  +----------------+
        |                  |                    |
        -----------------------------------------
                           |
                           v
                +-------------------+
                | CloudWatch Logs   |
                +-------------------+
```


## Features

- Automated EC2 start/stop using Lambda
- Automated S3 cleanup
- S3 encryption monitoring
- Automated EBS snapshot management
- CloudWatch logging integration
- Serverless AWS architecture


## Technologies Used

- AWS Lambda
- Amazon EC2
- Amazon S3
- Amazon EBS
- IAM
- CloudWatch
- Boto3
- Python 3.x

1. Automated EC2 Instance Management
Automated the starting and stopping of EC2 instances based on resource tags.

Features:

Detect instances tagged with Action=Auto-Stop
Stop matching instances
Detect instances tagged with Action=Auto-Start
Start matching instances
Generate execution logs in CloudWatch
2. Automated S3 Bucket Cleanup
Automated deletion of files older than the configured retention period.

Features:

List S3 objects
Check object age
Delete outdated objects
Log cleanup operations
3. Monitor S3 Bucket Encryption Status
Implemented a Lambda function to monitor S3 bucket encryption settings.

Features:

Scan all S3 buckets
Check server-side encryption status
Report encryption configuration through CloudWatch logs
Note: AWS automatically encrypts all new object uploads to Amazon S3 using SSE-S3 by default. This assignment demonstrates how bucket encryption settings can be monitored and validated programmatically.

4. Automatic EBS Snapshot and Cleanup
Automated EBS snapshot creation and lifecycle management.

Features:

Create snapshots for specified EBS volumes
Store snapshot details
Remove outdated snapshots
Log snapshot operations


## Documentation

Detailed implementation steps and screenshots are available in the attached project documentation.
