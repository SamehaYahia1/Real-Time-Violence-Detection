# 🎯Real-Time Violence Detection Backend (Graduation Project)
> Backend API for an intelligent real-time violence detection system — integrating AI video analysis, live notifications, and user management.

# 🧠 About The Project 
This project is part of my B.Sc. Graduation Project, built in collaboration with a team developing an AI-powered system to detect violent actions from live camera streams in real time.
The backend (this repository) was built using ASP.NET Core and acts as the central controller for the entire system — connecting the Flutter mobile app, AI microservices, and storage infrastructure.

My main focus areas included:

*   **Real-Time Data Pipeline:** Ingests live video streams and processes them into chunks for AI analysis using RabbitMQ and MinIO.

*   **Real-Time Notifications:** Instantly notifies users when a violent incident is identified.
*   **Microservice Architecture:** Uses separate containerized services for easier updates and scalable deployment.
*   **Camera Stream Coordination**: Handles camera streaming endpoints and synchronizes detected events from the AI services in real time.

## 🧰 Tech Stack

| 🧩 Component | ⚙️ Technology |
|--------------|----------------|
| **Backend Framework** | ASP.NET Core (C#) |
| **Database** | SQL Server |
| **Message Queue** | RabbitMQ |
| **Object Storage** | MinIO |
| **AI Integration** | Python Flask Services |
| **Client App** | Flutter |
| **Notifications** | Firebase Cloud Messaging (FCM) |
| **Containerization** | Docker |

## 📂 Project Repositories

This system is divided into **three main repositories**, each responsible for a specific part of the real-time violence detection workflow.  
All three should be set up to run the complete system properly.

### 🧱 1. Backend API — [`Real-Time-Violence-Detection-Backend`](https://github.com/SamehaYahia1/Real-Time-Violence-Detection)
Contains the **ASP.NET Core API**, handling authentication, user subscriptions, camera management, notifications, and communication with the AI microservices.

### 🤖 2. AI Microservices — [`Violence-Detection-AI-Services`](https://github.com/SamehaYahia1/Real-Time-Violence-Detection-Microservices)
Includes the **Python-based containerized AI services** responsible for video processing and real-time violence detection. These services interact with the backend through REST and message queues.

### 📱 3. Mobile Application — [`Real-Time-Violence-Detection-App`](https://github.com/SamehaYahia1/Real-Time-Violence-Detection-App)
A **Flutter-based client application** that allows users to log in, manage their cameras, view live streams, and receive instant alerts when violent actions are detected.

## Getting Started

To get a local copy up and running, follow these steps.

### Prerequisites

*   Docker and Docker Compose
*   .NET 8 SDK
*   Python 3.10

### Installation & Launch

1.  **Clone Both Repositories:** The system requires both the API and the AI services. It is recommended to clone them into the same parent directory.
    ```sh
    # Clone the Backend API (this repo)
    git clone https://github.com/SamehaYahia1/Real-Time-Violence-Detection.git

    # Clone the AI Microservices
    git clone https://github.com/SamehaYahia1/VdectDockerContainers.git
    ```
2.  **Configure Environment Variables:**
    *   Navigate into the `Real-Time-Violence-Detection` directory.
    *   Create a `.env` file by copying the provided `.env.example` file.
    *   Update the variables in the new `.env` file with your local configuration.
3.  **Launch the System with Docker Compose:**
    *   From the root of the `Real-Time-Violence-Detection-API` directory (where the `docker-compose.yml` file is located):
    ```sh
    docker-compose up --build
    ```
---



