# 🚀 WordPress Docker DevOps Project

This project demonstrates a production-ready WordPress deployment using Docker, with CI/CD integration and AWS infrastructure.

## 📦 Tech Stack
Docker, WordPress, MySQL, AWS EC2, GitHub Actions (CI/CD)

## ⚙️ Features
- Containerized WordPress environment
- Clean project structure (no WordPress core in repository)
- Separation of application and data (wp-content and database)
- Automated CI pipeline using GitHub Actions
- Backup and restore scripts
- Ready for cloud deployment (AWS EC2)

## 📁 Project Structure
wordpress-docker/
├── docker-compose.yml  
├── .env  
├── .gitignore  
├── README.md  
├── wp-content/  
└── scripts/  
  ├── backup.sh  
  └── restore.sh  

## 🚀 Run Locally
docker compose up -d

Open in browser:  
http://localhost:8081

## 🔄 CI/CD
GitHub Actions pipeline automatically:
- Starts Docker containers
- Verifies WordPress availability
- Performs HTTP health check

Workflow file:  
.github/workflows/deploy.yml

## ☁️ Deployment (AWS EC2)
1. Launch EC2 instance (Ubuntu)
2. Install Docker
3. Clone repository
4. Run: docker compose up -d

Access:  
http://<EC2-IP>:8081

## 💾 Backup and Restore
Backup:  
./scripts/backup.sh  

Restore:  
./scripts/restore.sh  

## ⚠️ Notes
- WordPress core is not stored in the repository (pulled from Docker image)
- wp-content/uploads is excluded from Git
- Database is stored in Docker volumes
- Default WordPress themes are excluded

## 🎯 Purpose
This project demonstrates practical DevOps skills including containerization, CI/CD pipelines, cloud deployment, and data migration strategies.
