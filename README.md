EBS Snapshot Cleanup using AWS Lambda, EventBridge, and SNS

																																					
Features 

✅ Identifies and deletes unattached EBS snapshots

✅ Uses EventBridge to run daily (or as scheduled) 

✅ Sends SNS notifications after cleanup 

✅ Optimizes AWS storage costs 



Setup Instructions


1. Deploy the Lambda Function
   
   Create an AWS Lambda function

   Use Python 3.9+ runtime

   Upload the lambda_function.py script

   Add necessary IAM permissions (EBS, SNS)



3. Configure AWS SNS for Notifications
   
   Create an SNS topic (e.g., EBS-Snapshot-Alerts)

   Subscribe your email to the topic

   Update SNS_TOPIC_ARN in lambda_function.py



4. Set Up EventBridge Rule for Automation
   
   Go to AWS EventBridge → Rules → Create Rule

   Choose Schedule Expression: cron(0 0 * * ? *) (Runs daily)

   Set Lambda as the target function



Technologies Used

AWS Lambda

AWS SNS (Simple Notification Service)

AWS EventBridge (CloudWatch)

AWS EC2 API (EBS Snapshots Management)

Python Boto3 SDK
