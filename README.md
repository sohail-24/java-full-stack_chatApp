# 🚀 Full Stack Realtime Chat Application

### DevOps & Kubernetes Production Deployment

This project demonstrates a complete **end-to-end DevOps workflow** for a Full Stack Realtime Chat Application using modern tools and best practices. It covers containerization, orchesation, networking, security, and scalable deployment using Kubernetes.

This is a real-world project designed to showcase **DevOps Engineer skills** in handling production-grade applications.

---

## 📌 Project Overview

A realtime chat application where users can:

* Sign up & login using JWT authentication
* Send realtime messages using Socket.IO
* View online users live
* Update profiles and settings
* Experience persistent sessions

The entire application is deployed using:

* Docker for containerization
* Kubernetes (Kind cluster) for orchestration
* Node.js backend API
* React + Vite frontend
* MongoDB database
* Nginx for frontend serving

---

## 🧱 Architecture

```
Browser
   |
Frontend (React + Nginx Container)
   |
NodePort Service (30080)
   |
Backend API (Node.js + Socket.io)
   |
NodePort Service (30001)
   |
MongoDB (ClusterIP)
```

### Pods Running:

* chat-frontend
* chat-backend
* mongo

---

## 🛠 DevOps Technologies Used

| Category         | Tools Used                            |
| ---------------- | ------------------------------------- |
| Containerization | Docker                                |
| Orchestration    | Kubernetes (Kind Cluster)             |
| CI Ready Design  | Image versioning (v1, v2)             |
| Frontend         | React + Vite + Nginx                  |
| Backend          | Node.js + Express + Socket.IO         |
| Database         | MongoDB                               |
| Security         | JWT Authentication + HttpOnly Cookies |
| Networking       | Kubernetes Services + Port Forward    |
| Registry         | Docker Hub (sohail28)                 |

---

## ✅ Key DevOps Features Implemented

* ✅ Multi-container microservice architecture
* ✅ Dockerized frontend and backend
* ✅ Version-controlled images pushed to Docker Hub
* ✅ Kubernetes Deployment & Services defined
* ✅ Secure JWT-based authentication
* ✅ Environment-based configuration
* ✅ Clean cluster rebuild & redeploy capability
* ✅ Realtime WebSocket communication
* ✅ Scalable pod architecture

---

## 📂 Project Structure

```
java-full-stack_chatApp/
│
├── backend/
│   ├── Dockerfile
│   ├── src/
│   └── controllers/
│
├── frontend/
│   ├── Dockerfile
│   ├── nginx.conf
│   └── src/
│
├── k8s/
│   ├── backend-deployment.yml
│   ├── backend-service.yml
│   ├── frontend-deployment.yml
│   ├── frontend-service.yml
│   ├── mongo-deployment.yml
│   └── mongo-service.yml
│
└── .env
```

---

## ⚙️ How to Deploy from Scratch

### 1️⃣ Clone the Repository

```
git clone https://github.com/sohail-24/java-full-stack_chatApp.git
cd java-full-stack_chatApp
```

### 2️⃣ Apply Kubernetes Manifests

```
kubectl apply -f k8s/
```

### 3️⃣ Verify Deployment

```
kubectl get pods
kubectl get svc
```

### 4️⃣ Access Application

```
kubectl port-forward svc/chat-frontend-service 30080:80 --address 0.0.0.0
```

Open in browser:

```
http://<YOUR_PUBLIC_IP>:30080
```

---

## 🔐 Environment Configuration

Backend uses secure environment variables:

```
MONGODB_URI=mongodb://mongo:27017/chatApp
JWT_SECRET=your-secret-key
PORT=5001
NODE_ENV=production
```

---

## 🧪 Key Testing Completed

* ✔ Login / Signup Flow
* ✔ Real-time Online Users display
* ✔ Message Sending & Receiving
* ✔ Session Persistence
* ✔ Reload & Reconnection Handling
* ✔ K8s Restart Stability

---

## 💼 Skills Demonstrated (For Recruiters)

* Kubernetes Cluster Setup & Management
* Docker Image Build & Optimization
* Full Stack CI-like Deployment
* Service Networking & Exposure
* Secure Authentication Implementation
* Troubleshooting & Debugging Production Issues
* Real-time Application Scaling Concept

---

## 📈 Future Enhancements

* Ingress Controller with NGINX
* SSL with HTTPS (Cert Manager)
* Jenkins CI/CD Pipeline
* Helm Chart Packaging
* Monitoring using Prometheus & Grafana

---

## 👨‍💻 Author

**Mohammed Sohail**
DevOps Engineer | AWS | Docker | Kubernetes

Docker Hub: [https://hub.docker.com/u/sohail28](https://hub.docker.com/u/sohail28)
GitHub: [https://github.com/sohail-24](https://github.com/sohail-24)

---

## ⭐ If you like this project

Give it a star and feel free to fork or contribute!

---

> This project represents my hands-on experience in real-world DevOps deployment and automation. It shows my capability to manage full lifecycle application deployment from code to production using industry standards.
