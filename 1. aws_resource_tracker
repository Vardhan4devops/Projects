# vim aws_resource_tracker.sh --file name
#!/bin/bash
# Author: Vardhan
# Date: 12th March, 2024
# Version: v1
# This script reoports AWS resource usage
###########################################
# Resources:
#EC2
#S3
#Lambda
#IAM users

# Reference link: https://docs.aws.amazon.com/cli/latest/

# list s3 buckets
echo "List of S3 buckets"
aws s3 ls >> ResourceTracker

#list aws instances
echo "List of Instances"
aws ec2 describe-instances | jq '.Reservations[].Instances[].InstanceId' >> ResourceTracker

#list aws lambda functions
echo "List of Lambda functions"
aws lambda list-functions >> ResourceTracker

# list IAM users
echo "List of IAM users"
aws iam list-users >> ResourceTracker

##################################################
chmod 777 aws_resource_tracker.sh
./aws_resource_tracker.sh
