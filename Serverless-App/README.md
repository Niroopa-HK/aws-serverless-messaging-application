                                          ###AWS Serverless Messaging Application
Designed and developed a serverless web application that enables users to send email and SMS notifications using AWS services, including Lambda, API Gateway, Step Functions, Amazon SES, and Amazon SNS. The solution eliminates the need for traditional server management while providing a scalable, cost-effective, and highly available architecture for message delivery and workflow automation.

Tools: 
(AWS) 
- S3 
- API Gateway 
- Lambda 
- Step Functions 
- SNS 
- SES 
(Programming) 
- Python 
- JS & Json 
- Html

Process: 
Step-1: Create Lambda Role 
- Go to IAM > Roles > Create Role 
- Choose AWS Service > Lambda 
- Attach Full Access policies for: 
- SES 
- SNS 
- Step Functions 
- Name and create the role.

<img width="1915" height="910" alt="Screenshot 2026-06-20 105642" src="https://github.com/user-attachments/assets/57f3d3cb-f265-4628-805f-6a043da55618" />

Step-2: Connect Lambda to SES & SNS 

• Create Lambda Function 1: sendEmail.py 
o Uses SES to send email 
• Create Lambda Function 2: sendSMS.py 
o Uses SNS to send SMS 
• Assign the IAM role to both functions

SES

<img width="1905" height="857" alt="Screenshot 2026-06-20 111323" src="https://github.com/user-attachments/assets/5d82a966-fd7a-4e27-a350-bdca5b0ce86b" />
