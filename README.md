# container_aws

## Build pFire container and push to aws
```

  # docker build -t hello-world .
  aws configure
  
  aws ecr  create-repository --repository-name pfire-aws --region us-east-1
  
  aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 513869766554.dkr.ecr.us-east-1.amazonaws.com
  
  docker pull insigneopfire/pfire:v0.4.0
  docker image tag insigneopfire/pfire:v0.4.0 pfire_aws_040
  #docker push  513869766554.dkr.ecr.us-east-1.amazonaws.com/pfire_aws_040
  docker tag pfire_aws_040:latest 513869766554.dkr.ecr.us-east-1.amazonaws.com/pfire-aws
  docker push  513869766554.dkr.ecr.us-east-1.amazonaws.com/pfire-aws

```
