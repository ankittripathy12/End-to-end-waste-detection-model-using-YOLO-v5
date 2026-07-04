# End-to-End Waste Detection Using YOLOv5

An end-to-end waste detection application built using **YOLOv5**. This project provides a complete pipeline for detecting waste objects, along with optional deployment workflows using **Docker**, **AWS**, **Azure**, and **GitHub Actions**.

---

## 📌 Features

- End-to-end waste detection using YOLOv5
- Modular project architecture
- Flask-based web application
- Docker support
- CI/CD with GitHub Actions
- AWS deployment using Amazon ECR and EC2
- Azure deployment using Azure Container Registry and Web Apps

---

## 📂 Project Structure

```text
.
├── app.py
├── components/
├── constants/
├── entity/
├── pipeline/
├── templates/
├── static/
├── requirements.txt
├── Dockerfile
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

Before running the project, ensure you have:

- Python 3.10 
- Conda (recommended)
- Git
- Docker (optional)

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/ankittripathy12/End-to-end-waste-detection-model-using-YOLO-v5.git

cd End-to-end-waste-detection
```

### 2. Create a Conda Environment

```bash
conda create -n waste python=3.7 -y
```

Activate the environment:

```bash
conda activate waste
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the Application

```bash
python app.py
```

After the application starts successfully, open your browser and navigate to:

```
http://localhost:5000
```

*(Use the port displayed in your terminal if it differs.)*

---

# 🏗️ Project Workflow

The project follows a modular architecture:

1. Constants
2. Entity
3. Components
4. Pipeline
5. Application (`app.py`)

---

# 🐳 Docker

Build the Docker image:

```bash
docker build -t waste-detection .
```

Run the container:

```bash
docker run -p 5000:5000 waste-detection
```

---

# ☁️ AWS Deployment (GitHub Actions)

## Services Used

- GitHub Actions
- Amazon ECR
- Amazon EC2
- Docker
- IAM

## Deployment Workflow

1. Build Docker image
2. Push image to Amazon ECR
3. Launch EC2 instance
4. Pull Docker image from ECR
5. Run the application inside Docker

---

## AWS Setup

### 1. Create an IAM User

Grant the following permissions:

- AmazonEC2ContainerRegistryFullAccess
- AmazonEC2FullAccess

---

### 2. Create an Amazon ECR Repository

Save the repository URI for later use.

Example:

```text
<account-id>.dkr.ecr.<region>.amazonaws.com/waste
```

---

### 3. Launch an EC2 Instance

Use Ubuntu as the operating system.

---

### 4. Install Docker

```bash
sudo apt-get update -y

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
```

---

### 5. Configure a Self-Hosted GitHub Runner

Navigate to:

```
Repository
→ Settings
→ Actions
→ Runners
→ New Self-hosted Runner
```

Follow the instructions provided by GitHub.

---

### 6. Configure GitHub Secrets

Add the following repository secrets:

| Secret | Description |
|---------|-------------|
| AWS_ACCESS_KEY_ID | AWS Access Key |
| AWS_SECRET_ACCESS_KEY | AWS Secret Key |
| AWS_REGION | AWS Region |
| AWS_ECR_LOGIN_URI | Amazon ECR Login URI |
| ECR_REPOSITORY_NAME | Repository Name |

---

# ☁️ Azure Deployment (GitHub Actions)

## Services Used

- GitHub Actions
- Azure Container Registry (ACR)
- Azure Web App
- Docker

---

## Build Docker Image

```bash
docker build -t <acr-name>.azurecr.io/waste:latest .
```

Login to Azure Container Registry:

```bash
docker login <acr-name>.azurecr.io
```

Push the image:

```bash
docker push <acr-name>.azurecr.io/waste:latest
```

---

## Deployment Workflow

1. Build Docker image
2. Push image to Azure Container Registry
3. Deploy to Azure Web App
4. Pull the image from ACR
5. Start the application

---

# 📦 Requirements

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# 🤝 Contributing

Contributions are welcome.

If you'd like to improve the project:

1. Fork the repository
2. Create a new branch
3. Commit your changes
4. Push your branch
5. Open a Pull Request

---

# 📄 License

This project is intended for educational and research purposes.

Feel free to modify and extend it according to your requirements.

---

# ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub.