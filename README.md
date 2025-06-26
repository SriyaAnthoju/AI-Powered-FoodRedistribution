# 🤖 AI-Powered Food Redistribution System

<p align="center">
  An intelligent web platform designed to combat food waste and hunger by connecting food donors with those in need through a smart, efficient, and automated system.
</p>

<p align="center">
  <img alt="Status" src="https://img.shields.io/badge/status-in%20progress-yellow">
  <img alt="Python" src="https://img.shields.io/badge/Python-3.8%2B-blue?logo=python">
  <img alt="Django" src="https://img.shields.io/badge/Django-4.x-green?logo=django">
  <img alt="React" src="https://img.shields.io/badge/React-18.x-blue?logo=react">
  <img alt="MySQL" src="https://img.shields.io/badge/MySQL-8.x-orange?logo=mysql">
</p>

---

##  Introduction

Food wastage is a significant global issue, particularly in urban areas where restaurants and events often have surplus edible food.Simultaneously, many individuals and communities face food insecurity and hunger.

This project introduces an **AI-Powered Food Redistribution System**, a digital platform that serves as a bridge between food donors (Senders) and receivers like NGOs or shelters (Receivers).Our goal is to redistribute surplus food smartly and efficiently, minimizing waste and supporting sustainable food management.

## ✨ Key Features

### 🧑‍💻 Role-Based Authentication
* Separate login and dashboards for:
    * **Senders (Food Donors):** Restaurants, caterers, and individuals with surplus food.
    * **Receivers (NGOs, Shelters, Volunteers):** Those looking to accept donations.

### 🍱 Food Donation & Claiming System
* Donors can upload details of available food: type, quantity, shelf life, and optional images.
* Receivers can browse and claim available donations.
* Once claimed, the donor receives confirmation for the handover.

### 🤖 AI-Powered Features
* **Smart Matching Engine:** Suggests the best donors for each receiver based on geographic proximity, food type, and historical preferences.
* **Demand Prediction:** Uses a Prophet model to forecast areas likely to need food and identify peak demand times.
* **Anomaly Detection:** Monitors system behavior to detect fake entries, suspicious cancellations, or platform abuse.

### ⏰ System Automation with Celery
* **Automated AI Model Retraining:** The demand prediction models are automatically retrained every day at midnight, ensuring the AI stays up-to-date with the latest data.
* **Scheduled Reminders:** The system automatically sends periodic email reminders for donation pickups and for leaving feedback, managed entirely in the background.

### 🗣 Feedback and Review System
* After a donation is picked up, receivers can leave reviews and ratings to encourage trust and transparency.

### 📊 Admin Dashboard
* Admins can view all users, donations, claims, and analytics, providing insights into platform activity.

### 🔐 Secure & Modular Architecture
* Features secure **JWT-based authentication** for the API.
* Built with RESTful APIs, enabling a scalable, microservices-style development approach.

## 🏗️ System Architecture

The platform is built on a modular, layered architecture, ensuring scalability and maintainability. It uses a task queue (Celery & Redis) to offload heavy processes from the main application thread, resulting in a faster user experience.

<p align="center">
  <img src="https://i.imgur.com/k9a4s2P.png" alt="System Architecture Diagram" width="700"/>
</p>


##  System Architecture

The platform is built on a modular, layered architecture, ensuring scalability and maintainability.Each component functions independently while working together to match donors and recipients seamlessly.

* **Presentation Layer (Frontend):** A dynamic and responsive user interface built with **React.js**. It handles user registration, login, food upload forms, and donation Browse.
* **Application Layer (Backend):** The core logic is powered by **Django**.It manages user sessions, REST APIs, and business logic, and communicates with the AI engine.
* **AI/ML Engine:** This layer houses our intelligent models for matching, prediction, and detection.
* **Data Layer:** Securely stores all platform data, including user profiles, donations, and ratings, using a **MySQL** database.Food images are managed via cloud or local file storage.
* **Notification Layer:** Handles all user communications, sending real-time alerts about new donations via **SMTP Email**.

## 💻 Technology Stack

| Component | Technology / Library |
| :--- | :--- |
| **Backend** | `Django`, `Django REST Framework`, `Celery` |
| **Frontend** | `React.js`, `JavaScript`, `HTML5`, `CSS3` |
| **Database** | `MySQL` |
| **Task Queue** | `Redis` (Broker), `django-celery-beat` (Scheduler)|
| **AI / ML** | `Scikit-learn`, `Prophet`, `Pandas`, `OpenCV` |
| **Authentication**| `Simple-JWT` |
| **Notifications** | `SMTP` (via Django) |
| **Image Storage** | `Local Storage` |

## 🚀 Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

* Python 3.8+
* Node.js and npm
* MySQL Server

### Installation

1.  **Clone the repo**
    ```sh
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    cd your-repo-name
    ```
2.  **Backend Setup**
    ```sh
    # Navigate to backend directory
    cd backend
    # Create a virtual environment and install dependencies
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    pip install -r requirements.txt
    # Set up your .env file with database credentials
    # Run database migrations and start the server
    python manage.py migrate
    python manage.py runserver
    ```
3.  **Frontend Setup**
    ```sh
    # Navigate to frontend directory
    cd frontend
    # Install NPM packages
    npm install
    # Start the development server
    npm start
    ```

## 👥 Key Roles

* **Sender (Donor):** An individual or organization with surplus food.Responsibilities include uploading food details (type, quantity, expiry), waiting for confirmation, and handing over the food.
* **Receiver (Acceptor):** An NGO, shelter, or person in need.Responsibilities include Browse and selecting donations, scheduling pickup, and providing feedback after collection.

## 📄 License

Distributed under the MIT License. See `LICENSE.txt` for more information.

---
