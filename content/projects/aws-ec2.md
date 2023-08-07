---
title: "AWS-EC2"
description: "Building Infrastructure for Basic Website"
dateString: "May 2020 "
ShowWordCount: true
ShowReadingTime: true
draft: false
tags: ["AWS", "EC2", "Docker", "Flask", "Python"]
showToc: false
weight: 205
cover:
   # image: "projects/face-landmarks-detection/cover.jpg"
--- 
### 🔗 [GitHub](https://github.com/gabrielaliera/AWS-ECS-EC2-Flask)

## Project Summary
***
The aim of this project is to build the infrastructure associated with continuous deployment in a CI/CD pipeline. A simple Flask application is packaged into a Docker image, which is then automatically deployed to AWS. AWS technologies utilized in this project include IAM, ECR, ECS, and Route53. Elastic Container Registry (ECR) holds the Docker image. When the code is committed this repository, GitHub workflow will build and push a new container image to Amazon ECR, and then will deploy a new task definition to Amazon ECS, when there is a push to the main branch. An application load balancer is used to direct user requests to the appropriate EC2 instance, and a domain name purchased from Route53 is utilized to customize the URL.
