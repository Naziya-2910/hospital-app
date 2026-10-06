# Hospital Appointment Application — AWS / DevOps Project

A hospital appointment web application built with **Spring Boot**, containerized with **Docker**, and delivered through an automated **CI/CD pipeline** (GitHub → Jenkins → Docker Build → AWS ECR → Deployment) on **AWS**.

## Overview

- Developed a hospital appointment web app with a Spring Boot backend and an HTML/CSS frontend.
- Used Git/GitHub for source control and Maven for application packaging.
- Created a Docker image and containerized the application.
- Built a CI/CD workflow to automate build and delivery.
- Practiced AWS Application Load Balancer (ALB) and Auto Scaling for traffic distribution and scaling.
- Practiced AWS ECS/EKS and Terraform concepts for container orchestration and infrastructure automation.

## Tech Stack

| Area | Tools |
|------|-------|
| Backend | Java, Spring Boot |
| Frontend | HTML, CSS |
| Build | Maven |
| Source Control | Git, GitHub |
| CI/CD | Jenkins |
| Containers | Docker |
| AWS | EC2, ECR, ALB, Auto Scaling, VPC |
| Orchestration / IaC (practiced) | ECS, EKS, Terraform |

## CI/CD Pipeline

```
GitHub  →  Jenkins  →  Maven Build  →  Docker Build  →  AWS ECR  →  Deployment (AWS EC2)
```

1. Code is pushed to GitHub.
2. Jenkins picks up the change and builds the application with Maven.
3. Jenkins builds a Docker image of the application.
4. The image is pushed to AWS ECR.
5. The container is deployed on AWS, with ALB and Auto Scaling used for traffic distribution and scaling.

## Run Locally

```bash
# Clone the repository
git clone https://github.com/Naziya-2910/hospital-app.git
cd hospital-app

# Build the application
./mvnw clean package

# Run the application
java -jar target/*.jar
```

## Run with Docker

```bash
# Build the image
docker build -t hospital-app .

# Run the container
docker run -d -p 8080:8080 hospital-app
```

Then open `http://localhost:8080` in your browser.

## Author

**Naziya Unnisa Begum** — DevOps Engineer | AWS Cloud
GitHub: [Naziya-2910](https://github.com/Naziya-2910)
