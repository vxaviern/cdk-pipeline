# CDK-Pipeline

This CDK app does 2 things:

1. Deploys a CodePipeline with 3 stages (Source --> Build --> Deploy)
2. Deploys a Lambda Functions using 1

Any code changes done to the lambda function (index.ts) will be picked up by the pipeline and a build will be triggered **automatically**

## Pre-Requisites
1. AWS CDK installed

### Setting Up TypeScript Project
1. Create a new CodeCommit repository named **pipeline** using the CodeCommit console or the AWS CLI.
2. Clone empty repo from above: git clone CODECOMMIT-REPO-URL **pipeline**
3. cd pipeline
4. cdk init --language typescript
5. npm install @aws-cdk/aws-codedeploy @aws-cdk/aws-lambda @aws-cdk/aws-codebuild @aws-cdk/aws-codepipeline
6. npm install @aws-cdk/aws-codecommit @aws-cdk/aws-codepipeline-actions @aws-cdk/aws-s3
7. rm -rf test
8. git add --all
9. git commit -m "initial commit"
10. git push

## Copy Code

11. lambda/lambda.ts
12. lib/lambda-stack.ts
13. lib/pipeline-stack.ts
14. bin/pipeline.ts
15. git add --all
16. git commit -m "add CDK app"
17. git push

## Deploy Pipeline

18. cdk bootstrap
19. cdk deploy PipelineDeployingLambdaStack

