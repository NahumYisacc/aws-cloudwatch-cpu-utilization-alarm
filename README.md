# aws-cloudwatch-cpu-alarm-project
Created a CloudWatch CPU utilization alarm that sends notifications when an EC2 instance exceeds a threshold.

# AWS CloudWatch CPU Utilization Alarm

## Project Overview
This project demonstrates how I created a CloudWatch alarm that monitors the CPU utilization of an EC2 instance.  
When the CPU goes above a set threshold, CloudWatch triggers an SNS notification.  
This is a common monitoring task in cloud support and helps ensure systems stay healthy and responsive.

## Architecture
EC2 Instance → CloudWatch Metrics → CloudWatch Alarm → SNS Topic → Email Notification

## Services Used
- Amazon EC2  
- Amazon CloudWatch  
- Amazon SNS  
- IAM  

## What I Did
- Selected an EC2 instance to monitor  
- Created an SNS topic and subscribed my email  
- Created a CloudWatch alarm for CPUUtilization  
- Set a threshold (ex: > 70% CPU for 5 minutes)  
- Linked the alarm to the SNS topic  
- Tested the alarm by stressing the CPU  
- Verified that the email notification was received  

## Example Stress Test Command
```bash
sudo amazon-linux-extras install epel -y
sudo yum install stress -y
stress --cpu 2 --timeout 120
```

## What I Learned
- How CloudWatch collects and displays EC2 metrics  
- How to create alarms based on thresholds  
- How SNS sends notifications to subscribers  
- How to test alarms using CPU stress tools  
- How monitoring helps with real-world troubleshooting  

## Skills Demonstrated
- CloudWatch monitoring  
- SNS notifications  
- EC2 performance testing  
- Alarm configuration  
- Troubleshooting and validation  

## Next Steps
- Add alarms for memory and disk usage  
- Create dashboards for visual monitoring  
- Automate alarm creation with CloudFormation  
- Integrate alarms with Slack or Teams  
