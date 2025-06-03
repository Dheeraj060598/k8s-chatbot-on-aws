# Chatbot on AWS EC2 using Kubernetes

This project demonstrates deploying a simple Flask-based chatbot using Docker and Kubernetes on an AWS EC2 instance.

## Features
- Python Flask chatbot
- Dockerized deployment
- Kubernetes managed service
- Hosted on AWS EC2 using Minikube

## Setup

### 1. Clone the repository
```bash
git clone https://github.com/your-username/k8s-chatbot-on-aws.git
cd k8s-chatbot-on-aws
```

### 2. Build Docker Image
```bash
docker build -t chatbot:latest .
```

### 3. Push to DockerHub
```bash
docker tag chatbot:latest your-dockerhub-username/chatbot:latest
docker push your-dockerhub-username/chatbot:latest
```

### 4. Apply Kubernetes Manifests
```bash
kubectl apply -f kubernetes/deployment.yaml
kubectl apply -f kubernetes/service.yaml
```

### 5. Access the App
Open browser: `http://<EC2_PUBLIC_IP>:30036`

## License
MIT
