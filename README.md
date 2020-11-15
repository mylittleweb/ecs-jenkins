# Prerequisite

Install the following binaries:
* awscli (https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html)
* docker (https://docs.docker.com/get-docker/)


# VPC initialization

```
aws cloudformation create-stack --stack-name init-ci --template-body file://init-ci.yaml
aws cloudformation wait stack-create-complete --stack-name init-ci
```

# Deploy Jenkins
```
aws cloudformation create-stack --stack-name ecs-jenkins --template-body file://ecs-jenkins.yaml --capabilities CAPABILITY_NAMED_IAM
aws cloudformation wait stack-create-complete --stack-name ecs-jenkins
```
