# EMR Serverless

Sample pulumi project to deploy an EMR serverless to AWS

## Workflows

Pull request on branch "main" triggers a pulumi preview
Pull request completed on branch "main" triggers a pulumi up
 
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

## Troubleshooting

Documentation: 
* https://docs.aws.amazon.com/emr/latest/EMR-Serverless-UserGuide/jobs-troubleshoot.html
* https://docs.aws.amazon.com/emr/latest/EMR-Serverless-UserGuide/security-iam-user-access-policies.html
