# Documentation


# 🎬 Movie Shop API

A RESTful API for managing movie data, built using **FastAPI** and **Pydantic**. This API allows users to retrieve and add movie information, including details such as movie title, director, and release date.

## 📚 Table of Contents
- [Overview](#overview)
- [Technologies](#technologies)
- [Features](#features)
- [Installation](#installation)
- [API Endpoints](#api-endpoints)
- [Usage Examples](#usage-examples)
- [Contributing](#contributing)


---

## 📝 Overview

The **Movie Shop API** is designed to manage a movie database. The API is built using FastAPI, a modern, fast web framework for building APIs with Python. Pydantic is used for data validation, ensuring that only valid data is processed by the API.

This API is asynchronous and can handle multiple requests efficiently, making it ideal for high-performance applications.

---

## 🛠️ Technologies

- **Python 3.12**
- **FastAPI**
- **Pydantic**
- **Uvicorn** (ASGI server)
- **Datetime** (Python's built-in module)

---

## 🚀 Features

- **GET**: Retrieve a list of movies.
- **POST**: Add a new movie to the database.
- Input validation with **Pydantic** to ensure data integrity.
- Asynchronous processing for fast and efficient responses.
- Auto-generated API documentation via OpenAPI and Swagger UI.

---

## 📥 Installation

To set up and run this project locally, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/movieshop-api.git
   ```

2. **Navigate to the project directory**:
   ```bash
   cd movieshop-api
   ```

3. **Create a virtual environment**:
   ```bash
   python -m venv .venv
   ```

4. **Activate the virtual environment**:
   - On Windows:
     ```bash
     .venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source .venv/bin/activate
     ```

5. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

6. **Run the application**:
   ```bash
   uvicorn main:app --reload
   ```

7. Open your browser and navigate to:
   - **Swagger UI**: `http://127.0.0.1:8000/docs`
   - **ReDoc**: `http://127.0.0.1:8000/redoc`

---

## 🌐 API Endpoints

### **GET /movie**
Retrieve a list of all movies.

- **Response**: 
  - Status: `200 OK`
  - Body: List of movie objects (ID, movie title, director, release date)

```json
[
  {
    "id": "01",
    "movie_title": "RRR",
    "Director": "SS Rajamouli",
    "Release_date": "2024-09-10"
  }
]
```

### **POST /movie**
Add a new movie to the database.

- **Request Body**:
```json
{
  "movie_title": "Inception",
  "Director": "Christopher Nolan",
  "Release_date": "2010-07-16"
}
```

- **Response**: 
  - Status: `200 OK`
  - Body: The newly added movie object (ID, movie title, director, release date)

```json
{
  "id": "02",
  "movie_title": "Inception",
  "Director": "Christopher Nolan",
  "Release_date": "2010-07-16"
}
```

---

## 🧑‍💻 Usage Examples

### Retrieve All Movies
You can retrieve all available movies by sending a **GET** request to the `/movie` endpoint.

```bash
curl -X 'GET' \
  'http://127.0.0.1:8000/movie' \
  -H 'accept: application/json'
```

### Add a New Movie
You can add a new movie by sending a **POST** request to the `/movie` endpoint with the following JSON body:

```bash
curl -X 'POST' \
  'http://127.0.0.1:8000/movie' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "movie_title": "Inception",
    "Director": "Christopher Nolan",
    "Release_date": "2010-07-16"
  }'
```

---

## 🛠️ Contributing

If you'd like to contribute to this project, follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/AmazingFeature`).
3. Make your changes and commit them (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

---


Feel free to reach out if you have any questions or suggestions for improving this project!

---