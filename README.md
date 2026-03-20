**Project Overview**

This project demonstrates a complete CI/CD pipeline using AWS services. The application is containerized using Docker and deployed on Kubernetes (Amazon EKS) with a LoadBalancer for public access.

**Technologies Used**

GitHub (Version Control)

AWS CodeBuild (CI)

Docker (Containerization)

Docker Hub (Image Registry)

Kubernetes (EKS)

AWS CloudWatch (Monitoring)

**Pipeline Flow**
GitHub → CodeBuild → Docker → Docker Hub → EKS → LoadBalancer → Live App
⚙️ Setup Instructions
1. Clone Repository
git clone https://github.com/dlokeshmech-glitch/Brain-Tasks-App
cd Brain-Tasks-App
2. Build Docker Image
docker build -t lokeshdev7/brain-app .
docker push lokeshdev7/brain-app
3. Deploy to Kubernetes (EKS)
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
4. Get Application URL
kubectl get svc
**Application URL**
arn:aws:elasticloadbalancing:ap-south-1:064863113663:loadbalancer/net/k8s-default-brainapp-116bcdd3fa/9289fd3bb56d7a3a

**Monitoring**

CloudWatch Logs used for build monitoring

** Kubernetes**
kubectl get pods
kubectl get svc
