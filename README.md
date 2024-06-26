# Architecture
![sitemap](https://github.com/memor24/myWebsite-backend/assets/112832477/fac305d9-f99c-488a-8ce9-d4c3f453ba0b)

# Backend
## Lambda Function
Since we use the serverless function, also known as FaaS-Function as a Service- this is a Python code for the Lambda serverless function that updates a counter when the page is viewd and stores it in a DynamoDB table like this:

![my ddb](https://github.com/memor24/myWebsite-backend/assets/112832477/e1eba4df-9a27-46f2-8681-32054399f111)

The JavaScript invokes the lambda funtion directly and shows the updated view count on the page. An application loadbalancer (AWS-ALB) will be added for additional security and will be secured further using a web application firewall (WAF). A Pytest code will be added into the continuous delivery in the test environment.

## Infrastructure as Code
TBU: All the AWS resources are defined as Terraform code and deployed using Terraform commands automatically.
Also the code for Lambda function is Dockerized and integrated via Jenkins to ECR. The Jenkins pipeline itself will be fully automated.
