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

##  Key Features

### 🧑‍💻 Role-Based Authentication
* Separate login and dashboards for:
    * **Senders (Food Donors):** Restaurants, caterers, and individuals with surplus food.
    * **Receivers (NGOs, Shelters, Volunteers):** Those looking to accept donations.

### 🍱 Food Donation & Claiming System
* Donors can upload details of available food: type, quantity, shelf life, and optional images.
* Receivers can browse and claim available donations.
* Once claimed, the donor receives confirmation for the handover.

### 📬 Real-Time Email Notifications
* All receivers get notified via email when new donations are posted.
* This helps ensure quick claiming and reduces food spoilage.

### 🤖 AI-Powered Features
* **Smart Matching Engine:** Suggests the best donors for each receiver based on geographic proximity, food type, quantity, and historical claim behavior.
* **Demand Prediction:** Learns from past data to forecast which areas are likely to need food and identify peak demand times.
* **Anomaly Detection:** Monitors system behavior to detect fake entries, suspicious cancellations, or abuse of the platform.

### 🗣 Feedback and Review System
* After a donation is picked up, receivers can leave reviews and ratings to encourage trust and transparency.

### 📊 Admin Dashboard
* Admins can view all users, donations, claims, and analytics.
* Provides insights into which locations have high donation frequency or unclaimed listings.

### 🔐 Secure & Modular Architecture
* Features JWT-based authentication for security.
* Built with RESTful APIs, enabling a scalable, microservices-style development approach.


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
| **Backend** | `Django`, `Django REST Framework` |
| **Frontend** | `React.js`, `JavaScript`, `HTML5`, `CSS3` |
| **Database** | `MySQL` |
| **AI / ML** | `Scikit-learn`, `Prophet`, `Pandas`, `OpenCV` |
| **Notifications** | `SMTP` (via Django)|
| **Image Storage** | `Cloudinary` / `AWS S3` |

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
