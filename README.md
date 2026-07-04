# End-to-End Waste Detection Using YOLOv5

An end-to-end waste detection application built using **YOLOv5**. This project provides a complete pipeline for detecting waste objects.

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


# 📦 Requirements

Install dependencies:

```bash
pip install -r requirements.txt
```



---

## 📸 Demo

<p align="center">
  <img src="screenshot.png" alt="Waste Detection using YOLOv5 Web Application" width="100%">
</p>

The web application allows users to upload an image, run inference using a trained **YOLOv5** model, and visualize the detected waste object along with its confidence score.

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