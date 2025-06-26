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

[cite_start]Food wastage is a significant global issue, particularly in urban areas where restaurants and events often have surplus edible food[cite: 1]. [cite_start]Simultaneously, many individuals and communities face food insecurity and hunger[cite: 2].

[cite_start]This project introduces an **AI-Powered Food Redistribution System**, a digital platform that serves as a bridge between food donors (Senders) and receivers like NGOs or shelters (Receivers)[cite: 3]. [cite_start]Our goal is to redistribute surplus food smartly and efficiently, minimizing waste and supporting sustainable food management[cite: 4, 7].

## ✨ Key Features

* [cite_start]**Separate Dashboards:** Dedicated login and dashboard interfaces for both Senders and Receivers[cite: 15].
* [cite_start]**Food Donation Listings:** Senders can easily upload details of surplus food, including type, quantity, shelf life, and optional images[cite: 5, 10].
* [cite_start]**Real-Time Notifications:** Receivers are instantly notified about new, nearby food donations via email (SMTP)[cite: 6, 25, 26].
* [cite_start]**AI-Powered Matching:** An intelligent engine matches donations with the most suitable receivers based on location, food type, and preferences[cite: 7, 21].
* [cite_start]**Image Analysis:** A lightweight AI model assesses uploaded images to check for food freshness[cite: 12, 20].
* [cite_start]**Feedback System:** A simple rating and review system allows receivers to provide feedback on donations[cite: 11, 15].
* [cite_start]**Admin Analytics:** An administrative overview panel for tracking all platform activity and generating data analytics[cite: 15].

## 🧠 Why an AI-Powered System?

[cite_start]The integration of Artificial Intelligence elevates the platform's efficiency and effectiveness[cite: 12]:

* **Smart Matching:** Our AI recommends the best receivers for a donation by analyzing historical data, location, and food preferences. [cite_start]We use a `RandomForestRegressor` model from Scikit-learn for this task[cite: 12, 33].
* [cite_start]**Demand Prediction:** The system uses a **Prophet** model to forecast areas that will have a high demand for food at specific times, allowing for proactive planning[cite: 13, 33].
* [cite_start]**Anomaly Detection:** AI helps maintain platform integrity by detecting fraudulent activities or unusual user behavior, such as repeated cancellations, using threshold-based checks[cite: 14, 22, 33].
* [cite_start]**Image Classification:** A Convolutional Neural Network (CNN) provides a preliminary check on whether an uploaded food image appears fresh or spoiled[cite: 12, 20].

## 🏗️ System Architecture

The platform is built on a modular, layered architecture, ensuring scalability and maintainability. [cite_start]Each component functions independently while working together to match donors and recipients seamlessly[cite: 16].

<p align="center">
  <img src="https://i.imgur.com/k9a4s2P.png" alt="System Architecture Diagram" width="700"/>
</p>

* **Presentation Layer (Frontend):** A dynamic and responsive user interface built with **React.js**. [cite_start]It handles user registration, login, food upload forms, and donation Browse[cite: 17, 18].
* **Application Layer (Backend):** The core logic is powered by **Django**. [cite_start]It manages user sessions, REST APIs, and business logic, and communicates with the AI engine[cite: 19].
* [cite_start]**AI/ML Engine:** This layer houses our intelligent models for matching, prediction, and detection[cite: 20, 21, 22].
* **Data Layer:** Securely stores all platform data, including user profiles, donations, and ratings, using a **MySQL** database. [cite_start]Food images are managed via cloud or local file storage[cite: 23, 24, 31].
* [cite_start]**Notification Layer:** Handles all user communications, sending real-time alerts about new donations via **SMTP Email**[cite: 25, 26].

## 💻 Technology Stack

| Component | Technology / Library |
| :--- | :--- |
| **Backend** | [cite_start]`Django`, `Django REST Framework` [cite: 29] |
| **Frontend** | [cite_start]`React.js`, `JavaScript`, `HTML5`, `CSS3` [cite: 29] |
| **Database** | [cite_start]`MySQL` [cite: 31] |
| **AI / ML** | [cite_start]`Scikit-learn`, `Prophet`, `Pandas`, `OpenCV` [cite: 33] |
| **Notifications** | [cite_start]`SMTP` (via Django) [cite: 26] |
| **Image Storage** | [cite_start]`Cloudinary` / `AWS S3` [cite: 31] |

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

* **Sender (Donor):** An individual or organization with surplus food. [cite_start]Responsibilities include uploading food details (type, quantity, expiry), waiting for confirmation, and handing over the food[cite: 9, 10].
* **Receiver (Acceptor):** An NGO, shelter, or person in need. [cite_start]Responsibilities include Browse and selecting donations, scheduling pickup, and providing feedback after collection[cite: 11].

## 📄 License

Distributed under the MIT License. See `LICENSE.txt` for more information.

---
