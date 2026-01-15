# GMT458 Final Project – Full-Stack Web GIS (GeoGame Extension)

This repository contains the public README-only description of my GMT458 – Web GIS final project. The project extends the previously developed GeoGame into a Full-Stack Web GIS application by integrating backend services, authentication, logging, and persistent storage.

The application is deployed on Amazon Web Services (AWS) using an EC2 instance and is publicly accessible via Apache HTTP Server.

Live Application URL:
http://3.121.201.89

If the page does not load due to browser caching, try:
http://3.121.201.89/?v=1

---

Project Description

This project demonstrates how a Web GIS application can be transformed into a full-stack system. A static Web GIS frontend is combined with a backend REST API to support user authentication, role management, score submission, and data persistence. The application follows a game-based GIS concept where users interact with spatial data and submit scores.

---

Implemented Features (Final Project)

Managing Different User Types
- Scout (Player): Can register, log in, play the game, and submit scores.
- Commander: Planned / Optional (not fully implemented).
- Sultan (Admin): Planned / Optional (not fully implemented).
User roles are assigned during registration and stored in the backend.

Authentication and Authorization
- User registration and login are implemented.
- Token-based session handling is used.
- Only authenticated users can access gameplay and submit scores.

CRUD Operations
- Create: Users are created during registration; scores are created when a game session ends.
- Read: Users and scores can be retrieved via API endpoints.
- Update and Delete operations are limited due to project scope.

Backend API Development
A RESTful backend API is implemented using Node.js and Express.

Available endpoints:
- POST /auth/register
- POST /auth/login
- POST /api/score
- GET /api/scores

Logging
- HTTP request logging is implemented using Morgan.
- All incoming requests are recorded in an access log file located at:
  backend/logs/access.log

NoSQL / File-Based Database
- A lightweight JSON-based storage approach is used.
- users.json stores registered users.
- scores.json stores submitted game scores.
- These files act as a simple NoSQL-style persistence layer for the project.

---

Deployment Details (AWS)

Cloud Provider: Amazon Web Services (AWS)
Service: EC2
Operating System: Amazon Linux 2023
Web Server: Apache HTTP Server (httpd)
Protocol: HTTP (Port 80)

The frontend is deployed as a static website under Apache’s DocumentRoot directory. The default Apache welcome page was disabled to ensure that the custom application content is served correctly. EC2 Security Group rules were configured to allow inbound HTTP traffic on port 80 and SSH access for server management.

---

Project Structure (High-Level)

full-stack-web-gis-enesdicle0/
├── backend/
│   ├── logs/
│   │   └── access.log
│   ├── users.json
│   ├── scores.json
│   └── server files
├── frontend/
│   ├── index.html
│   ├── game.js
│   ├── style.css
│   ├── images/
│   ├── sounds/
│   ├── coordinates.csv
│   └── teams.geojson
└── README.md

Only this README is published publicly for peer-review. The full source code is available in the private GitHub Classroom repository.

---

Author

Enes Dicle  
GMT458 – Web GIS  
Hacettepe University
