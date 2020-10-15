# CDK-Pipeline

## Pre-Requisites
1. AWS CDK installed

### Setting Up Project
1. Create a new CodeCommit repository named **pipeline** using the CodeCommit console or the AWS CLI.
2. Clone empty repo from above: git clone CODECOMMIT-REPO-URL pipeline
3. cd pipeline
4. cdk init --language typescript
5. npm install @aws-cdk/aws-codedeploy @aws-cdk/aws-lambda @aws-cdk/aws-codebuild @aws-cdk/aws-codepipeline
6. npm install @aws-cdk/aws-codecommit @aws-cdk/aws-codepipeline-actions @aws-cdk/aws-s3
7. rm -rf test
8. git add --all
9. git commit -m "initial commit"
10. git push

