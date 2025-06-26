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

## 🌟 Introduction

Food wastage is a significant global issue, particularly in urban areas where restaurants and events often have surplus edible food.Simultaneously, many individuals and communities face food insecurity and hunger.

This project introduces an **AI-Powered Food Redistribution System**, a digital platform that serves as a bridge between food donors (Senders) and receivers like NGOs or shelters (Receivers).Our goal is to redistribute surplus food smartly and efficiently, minimizing waste and supporting sustainable food management.

## ✨ Key Features

* **Separate Dashboards:** Dedicated login and dashboard interfaces for both Senders and Receivers.
* **Food Donation Listings:** Senders can easily upload details of surplus food, including type, quantity, shelf life, and optional images.
* **Real-Time Notifications:** Receivers are instantly notified about new, nearby food donations via email (SMTP).
* **AI-Powered Matching:** An intelligent engine matches donations with the most suitable receivers based on location, food type, and preferences.
* **Image Analysis:** A lightweight AI model assesses uploaded images to check for food freshness.
* **Feedback System:** A simple rating and review system allows receivers to provide feedback on donations.
* **Admin Analytics:** An administrative overview panel for tracking all platform activity and generating data analytics.

## 🧠 Why an AI-Powered System?

The integration of Artificial Intelligence elevates the platform's efficiency and effectiveness:

* **Smart Matching:** Our AI recommends the best receivers for a donation by analyzing historical data, location, and food preferences.We use a `RandomForestRegressor` model from Scikit-learn for this task.
* **Demand Prediction:** The system uses a **Prophet** model to forecast areas that will have a high demand for food at specific times, allowing for proactive planning.
* **Anomaly Detection:** AI helps maintain platform integrity by detecting fraudulent activities or unusual user behavior, such as repeated cancellations, using threshold-based checks.
* **Image Classification:** A Convolutional Neural Network (CNN) provides a preliminary check on whether an uploaded food image appears fresh or spoiled.

## 🏗️ System Architecture

The platform is built on a modular, layered architecture, ensuring scalability and maintainability.Each component functions independently while working together to match donors and recipients seamlessly.

<p align="center">
  <img src="https://i.imgur.com/k9a4s2P.png" alt="System Architecture Diagram" width="700"/>
</p>

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
