
# AI-Based Green Smart Traffic Management System

## Project Overview

The AI-Based Green Smart Traffic Management System is designed to manage traffic signals dynamically using traffic density, vehicle count, waiting time, and emergency vehicle priority.

The system consists of:

- AI vehicle detection
- FastAPI backend
- Adaptive traffic signal algorithm
- SQLite database
- ESP32 traffic light controller
- Dashboard for monitoring traffic information

## Backend

The backend is developed using FastAPI.

It receives traffic information from the AI module and calculates:

- Traffic priority
- Green-light duration
- Emergency vehicle priority
- Current signal status
- Traffic history
- Traffic analytics

## Technologies Used

- Python
- FastAPI
- Uvicorn
- SQLAlchemy
- SQLite
- Pydantic
- ESP32
- OpenCV
- YOLO
- React

## Backend APIs

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/` | Check backend |
| GET | `/health` | Check backend health |
| POST | `/traffic` | Receive traffic data and calculate signal |
| GET | `/signal-status` | Get current signal status |
| POST | `/manual-override` | Manually control a signal |
| GET | `/traffic-history` | View stored traffic records |
| GET | `/analytics` | View traffic analytics |

## Adaptive Signal Logic

The backend calculates a priority score using:

**Priority Score = Density × 0.7 + Waiting Time × 0.3**

The green-light duration is limited between:

- **Minimum:** 15 seconds
- **Maximum:** 60 seconds

If an emergency vehicle is detected, that direction receives priority.

## Database

Traffic information and signal decisions are stored using SQLite.

The database contains:

- Vehicle counts
- Traffic density
- Waiting time
- Emergency vehicle status
- Priority direction
- Green-light duration
- Timestamp

## Running the Backend

### 1. Activate the Virtual Environment

From the project root:

```bash
source venv/bin/activate
```

## Team Members and Contributions

### **[Samruddhi]**

**Role: Frontend Developer**

- Developed the complete frontend of the web application.
- Designed and implemented the traffic monitoring dashboard.
- Worked on connecting the frontend interface with the traffic light functionality.

### **Sneha**

**Role: Backend Developer**

- Developed the FastAPI backend.
- Implemented backend APIs and traffic management logic.
- Integrated the frontend with the backend.

### **Ishita**

**Role: Hardware Integration**

- Worked on ESP32 hardware integration.
- Connected and implemented the traffic light hardware.

## Project Type

**Academic Group Project**

## My Contribution

**Frontend Development and Traffic Light Interface Integration.**
