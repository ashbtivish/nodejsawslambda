# nodejsawslambda
Test Repo for AWS Lambda Function with NodeJS

To run this Application on AWS Lamba

1. Create AWS Access key
2. Install Serverless framework using npm command below
npm install -g serverless

3. Login to the AWS Acccount using Serverless CLI below
serverless config credentials --provider aws --key '<AccessKey>' --secret '<SecretKey>'
 
4. Depoy the package using
serverless deploy

------------------------------------------------------------------------------------------------------------------
