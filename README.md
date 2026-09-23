# AWS Automation Practice

Small DevOps/cloud automation project created to practice AWS operations from the command line and Python.

## What it includes

### EC2 management with Python
`gestionar_ec2.py` uses Boto3 to:

- List EC2 instances.
- Display instance ID, type, state and Name tag when available.
- Start an EC2 instance by ID.
- Stop an EC2 instance by ID.

The script relies on the standard AWS credential chain configured outside the repository. No AWS access keys should be stored in the code.

### S3 backup automation with Bash
`backup_s3.sh`:

1. Receives a local directory and S3 bucket as arguments.
2. Creates a timestamped `.tar.gz` archive.
3. Uploads the archive with the AWS CLI.
4. Writes a local execution log.
5. Removes the temporary archive after upload.

## Technologies

- Python
- Boto3
- Bash
- AWS CLI
- Amazon EC2
- Amazon S3
- Linux command line

## Security notes

AWS credentials must be configured through the AWS CLI, IAM roles, or another supported credential provider. Never hardcode access keys in source code.
