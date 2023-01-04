# EMR Serverless

Sample pulumi project to deploy an EMR serverless to AWS

**CAUTION: please keep emr-serverless automatic provisionning private by default**

## Provision the project

Fetch dependencies and then use pulumi up command: 
```
npm install
pulumi up
```

## Run job on EMR Serverless

```
spark-submit s3://deployment-dev-xxxxxxx/jobs/sample-job-assembly-1.0.jar s3://data-dev-xxxxxxx/in/sample.csv s3://data-dev-xxxxxxx/out/sample-json 
```

## Configure the secrets for Workflows 

Setup the following repository secrets: 
* AWS_ACCESS_KEY_ID
* AWS_REGION
* AWS_SECRET_ACCESS_KEY
* PULUMI_ACCESS_TOKEN

## Workflows

Pull request on branch "main" triggers a pulumi preview
Pull request completed on branch "main" triggers a pulumi up


## Troubleshooting

Documentation: 
* https://docs.aws.amazon.com/emr/latest/EMR-Serverless-UserGuide/jobs-troubleshoot.html
* https://docs.aws.amazon.com/emr/latest/EMR-Serverless-UserGuide/security-iam-user-access-policies.html
