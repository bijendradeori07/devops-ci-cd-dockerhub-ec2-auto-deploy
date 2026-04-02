# Project 4: Docker Hub Image Registry Integration with Github Actions

## 📌 Overview

This Project demonstrates a complete CI/CD pipelines where a Docker Image is built using Github Actions, pushes to Docker Hub and Deployed on an AWS EC2 instance

## 🧠 Architecture

Code → GitHub → GitHub Actions → Docker Hub → AWS EC2 → Live Application

## 💻 Tech Stack

- Docker
- GitHub Actions
- AWS EC2
- Nginx (for serving static content)

## 📂 Project Structure

```
dockerhub-image-registry-github-actions/
    ├─────── Dockerfile
    ├─────── index.html
    ├─────── README.md
    └─────── .github/
                └─────── workflows/
                            └─────── docker.yml
```

## 🔥 WorkFlow Steps

1. Push to Code
2. GitHub Actions build Docker Image
3. Image is tagged and pushed to Docker Hub
4. EC2 instance pulls the latest image
5. Container runs on port 80

## 🐳 Docker Commands

### Build Image 
```
docker build -t <dockerhub-username/image-name> .
```
### Run Container
```
docker run -d -p 80:80 <dockerhub-username/image-name>
```

## 🔐GitHub Secrets Used

- DOCKER_USERNAME
- DOCKER_PASSWORD

## 🌐Live Output

Application deployed on AWS EC2 using Docker container

## 📈Learning Outcomes

- CI/CD pipeline setup using GitHub Actions
- Docker Image creation and management
- DockerHub integration
- Cloud deployment using AWS EC2

## 🚀Future Improvements

- Automate deployment using SSH in GitHub Actions
- Add Terraform for infrastructure automation
- Integrate Kubernetes for scaling
- Add monitoring with Prometheus and Grafana


## 👨‍💻Author
Bijendra  Kumar Deori
