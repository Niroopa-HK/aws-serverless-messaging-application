                                          ### AWS Serverless Messaging Application
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

- Create Lambda Function 1: sendEmail.py 
- Uses SES to send email 
- Create Lambda Function 2: sendSMS.py 
- Uses SNS to send SMS 
- Assign the IAM role to both functions

SES-->

<img width="1905" height="857" alt="Screenshot 2026-06-20 111323" src="https://github.com/user-attachments/assets/5d82a966-fd7a-4e27-a350-bdca5b0ce86b" />

SMS-->

<img width="1908" height="902" alt="Screenshot 2026-06-20 111350" src="https://github.com/user-attachments/assets/0f11185f-1dda-4194-9b62-3cca55094573" />

Step-3: Create Step Function Workflow 
- Go to Step Functions > Create State Machine 
- Define a workflow: 
- Input validation 
- Conditional logic (email, SMS, or both) 
- Invoke appropriate Lambda functions

                                               ## Step Function
  
  <img width="1917" height="887" alt="Screenshot 2026-06-20 114622" src="https://github.com/user-attachments/assets/0e76c324-23a0-4108-b0da-3bdb83993401" />

Step-4: Create REST API Handler 
- Create Lambda Function 3: handler.py 
- Accepts JSON input from frontend 
- Starts Step Function execution

<img width="1918" height="905" alt="Screenshot 2026-06-20 111504" src="https://github.com/user-attachments/assets/b33c0ff2-e682-4be2-ae94-1120ca318efc" />

Step-5: Set Up API Gateway 
- Go to API Gateway > Create API 
- Create a REST API with /send endpoint 
- Integrate with handler.py Lambda 
- Enable CORS for frontend access

<img width="1918" height="908" alt="Screenshot 2026-06-20 115010" src="https://github.com/user-attachments/assets/6cdd6a18-6b5c-4681-a5a6-4db54b192b58" />

 
Step-6: Upload Website to S3 
- Build your frontend using HTML + JS 
- Go to S3 > Create Bucket 
- Upload your files 
- Enable Static Website Hosting 
- Set permissions for public access

<img width="1918" height="1013" alt="Screenshot 2026-06-20 122905" src="https://github.com/user-attachments/assets/bf8edb70-c7ee-43b2-8b72-377e18a27197" />

<img width="1915" height="888" alt="Screenshot 2026-06-20 115049" src="https://github.com/user-attachments/assets/f738b394-dd23-436b-a56d-af3b8fba2867" />

<img width="1918" height="862" alt="Screenshot 2026-06-20 123411" src="https://github.com/user-attachments/assets/be3de294-99ea-44c6-92c3-9497ce9bdbdf" />

OUTPUT: http://serverless-message-app.s3-website.ap-south-1.amazonaws.com 


<img width="1912" height="895" alt="Screenshot 2026-06-20 111233" src="https://github.com/user-attachments/assets/a20e5436-3b09-41f5-9494-9c30bd5e60da" />

Conclusion

## Conclusion

This project demonstrates the power of serverless architecture in building scalable, reliable, and cost-effective cloud applications. By integrating Amazon S3, API Gateway, AWS Lambda, Step Functions, Amazon SES, and Amazon SNS, a complete messaging platform was developed without the need to provision or manage servers.

Through this project, I gained hands-on experience in designing event-driven workflows, orchestrating serverless services, implementing REST APIs, and automating email and SMS notifications using AWS. It strengthened my understanding of cloud-native application development, security, workflow automation, and serverless computing best practices.

This project reflects my practical experience with AWS services and my ability to design modern cloud solutions that are scalable, highly available, and efficient. It also serves as a strong foundation for building more advanced cloud and DevOps solutions in the future.

⭐ Show Your Support

If this project helped you learn something new about AWS Serverless Architecture, consider giving it a ⭐ on GitHub.
