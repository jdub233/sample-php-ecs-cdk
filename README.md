# Sample PHP ECS Fargate Application with CDK

This is a sample PHP ECS project using AWS CDK and TypeScript, based on the [serverless cdk pattern](https://github.com/aws-samples/serverless-patterns/tree/main/fargate-cdk/cdk). It creates an ECS cluster with an http listener and all of the associated resources as defined by CDK. The cluster will run a container with the PHP image defined in the `/src` directory.  The container will run a simple page that displays an environment variable (defined in the CDK stack code).

The `cdk.json` file tells the CDK Toolkit how to execute the app.

Run `npm run cdk syth` to see the CloudFormation template that will be generated.

## Prerequisites

Run `npm install` to install the required dependencies locally to the repo. They will pick up any AWS credentials you have configured locally.

## Useful commands

* `npm run bootstrap` a one time task that is only necessary if no other CDK stacks have been deployed in the account/region.  It will create a bucket in S3 that is used by CDK to store assets.
* `npm run deploy` to deploy the stack to your default AWS account/region.  The stack will output the URL of the load balancer.  You can use this URL to access the sample page.region
* `npm run cdk destroy` to remove the stack from your default AWS account/region.
