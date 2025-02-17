

<img src="https://github.com/user-attachments/assets/1f7fa88b-1991-4129-a5f2-d93b26f9c341" width="1000" />



<h1 align="center">Ledgerly</h1>
<br>
<p align="center">
An open source, self hostable expense tracking platform built with NextJS, Python
<br>
and AWS for the Lambda functions and S3 object storage.
<br>
Manage and gain insights from your expenses.
<br>
</p>

<h1 align="center">Overview</h1>
<br>
<p align="center">
<img src="https://github.com/user-attachments/assets/373d6857-c452-44d3-90f6-090236fa53bf" width="600" />
<br>
 
</p>
<br>

**The backend consists of three services:-**
1. Python based REST API developed using FastAPI for serving requests <br>
2. RDS postgres database for data storage and retrieval <br>
3. S3 Bucket for image storage and hosting 

**Additional services:-**

1. Traefik:Acts as a reverse proxy for automatic SSL provisioning and log generation.<br>
2. Prometheus and Grafana: Collect and visualize resource usage with custom log exporters.<br>
All of these services are run using Docker containers to ensure availability and performance.

## Project structure 

```
.
├── README.md
├── assets
│   ├── arch.png
│   ├── banner.png
│   ├── er.png
│   ├── goaccess.png
│   ├── grafana.png
│   ├── inboundrules.png
│   └── lambda-uri.png
├── docker-compose.yml
├── monitoring
│   ├── grafana
│   │   └── datasources.yml
│   └── prometheus
│       └── prometheus.yaml
└── services
    ├── backend
    │   ├── Dockerfile
    │   ├── app
    │   │   ├── __init__.py
    │   │   ├── app.py
    │   │   ├── core
    │   │   │   ├── __init__.py
    │   │   │   ├── config.py
    │   │   │   ├── db.py
    │   │   │   └── utils.py
    │   │   ├── db
    │   │   │   ├── __init__.py
    │   │   │   └── models.py
    │   │   ├── main.py
    │   │   └── routers
    │   │       ├── __init__.py
    │   │       ├── auth.py
    │   │       ├── deps.py
    │   │       └── receipts.py
    │   ├── pyproject.toml
    │   └── uv.lock
    ├── ledgerly.sql
    └── receipt-ocr
        ├── Dockerfile
        └── app.py

```
<br>

## Features
### Website
  - [NextJS](https://nextjs.org) App Router
  - [Amazon Web Services](https://docs.aws.amazon.com/) for backend functionality with `EC2`
  - Support for `S3` File Storage, and `Lambda` Container image based Functions
  - Edge runtime-ready
### AWS infrastructure
 - [Amazon S3](https://aws.amazon.com/s3) Utilized for image storage.
  - [AWS Lambda](https://aws.amazon.com/lambda) for processing JSON and filtering required data
  - [Amazon EC2](https://aws.amazon.com/sns) for provisioning VM instances 
  - [Amazon ECR](https://aws.amazon.com/ecr) for privately hosting container images 
### External
  - [Prometheus](https://prometheus.io/docs/introduction/overview/), [Grafana](https://grafana.com/docs/grafana/latest/) and [GoAccess](https://goaccess.io/) for extensive observability and monitoring of resources. 
  - [Gemini API](https://ai.google.dev/gemini-api/docs) for image to text extraction using Vision Model within free tier limits.
  - [Github Actions](https://github.com/features/actions) CI pipelines to build, test and push application images from Github to various registries.
  - [Traefik](https://doc.traefik.io/) acts as a dynamic reverse proxy and automatically manages SSL/TLS certificates

## Working
-A picture of the bill is uploded to the S3 bucket. 
<br>
-lambda function is triggered and it scan and get the total amount from the bill.
<br>
-The expense data is stored in PostgreSQL database.



 
## Tech Stack
![NextJs](https://img.shields.io/badge/Nextjs-black?style=for-the-badge&logo=nextdotjs&logoColor=white)
![Python](https://img.shields.io/badge/Python-blue?style=for-the-badge&logo=python&logoColor=white)
![Uvicorn](https://img.shields.io/badge/uvicorn-E6526F.svg?style=for-the-badge&logo=gunicorn&logoColor=white)
![EC2](https://img.shields.io/badge/ec2-orange?style=for-the-badge&logo=amazon-ec2&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![ECR](https://img.shields.io/badge/ecr-f06611.svg?style=for-the-badge&logo=square&logoColor=white)
![S3](https://img.shields.io/badge/S3-darkgreen?style=for-the-badge&logo=amazon-s3&logoColor=white)
![Lambda](https://img.shields.io/badge/Lambda-FF9900?style=for-the-badge&logo=aws-lambda&logoColor=white)
![Gemini](https://img.shields.io/badge/gemini-8E75B2?style=for-the-badge&logo=google%20gemini&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)
![Grafana](https://img.shields.io/badge/grafana-%23F46800.svg?style=for-the-badge&logo=grafana&logoColor=white)
![Traefik](https://img.shields.io/badge/Traefik-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=Prometheus&logoColor=white)





