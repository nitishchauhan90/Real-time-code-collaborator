🚀 Real-Time Code Collaborator

A production-ready Real-Time Collaborative Code Editor built using React, Node.js, Express, Socket.IO, and Yjs (CRDT). The platform enables multiple developers to join a room and collaboratively edit code in real time with automatic conflict resolution.

The application is fully containerized using Docker and deployed on AWS ECS, with Amazon ECR for container image storage and an Application Load Balancer (ALB) for routing external traffic.

⸻

🌐 Live Demo

Application URL

http://docker-aws-alb-616852119.eu-north-1.elb.amazonaws.com/?username=nitish

Current deployment uses an AWS Application Load Balancer over HTTP. HTTPS can be enabled using AWS Certificate Manager (ACM) and a custom domain.

✨ Features

* 🚀 Real-time collaborative code editing
* 👥 Multi-user collaboration
* 🏠 Room-based coding sessions
* 🔄 Conflict-free concurrent editing using Yjs (CRDT)
* ⚡ Instant synchronization using Socket.IO
* 💻 Monaco Code Editor
* 📱 Responsive UI
* 🐳 Dockerized frontend & backend
* ☁️ Production deployment using AWS ECS
* 📦 Amazon ECR image repository
* ⚖️ Application Load Balancer
* 🔐 Secure architecture (HTTPS-ready)
* 📈 Horizontal scaling ready

⸻

🛠 Tech Stack

Frontend

* React.js
* JavaScript
* HTML5
* CSS3
* Monaco Editor
* Socket.IO Client
* Yjs
* Axios

Backend

* Node.js
* Express.js
* Socket.IO
* Yjs
* REST API

DevOps & Cloud

* Docker
* Multi-stage Docker Build
* Amazon ECS
* Amazon ECR
* Application Load Balancer (ALB)
* IAM
* Security Groups
* CloudWatch

🏗 System Architecture


                         Users
                           │
                           ▼
                  Application Load Balancer
                           │
                           ▼
                    Amazon ECS Service
                           │
                    ECS Task (Container)
                           │
                 Node.js + Express Server
                           │
          ┌────────────────┴────────────────┐
          ▼                                 ▼
     React Static Files              Socket.IO Server
                                              │
                                              ▼
                                      Yjs Shared Document
                                              │
                     ┌────────────────────────┼────────────────────────┐
                     ▼                        ▼                        ▼
                 Browser A               Browser B               Browser C

⸻

