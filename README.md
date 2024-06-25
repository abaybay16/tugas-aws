# ![aws](https://github.com/julien-muke/Search-Engine-Website-using-AWS/assets/110755734/01cd6124-8014-4baa-a5fe-bd227844d263)     Deploy Node JS Docker Container to AWS ECS Cluster (Fargate).


## <a name="introduction">🤖 Introduction</a>

In this hands-on we're diving deep into the world of AWS as we guide you through the process of pushing your Node.js Docker container to AWS Elastic Container Registry and deploying it to AWS Elastic Container Service. 

## <a name="design">📐 Architecture Diagram</a>

![AWS EC2 Auto Scaling](https://github.com/julien-muke/aws-ec2-auto-scaling-group/assets/110755734/274005ff-7950-4846-8feb-3f64f0e927d1)



## <a name="steps">☑️ Steps</a>

The procedure for deploying this architecture on AWS consists of the following steps:

Step 1. Create WebApp Docker Image
Step 2. Create aws-cli user
Step 3. Create & push image to AWS ECR repository
Step 4. Create Security Groups
Step 5. Create AWS ECS Fargate Cluster
Step 6. Create Task Definition
Step 7. Create ECS Service with Application Load Balancer
Step 8 Update Application Load Balancer Security Group


## ➡️ Step 1 - Create WebApp Docker Image