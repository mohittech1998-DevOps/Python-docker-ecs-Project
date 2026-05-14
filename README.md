Docker to AWS ECS Deployment Project 🚀

This project is a simple Python Flask application containerized using Docker and prepared for deployment on AWS ECS (Elastic Container Service).

Project Overview

The application displays a basic web page using Flask and runs inside a Docker container. The project demonstrates how to:

Build a Python Flask application
Create a Docker image
Run the application inside a container
Push Docker image to AWS ECR
Deploy containerized application on AWS ECS Fargate
Access application through Load Balancer
Technologies Used
Python
Flask
Docker
AWS ECS
AWS ECR
Application Load Balancer (ALB)
Application Code

The Flask application runs on port 3000 and returns a simple response:

from flask import Flask

app = Flask(__name__)

@app.route('/')
def home():
    return "Python ECS Project Running 🚀"

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=3000)
Docker Build Command
docker build -t flask-ecs-app .
Run Docker Container
docker run -d -p 3000:3000 flask-ecs-app
Verify Application

Open browser:

http://localhost:3000
Project Benefits
Containerized deployment
Consistent environment across systems
Easy portability
Cloud-ready architecture
Simplified deployment process
Learning Outcome

This project helped in understanding:

Docker image creation
Container lifecycle
Python dependency management
AWS container services
Basic DevOps deployment workflow
Future Improvements
CI/CD pipeline integration
Auto Scaling in ECS
HTTPS with Load Balancer
Monitoring using CloudWatch
Multi-container microservices architecture
