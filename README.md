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


## Documentation

Detailed implementation steps and screenshots are available in the attached project documentation.
