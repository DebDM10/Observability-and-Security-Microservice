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

---

## 🧠 Sample Output

Below is a sample `/summary` API response (for demonstration):

```json
{
  "total_alerts": 12,
  "breakdown": {"cpu": 9, "memory": 3},
  "last_alerts": [
    {
      "ts": "2025-11-04T10:45Z",
      "type": "cpu",
      "value": 91.4,
      "message": "CPU usage 91.4% > 80%"
    }
  ],
  "averages_last_10": {"cpu": 75.3, "memory": 68.9}
}

