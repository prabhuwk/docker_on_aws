##Docker on AWS

ECS stack deploys **httpd and mysql containers** exposing only port 80. httpd will be able to communicate with mysql container without port mapping in link mode. Creates consistent mount point for storing web content and database. Logs will be forwarded to cloudwatch using awslogs log driver. Leverages functionality of ECS service to make container services available all time. AMI (amazon-ecs-optimized) are used to spin up instances. ECS container instances that run agent uses ECS instance role to join ECS cluster. Cluster Instances can be resized dynimcally.

### Create or Terminate ECS Stack
1. Security Group
2. ECS Instance IAM role
3. ECS Cluster
4. ECS Cluster Instance
5. Cloudwatch log group for container logs
6. ECS Task Definition for httpd and mysql linked container
7. ECS Service
8. Deploy Web Content
