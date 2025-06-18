# Uber App

A full-stack ride hailing application inspired by Uber, supporting user and driver (captain) accounts, real-time ride requests, fare calculation, and map-based location services.

---

## Table of Contents

- [Features](#features)
- [Architecture](#architecture)
- [Getting Started](#getting-started)
- [API Endpoints](#api-endpoints)
- [File Structure](#file-structure)
- [License](#license)

---

## Features

- **User and Driver (Captain) Authentication**
  - Register, login, logout, and profile management for both users and captains
  - JWT-based authentication for security

- **Ride Management**
  - Book rides, get fare estimates, and manage ride statuses
  - OTP-based ride verification

- **Mapping Services**
  - Address autocomplete and suggestions
  - Coordinate retrieval and distance/time calculation between locations

- **Modern Frontend**
  - Built with React and Vite for fast, modern UI/UX

---

## Architecture

- **Frontend:**  
  - React.js (with Vite for rapid development and build)
  - Located in the `/frontend` directory

- **Backend:**
  - RESTful API (detailed documentation in `/Backend/README.md`)
  - Handles authentication, ride logic, mapping, and more
  - Located in the `/Backend` directory

---

## Getting Started

### Prerequisites

- Node.js (v16+ recommended)
- npm or yarn

### Setup

#### 1. Clone the repository

```bash
git clone https://github.com/Aadi1909/uber-app.git
cd uber-app
```

#### 2. Install dependencies

```bash
# Frontend
cd frontend
npm install

# Backend
cd ../Backend
npm install
```

#### 3. Run the app

- **Frontend:**
  ```bash
  npm run dev
  ```
  Visit [http://localhost:5173](http://localhost:5173) (or the port shown in your terminal).

- **Backend:**
  ```bash
  npm start
  ```
  Backend API usually runs on [http://localhost:3000](http://localhost:3000).

---

## API Endpoints

The backend provides a comprehensive REST API for users, captains, rides, and maps.  
**See [`Backend/README.md`](Backend/README.md) for detailed usage and examples.**

### Example Endpoints

- `/users/register` & `/users/login`: User registration and login
- `/captains/register` & `/captains/login`: Captain registration and login
- `/rides/create`: Create a new ride (requires authentication)
- `/rides/get-fare`: Get fare estimates
- `/maps/get-coordinates`, `/maps/get-distance-time`: Map and location utilities

---

## File Structure

```
uber-app/
├── Backend/            # Express.js (Node) backend API
│   └── README.md       # Full API documentation
├── frontend/           # React + Vite frontend
│   └── README.md       # Frontend tooling details
└── README.md           # (You are here)
```

---

## License

MIT

---

*For questions or contributions, please open an issue or submit a pull request!*
