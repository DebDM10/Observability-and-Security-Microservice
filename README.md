# Observability & Security Microservice

A FastAPI-based microservice that performs log analysis, collects system metrics, and manages secure user sessions.

## Setup
```bash
pip install -r requirements.txt
uvicorn app.main:app --reload
```

## API Endpoints
- `/register` - Register new user
- `/login` - Login and get session token
- `/summary` - Get metrics and alerts summary (token required)
