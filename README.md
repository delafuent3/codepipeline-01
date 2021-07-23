# codepipeline-01
Example on how to configure codepipeline to deploy an S3 bucket to aws

1.- Create a repo to store the CloudFormation Templates
2.- Create IAM Role for CodePipeline
  a.- Create Role for EC2 (Dont attach any policy)
  b.- Edit Role and attach inline policy (custom_codepipeline_policy.json)
  c.- Edit Trust Relationship (Replace ec2 with codepipeline)

3.- Create IAM Role for CloudFormation to have access to s3
  a.- Create Role for CloudFormation
  b.- Attach the policy "AmazonS3FullAccess"

4.- Create pipeline
  a.- Go to CodePipeline -> Pipelines -> Click "Create Pipeline"
  b.- Write a name
  c.- In "Service Role" select "Existing service role" and select role created in Step 1
