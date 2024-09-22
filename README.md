# GoGetaway Project

GoGetaway is a smart trip planning platform that allows users to plan their trips, book transportation, and explore destinations effortlessly. This project uses **React.js** for the frontend with **Firebase** for authentication, and **Flask** for the backend.

---

## Table of Contents

- [Features](#features)
- [Technologies](#technologies)
- [Setup Instructions](#setup-instructions)
- [Frontend Setup](#frontend-setup)
- [Backend Setup](#backend-setup)
- [Running the Project](#running-the-project)
- [Troubleshooting](#troubleshooting)

---

## Features

- Firebase-based user authentication (login, signup)
- Smart trip planning and itinerary creation
- Real-time transportation booking and suggestions
- Flask backend for trip data management
- Google OAuth integration

---

## Technologies

### Frontend:
- React.js
- Firebase (Authentication)
- Axios (API requests)

### Backend:
- Flask (Python)
- Flask-CORS (Cross-Origin Resource Sharing)
- Flask-RESTful (REST API support)
- SQLite or any database for data storage

---

## Setup Instructions

### Prerequisites

- **Node.js** (version 14 or higher)
- **npm** or **yarn** (package managers for Node.js)
- **Python** (version 3.7 or higher)
- **Firebase** account and project
- **Flask** and Flask dependencies

---

## Frontend Setup

1. **Navigate to the frontend directory:**

    ```bash
    cd frontend
    ```

2. **Install Node.js modules:**

    Install the required packages for the React frontend:

    ```bash
    npm install
    ```

    Alternatively, using yarn:

    ```bash
    yarn install
    ```

3. **Install additional required modules:**

    - **Firebase**: For authentication and cloud services:

      ```bash
      npm install firebase
      ```

    - **Axios**: For making HTTP requests to the Flask backend:

      ```bash
      npm install axios
      ```

    - **React Router DOM**: For routing in React:

      ```bash
      npm install react-router-dom
      ```

4. **Firebase Configuration:**

    - Go to the [Firebase Console](https://console.firebase.google.com/), create a new project, and enable Authentication (choose Email/Password or Google OAuth).
    - After creating the project, generate Firebase SDK configuration and copy it.
    - Create a `.env` file in the `frontend` directory and add your Firebase configuration:

    ```env
    REACT_APP_FIREBASE_API_KEY=your_firebase_api_key
    REACT_APP_FIREBASE_AUTH_DOMAIN=your_project_id.firebaseapp.com
    REACT_APP_FIREBASE_PROJECT_ID=your_project_id
    REACT_APP_FIREBASE_STORAGE_BUCKET=your_project_id.appspot.com
    REACT_APP_FIREBASE_MESSAGING_SENDER_ID=your_messaging_sender_id
    REACT_APP_FIREBASE_APP_ID=your_firebase_app_id
    ```

---

## Backend Setup

1. **Navigate to the backend directory:**

    ```bash
    cd backend
    ```

2. **Create a virtual environment:**

    ```bash
    python -m venv venv
    ```

3. **Activate the virtual environment:**

    - On macOS/Linux:

      ```bash
      source venv/bin/activate
      ```

    - On Windows:

      ```bash
      venv\Scripts\activate
      ```

4. **Install Flask and required dependencies:**

    ```bash
    pip install Flask Flask-CORS Flask-RESTful
    ```

5. **Set up the Flask environment:**

    - Create a `.env` file in the backend directory and add any necessary configurations (such as database URL or secret keys).
    
6. **Create the Flask backend structure:**

    - Create necessary Python files, such as:

      ```bash
      ├── app.py          # Main Flask application
      ├── models.py       # Database models
      ├── routes.py       # API routes
      ├── requirements.txt # Dependencies file
      ```

7. **Add CORS (Cross-Origin Resource Sharing) support:**

    In `app.py`:

    ```python
    from flask import Flask
    from flask_cors import CORS

    app = Flask(__name__)
    CORS(app)
    ```

8. **Install and update dependencies:**

    - If additional modules are needed (e.g., SQLAlchemy for database):

    ```bash
    pip install <package_name>
    ```

    - Update `requirements.txt` with:

    ```bash
    pip freeze > requirements.txt
    ```

---

## Running the Project

### Start the Backend:

1. **Navigate to the backend directory:**

    ```bash
    cd backend
    ```

2. **Run Flask server:**

    ```bash
    python app.py
    ```

    The backend server will be running on `http://127.0.0.1:5000/`.

### Start the Frontend:

1. **Navigate to the frontend directory:**

    ```bash
    cd frontend
    ```

2. **Start the React development server:**

    ```bash
    npm start
    ```

    The frontend server will be running on `http://localhost:3000/`.

---

## Troubleshooting

- **CORS Issues:** Ensure that Flask-CORS is enabled in the backend to avoid cross-origin errors when connecting to the frontend.
- **Firebase Errors:** Double-check the Firebase project settings and `.env` file for any incorrect configurations.
- **Database Issues:** If using a database, ensure all necessary migrations are done and the database is properly configured.

---

## License

This project is licensed under the MIT License. You are free to modify and use it as needed.

