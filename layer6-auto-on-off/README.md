# Ec2 On/Off Lambda Function

This layer simply runs a Cloudformation script which creates a Lambda function to atomically startup/shutdown EC2 instances at scheduled times

# Using this template 

## Instructions

1.	Navigate to the AWS CloudFormation service in your preferred AWS region.
2.	Create Stack.
3.	Choose template and upload the layer6-auto-on-off/ec2-auto-on0ff.yml template.
4.	Complete the required parameters. See Inputs section below for more descriptive parameter definitions.
5.	On successful stack creation, the lambda function for ec2 auto on off will have been created


### Inputs

| Parameter | Description |
|-----------|-------------|
| Custom TagName | This has a default of “scheduler:ec2-startstop”. You have already added this tag to your EC2 instance, therefore do not change it. |
| Schedule | How often AWS will check to see if there has been a change to the schedule. We currently have this set to 30 minutes.. | 
| DefaultStartTime | When you would like EC2 instances to startup. | 
| DefaultStopTime | When you would like EC2 instances to shutdown. | 
| DefaultDaysActive  | Which days the Lambda function should run. | 
| CloudWatchMetrics | This should be set to “Enabled” to create a custom CloudWatch Metric. |
| SendAnonymousData | Choice of if you would like to send anonymous data to AWS |

# CloudFormation

The service uses the AWS CloudFormation service to provision the resource required for the scheduled EC2 On/Off Lambda Function

# User feedback

## Documentation
Documentation will be captured within this README.md.

## Issues
If you have any problems with or questions about this, please raise an issue.

## Contribute
You are invited to contribute new features, fixes, or updates, large or small; we are always thrilled to receive pull requests, and do our best to process them as fast as we can.

We expect you to have forked this repository in Github and modified to meet your project requirements as needed.
