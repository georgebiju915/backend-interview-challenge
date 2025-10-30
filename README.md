# 🧩 Task Management API

## Overview
The Task Management API is a simple yet powerful backend application I built using Python and FastAPI, with SQLite as the database to store task details. It supports all the core CRUD operations — creating, reading, updating, and deleting tasks — making it easy to manage and organize task data efficiently. I developed this project as part of my journey to learn backend development hands-on, focusing on how APIs connect with databases and handle real-world operations. Throughout the process, I used ChatGPT and Google to guide me through challenges, debug errors, and learn best practices for building clean and efficient APIs. This project not only helped me improve my technical skills but also gave me valuable experience in designing and implementing a complete backend system from scratch.

---

## 🚀 Features
- RESTful API built with **FastAPI**
- SQLite database with **SQLAlchemy ORM**
- Task model with `title`, `description`, `completed`
- Offline-first design with sync endpoints
- JSON-based CRUD operations
- Unit testing using **pytest** and **FastAPI TestClient**
- Simple web UI (HTML + JS) for testing API endpoints

---

## 🧠 My Learning Experience

This project was part of my journey to explore and practice backend development. Completing it within a short time frame of just 2–3 hours was definitely challenging, but also incredibly rewarding. With the help of AI tools like ChatGPT, GitHub Copilot, and Google, I was able to navigate through the tough parts and bring the project to life.

One of the biggest challenges I faced was building the offline queue system, since the API was meant to function independently from any web or mobile application. Getting this mechanism to work properly required a lot of experimentation and creative problem-solving.

Another major hurdle was testing. The test files provided were written in TypeScript, while my entire backend was developed in Python using FastAPI. This meant I had to adapt and perform manual testing before creating my own Python-based test cases to ensure the API worked correctly.

Despite the challenges, I didn’t give up. By using tools like Google, ChatGPT, Copilot, and Gemini, I was able to debug issues, improve my code, and verify the functionality of the API. This experience helped me grow both technically and personally — teaching me how to stay persistent, learn quickly, and use modern tools effectively to solve real-world problems.

I used **ChatGPT** to:
- Generate boilerplate FastAPI code and understand API structure.
- Debug issues such as 422 and 404 errors.
- Write clear `requirements.txt`, test cases, and Pydantic schema updates.
- Learn about modern Python features like async support, dependency injection, and request validation.

I also used **Google** to:
- Search for common FastAPI and SQLAlchemy integration problems.
- Understand Python’s virtual environments and testing with pytest.
- Research deployment guides for Render and related hosting platforms.

Overall, combining **AI guidance** with **hands-on coding** helped me:
- Strengthen my understanding of REST APIs.
- Improve debugging and testing skills.
- Learn how to translate TypeScript/Node.js-style tests into Python equivalents.
- Build a real-world project end-to-end.

---

## 🧩 Tech Stack
| Category | Tools Used |
|-----------|-------------|
| Framework | FastAPI |
| Database | SQLite + SQLAlchemy |
| Validation | Pydantic |
| Testing | pytest, FastAPI TestClient |
| Environment | Python-dotenv |
| Deployment | Render (Free Tier) |
| Frontend | HTML, CSS, JavaScript (for quick API testing) |

---

# ⚙️ Setup Instructions

## 1. Project Setup

### Clone the repository
```bash
git clone https://github.com/georgebiju915/backend-interview-challenge
cd backend-interview-challenge

python -m venv .venv
.venv\Scripts\activate     # for Windows
source .venv/bin/activate

pip install -r requirements.txt

### Api Implementation
src/
├── main.py          # Entry point of the FastAPI app
├── models.py        # Database models (SQLAlchemy)
├── schemas.py       # Pydantic schemas for validation
├── database.py      # SQLite database connection
├── services.py      # Business logic for task operations
└── routes/
###  Execution
uvicorn src.main:app --reload

###  Testing
pip install httpx pytest-asyncio
pytest -v
