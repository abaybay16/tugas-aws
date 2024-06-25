# ![aws](https://github.com/julien-muke/Search-Engine-Website-using-AWS/assets/110755734/01cd6124-8014-4baa-a5fe-bd227844d263)     Deploy Node JS Docker Container to AWS ECS Cluster (Fargate).


## <a name="introduction">🤖 Introduction</a>

Amazon ECS uses Docker images in task definitions to launch containers. Docker is a technology that provides the tools for you to build, run, test, and deploy distributed applications in containers.

In this hands-on we're diving deep into the world of AWS as we guide you through the process of pushing your Node.js Docker container to AWS Elastic Container Registry and deploying it to AWS Elastic Container Service.


## <a name="design">📐 Architecture Diagram</a>

![Docker Image-2](https://github.com/julien-muke/nodejs-docker-aws-ecs/assets/110755734/121e371a-3b6f-4a7c-a20d-34a05b2af90a)


## Use Case: Deploying Web Application on Amazon ECS.

Imagine you are developing a basic web application, and you want to deploy it using Amazon ECS. Example: Imagine a simple Node.j  application that displays "Hello, World!" on a webpage. The Dockerfile could specify the Node.js base image and install any required dependencies. You'd then build and push the image to ECR. Finally, by creating an ECS service with your task definition, you'd deploy the application on Fargate, making it accessible on the internet.


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

Amazon ECS uses Docker images in task definitions to launch containers. Docker is a technology that provides the tools for you to build, run, test, and deploy distributed applications in containers. 

To create a Docker image of a simple web application:

1. Create a file called Dockerfile. A Dockerfile is a manifest that describes the base image to use for your Docker image and what you want installed and running on it. For more information about Dockerfiles.

```bash
touch Dockerfile
```

2. Edit the Dockerfile you just created and add the following content.

```bash
FROM node:alpine

WORKDIR /nodejs-docker-aws-ecs

COPY package.json .

RUN npm install

COPY . .

EXPOSE 3000

CMD [ "node", "app.js" ]
```

