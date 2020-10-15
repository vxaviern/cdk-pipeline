# CDK-Pipeline

Esta aplicacion de CDK hace 2 cosas:

1. Crea un CodePipeline con 3 etapas (Source --> Build --> Deploy)
2. Despliega una funcion lambda utilizando la CodePipeline 

Cualquier cambio que se le haga a la funcion lambda (index.ts) sera detectada por la Pipeline y **automaticamente se dispara un build**

## Pre-Requisitos
1. [AWS CDK instalado](https://cdkworkshop.com/15-prerequisites/500-toolkit.html)

### Configurar el proyecto de Typescript
1. Creen un repositorio CodeCommit y llamenlo **pipeline** usando la consola de AWS o la CLI
2. Clonen el repositorio: git clone CODECOMMIT-REPO-URL **pipeline**
3. cd pipeline
4. cdk init --language typescript
5. npm install @aws-cdk/aws-codedeploy @aws-cdk/aws-lambda @aws-cdk/aws-codebuild @aws-cdk/aws-codepipeline
6. npm install @aws-cdk/aws-codecommit @aws-cdk/aws-codepipeline-actions @aws-cdk/aws-s3
7. rm -rf test
8. git add --all
9. git commit -m "initial commit"
10. git push

## Copiar el Codigo

1. lambda/lambda.ts
2. lib/lambda-stack.ts
3. lib/pipeline-stack.ts
4. bin/pipeline.ts
5. git add --all
6. git commit -m "add CDK app"
7. git push

## Crear CodePipeline y Desplegar la Funcion Lambda

1. cdk bootstrap
2. cdk deploy PipelineDeployingLambdaStack

## Borrar la Infraestructura

Desde la consola de Cloudformation, borren ambos stacks en **este orden**:

1. LambdaDeploymentStack
2. PipelineDeployingLambdaStack

