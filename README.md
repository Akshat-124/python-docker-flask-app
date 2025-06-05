# python-docker-flask-app
# 🐳 Python Flask App in Docker

This is a simple Flask web application containerized using Docker.  
It returns a basic greeting and serves as a great beginner project for learning Docker with Python.

---

## 🚀 Project Features

- Lightweight Flask app
- Dockerized for consistent deployment
- Port mapping to access the app from your browser
- Clean project structure for easy extension

---

## 📁 Project Structure

python-docker-flask-app/
├── app.py # Flask app
├── requirements.txt # Python dependencies
└── Dockerfile # Instructions to build the Docker image

## 🛠️ Technologies Used

- Python 3.11
- Flask
- Docker

## 🧪 How to Run the App

### 🔹 Step 1: Clone the Repository

```bash
git clone https://github.com/Akshat-124/python-docker-flask-app.git
cd python-docker-flask-app
🔹 Step 2: Build the Docker Image
```bash
docker build -t flask-docker-app:1.0 .
🔹 Step 3: Run the Container
```bash
docker run -p 5000:5000 flask-docker-app:1.0
Now, open your browser and go to:
👉 http://localhost:5000

📦 Sample Output
Hello, Docker!
