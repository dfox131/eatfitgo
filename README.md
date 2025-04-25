# EatFitGo 🥗🏃‍♂️

EatFitGo is a full-stack fitness and diet recommendation mobile app built with the MERN stack. It helps users track their daily steps, monitor calories burned, and receive personalized diet suggestions based on their physical activity.

## 🚀 Features

- 🔐 User Authentication via email and OAuth
- 📊 Real-time step tracking with distance and calorie estimation
- 🥗 Dynamic diet suggestions based on steps and calories burned
- 👤 User profile and fitness goal configuration
- 🔔 Push and email notifications for health reminders
- 🧠 Microservices architecture for scalability and modularity

## 🧱 Tech Stack

- **Frontend:** React Native
- **Backend:** Node.js + Express
- **Database:** MongoDB
- **Architecture:** Microservices (5 services)
- **Authentication:** OAuth + JWT
- **Notifications:** Push notifications + Email

## 🧩 Microservices Overview

| Service                 | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| **Authentication**      | Handles signup, login, and token-based auth                  |
| **Profile**             | Manages user info, goals, height, weight, and preferences    |
| **Step Tracking**       | Collects and analyzes step data, distance, and calories      |
| **Diet Recommendation** | Generates personalized meal suggestions from a large dataset |
| **Notification**        | Sends push and email notifications to keep users on track    |

Each service runs independently and communicates via RESTful API calls.

## 📐 System Architecture

All microservices are containerized and communicate through REST APIs. MongoDB is used across services with independent collections. Authentication uses JWT for token-based access control. The architecture allows future integration with third-party health and nutrition APIs.

## 📡 API Endpoints

- `POST /auth/register` – Register new user
- `POST /auth/login` – Login and receive token
- `GET /steps/:userId` – Fetch step data
- `POST /diet/suggest` – Get meal plan based on calories burned
- `POST /notify/reminder` – Send a health notification

## 🔒 Security

- JWT-based authentication
- OAuth support for Google sign-in
- Passwords hashed using bcrypt
- HTTPS enforced in production

## 📈 Scalability & Performance

- Stateless services behind a load balancer
- MongoDB sharded collections for large datasets
- Caching strategy under consideration for frequent diet queries

## 👨‍👩‍👧‍👦 User Roles

| Role  | Permissions                         |
| ----- | ----------------------------------- |
| Guest | View public data, register          |
| User  | Full app access (profile, tracking) |
| Admin | Manage users, monitor usage         |

## 📬 Contact & Team

> Created as part of a graduate software engineering project at Pace University.

Team Members:

- Daniel Fox
- Cristian Bolanos
- Manohar Killamsetti
- Kiran Rathod
- Aakash Varma
