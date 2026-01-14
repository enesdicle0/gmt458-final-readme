# gmt458-final-readme
GMT458 Final Project — Full-Stack Web GIS (Cesium Game)
This repository contains only the README.md for peer-review access (no source code shared publicly).
Project code is hosted in my GitHub Classroom private repository.

Project Summary
A Web GIS mini-game built with CesiumJS on the frontend and a Node.js (Express) backend.
Players guess locations on a 3D globe/map, earn points based on distance, and the system supports basic user/login flows and server-side monitoring.

Implemented Items (Chosen Features)
✅ 1) Managing Different User Types (Bonus)
A Login/Register screen (login.html, login.js)
Users select a role during register:
scout
commander
sultan
Basic login control using localStorage (token/username/role).
✅ 2) Performance Monitoring / Server Logging (Bonus)
Server-side request logging using Morgan
Logs written to file:
backend/logs/access.log
Logs also printed to terminal (morgan("dev"))
✅ 3) Backend API Integration
Frontend consumes backend API endpoint(s)
Example GeoJSON endpoint for testing:
GET /api/pois
✅ 4) Frontend Web GIS + Interaction
CesiumJS viewer
UI flow includes intro/menu/game screens
Player actions update score and timers in real-time
Tech Stack
Frontend

HTML / CSS / JavaScript
CesiumJS
Backend

Node.js
Express.js
Morgan (logging)
CORS
How to Run (Local)
1) Backend
cd backend
npm install
npm run dev
