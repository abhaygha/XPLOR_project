nfrastructure Stack for Static Website
This project sets up the infrastructure to host a static website using AWS CDK in TypeScript. The infrastructure includes an S3 bucket to store the website content and a CloudFront distribution for content delivery.

Prerequisites
AWS CLI configured with appropriate permissions.
Node.js and npm installed.
AWS CDK installed (npm install -g aws-cdk).
Project Structure
plaintext
Copy code
├── bin
│   └── infrastructure.ts
├── lib
│   └── infrastructure-stack.ts
├── website
│   └── index.html
│   └── error.html
├── .gitignore
├── cdk.json
├── package.json
├── README.md
├── tsconfig.json
Deployment Instructions
Install Dependencies

bash
Copy code
npm install
Build the CDK App

bash
Copy code
npm run build
Synthesize the CloudFormation Template

bash
Copy code
cdk synth
Deploy the Stack

bash
Copy code
cdk deploy
Access the Website

After successful deployment, the CloudFront URL will be provided in the output. Use this URL to access the static website.

bash
Copy code
Outputs:
Outputs:
InfrastructureStack.CfnOutCloudFrontUrl = https://d31zs4xonho09p.cloudfront.net
InfrastructureStack.CfnOutDistributionId = E2AU5NX1Y0VQE3
Stack ARN:
arn:aws:cloudformation:us-east-1:891377120087:stack/InfrastructureStack/16332700-4a68-11ef-88d6-0affdc3634cd
Accessing the Website
After deployment, access your website using the CloudFront URL provided in the output. Open your web browser and navigate to the provided URL to see the index.html page.

Future Improvements
Security
Use AWS WAF: Integrate AWS WAF with CloudFront to protect against common web exploits.
S3 Bucket Policies: Enhance S3 bucket policies to restrict access further.
CloudFront Security: Use additional CloudFront security features like Geo-Restriction.
Observability
AWS CloudWatch: Set up CloudWatch alarms and dashboards for monitoring.
