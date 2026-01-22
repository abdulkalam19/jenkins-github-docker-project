🚀 Jenkins + GitHub + Docker CI/CD Project
📌 Project Overview

This project demonstrates a basic CI/CD pipeline where Jenkins automatically pulls source code from GitHub, builds a Docker image, and deploys a web application inside a Docker container.

The application is a simple static HTML page served using NGINX and deployed automatically through Jenkins.

🛠️ Tools & Technologies

Git & GitHub – Version control and source code management

Jenkins (Freestyle Job) – CI/CD automation

Docker & Docker Desktop – Containerization

NGINX – Web server

HTML – Application code

Windows OS – Execution environment

📂 Project Structure
jenkins-github-docker-project/
├── Dockerfile
├── index.html
└── README.md

⚙️ How the Project Works

Source code is stored in GitHub.

Jenkins job is triggered manually.

Jenkins pulls the latest code from GitHub.

Jenkins builds a Docker image using the Dockerfile.

Jenkins runs a Docker container from the image.

Application is exposed via port mapping and accessed through a browser.

🐳 Dockerfile
FROM nginx:latest
COPY index.html /usr/share/nginx/html/index.html

🧪 Jenkins Build Commands

Jenkins executes the following Windows batch commands:

cd C:\Users\kalam\.jenkins\workspace\github-docker-webapp

docker rm -f github-webapp-container

docker build -t github-webapp .

docker run -d -p 8086:80 --name github-webapp-container github-webapp

🌐 Application Access

After a successful Jenkins build, open the browser and visit:

http://localhost:8086

✅ Output

The web page displays:

Jenkins + GitHub + Docker Working!
Deployed automatically using Jenkins.

⚠️ Issues Faced & Fixes

Dockerfile not found: Fixed Dockerfile naming issue (Dockerfile.txt → Dockerfile)

Jenkins could not access WSL paths: Moved project to Windows Documents folder

Wrong Jenkins build step: Used Execute Windows batch command instead of Execute Shell

Docker daemon issue: Ensured Docker Desktop was running and accessible

📘 Learning Outcomes

Understood CI/CD fundamentals using Jenkins

Integrated GitHub with Jenkins

Built and deployed Docker containers automatically

Learned real-world troubleshooting on Windows and WSL

Gained hands-on DevOps experience

📄 Resume Summary

Automated the deployment of a Dockerized web application using GitHub, Jenkins, and Docker.

🔗 GitHub Repository

https://github.com/abdulkalam19/jenkins-github-docker-project

👤 Author

Abdul Kalam
