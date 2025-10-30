# Real-Time Violence Detection Backend (Graduation Project)
> Backend API for an intelligent real-time violence detection system — integrating AI video analysis, live notifications, and user management.
# About The Project 
This project is part of my B.Sc. Graduation Project, built in collaboration with a team developing an AI-powered system to detect violent actions from live camera streams in real time.
The backend (this repository) was built using ASP.NET Core and acts as the central controller for the entire system — connecting the Flutter mobile app, AI microservices, and storage infrastructure.

My main focus areas included:

*   **Real-Time Data Pipeline:** Ingests live video streams and processes them into chunks for AI analysis using RabbitMQ and MinIO.

*   **Real-Time Notifications:** Instantly notifies users when a violent incident is identified.
*   **Microservice Architecture:** Uses separate containerized services for easier updates and scalable deployment.   


Handling camera streaming endpoints and coordinating with AI detection results
