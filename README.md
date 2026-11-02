AI-Based Green Smart Traffic Management System
1. Project Overview

The AI-Based Green Smart Traffic Management System is an intelligent traffic management solution designed to optimize traffic signal operations dynamically based on vehicle density, vehicle count, waiting time, and emergency vehicle priority.

The system aims to improve traffic flow, reduce unnecessary waiting time, and provide efficient traffic signal management through AI-based vehicle detection, adaptive signal control, and hardware integration.

Key Features
AI-based vehicle detection and counting.
Dynamic traffic signal management.
Traffic density-based signal prioritization.
Adaptive green-light duration.
Emergency vehicle priority.
Real-time traffic monitoring dashboard.
ESP32-based traffic light control.
Traffic history and analytics.
2. System Architecture

The system consists of the following major components:

Frontend: Web-based dashboard for traffic monitoring and signal interaction.
Backend: FastAPI application for processing traffic data and managing signal decisions.
AI Module: Vehicle detection and traffic density analysis using OpenCV and YOLO.
Database: SQLite for storing traffic information and signal history.
Hardware: ESP32-based traffic light controller.
3. Technologies Used
Programming Languages
Python
JavaScript
Frontend
React
HTML
CSS
Backend
FastAPI
Uvicorn
SQLAlchemy
Pydantic
Database
SQLite
AI and Computer Vision
OpenCV
YOLO
Hardware
ESP32
Traffic Light Control Components
4. Frontend Development

The frontend provides a web-based interface for monitoring and interacting with the smart traffic management system.

Frontend Responsibilities
Designed and developed the complete web interface.
Created the traffic monitoring dashboard.
Implemented frontend components for displaying traffic information.
Developed the user interface for traffic signal monitoring and interaction.
Worked on connecting the frontend interface with the traffic light functionality.
Focused on usability and clear presentation of traffic information.
5. Backend Development

The backend is developed using FastAPI.

It receives traffic information from the AI module and calculates:

Traffic priority.
Green-light duration.
Emergency vehicle priority.
Current signal status.
Traffic history.
Traffic analytics.
6. Backend APIs
Method	Endpoint	Purpose
GET	/	Check backend
GET	/health	Check backend health
POST	/traffic	Receive traffic data and calculate signal
GET	/signal-status	Get current signal status
POST	/manual-override	Manually control a signal
GET	/traffic-history	View stored traffic records
GET	/analytics	View traffic analytics
7. Adaptive Signal Logic

The backend calculates a priority score using:

Priority Score = Density × 0.7 + Waiting Time × 0.3

The green-light duration is limited between:

Minimum: 15 seconds
Maximum: 60 seconds

If an emergency vehicle is detected, that direction receives priority.

8. Database Management

Traffic information and signal decisions are stored using SQLite.

The database contains:

Vehicle counts.
Traffic density.
Waiting time.
Emergency vehicle status.
Priority direction.
Green-light duration.
Timestamp.
9. Hardware Integration

The hardware component uses ESP32 for traffic light control.

Hardware Responsibilities
ESP32-based hardware integration.
Traffic light control implementation.
Hardware-side signal operations.
Integration of hardware components with the traffic management system.
10. Team Members and Contributions

This project was developed collaboratively by a team of three members, with responsibilities divided across frontend development, backend development, and hardware integration.

1. Frontend Development – [Samruddhi Misale]
Developed the complete frontend of the web application.
Designed and implemented the traffic monitoring dashboard.
Developed the user interface and frontend functionality.
Worked on connecting the frontend interface with the traffic light functionality.
Contributed to the overall system integration.
2. Backend Development and Integration – Sneha
Developed the backend using Python and FastAPI.
Implemented backend APIs and traffic management logic.
Worked on frontend-backend integration.
Handled communication between the frontend and backend.
3. Hardware Integration – Ishita
Worked on ESP32 hardware integration.
Implemented hardware-side traffic light connections.
Contributed to the integration of traffic light hardware with the system.
11. Team Collaboration
Collaborated on the planning and development of the project.
Divided responsibilities across frontend, backend, and hardware components.
Coordinated the integration of different system modules.
Worked together on testing, debugging, and problem-solving.
Contributed to developing an integrated smart traffic management solution.
12. Running the Backend
Step 1: Activate the Virtual Environment

From the project root:

bash
source venv/bin/activate

Step 2: Install Dependencies
bash
pip install -r requirements.txt

Step 3: Start the Backend
bash
uvicorn main:app --reload

Step 4: Access API Documentation

Open the following URL in your browser:

text
http://127.0.0.1:8000/docs

13. Project Outcomes
Developed a web-based traffic monitoring interface.
Implemented backend-driven adaptive traffic management.
Integrated AI-based vehicle detection concepts.
Worked with ESP32-based traffic light hardware.
Gained practical experience in frontend development, backend integration, and hardware-based system development.
Improved teamwork, communication, and collaborative problem-solving skills.
14. Learning Outcomes

Through this project, we gained practical experience in:

Frontend Web Development.
Python Backend Development.
REST API Integration.
AI and Computer Vision Fundamentals.
Database Management.
ESP32 Hardware Integration.
Team Collaboration and Project Development.

Project Type: Academic Group Project

Domain: Artificial Intelligence, Web Development, and IoT-Based Smart Traffic Management
