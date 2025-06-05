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

###🔹step 1: clone this repository
```bash
git clone https://github.com/Akshat-124/python-docker-flask-app.git
cd python-docker-flask-app
###🔹Step 2: Build the Docker Image
```bash
docker build -t flask-docker-app:1.0 .
###🔹Step 3: Run the Container
```bash
docker run -p 5000:5000 flask-docker-app:1.0
Now, open your browser and go to:
👉 http://localhost:5000

📦 Sample Output
Hello, Docker!

## 📄 File Descriptions

### 🐍 `app.py`

This is the main Python file that contains your Flask web application code.  
It defines the web server logic, routes, and responses.

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def hello():
    return "Hello, Docker!"

if __name__ == "__main__":
    app.run(host="0.0.0.0", port=5000)

🐳 Dockerfile:-
This file contains the instructions to build your custom Docker image for the Flask app.

Key parts include:

Using a Python base image

Installing required dependencies

Copying your application code into the image

Defining how the container starts

Example:

```Dockerfile

FROM python:3.11-slim
WORKDIR /app
COPY requirements.txt requirements.txt
RUN pip install --no-cache-dir -r requirements.txt
COPY . .
CMD ["python", "app.py"]

📦 requirements.txt:-
This file lists all the Python dependencies your Flask app needs.
When Docker builds the image, it installs these libraries.

Example contents:

nginx
flask
