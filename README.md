# Food Order App

## Overview
This project is a food ordering app designed for restaurants, enabling customers to place orders through a user-friendly interface. After placing an order, the app generates an order number, which customers can use to collect their food at the counter. The system ensures a smooth ordering process with real-time communication and scalability.

## Technologies Used
- **Golang**: Backend API for order management.
- **React**: Frontend UI for customers to place orders.
- **MongoDB**: NoSQL database for storing orders and customer data.
- **RabbitMQ**: Message broker for managing real-time order processing.
- **Docker**: Containerization of the application for consistency and easy deployment.
- **Kubernetes**: Orchestration for scalable deployment and management of containers.

## Features
- **Order Placement**: Customers can select items, place their orders, and receive an order number.
- **Order Tracking**: Customers can track their orders using the generated order number.
- **Real-Time Updates**: Leveraging RabbitMQ for real-time order updates between services.
- **Scalability**: Kubernetes is used to scale the app and handle increasing traffic efficiently.
- **Database Management**: MongoDB stores customer orders and ensures fast data retrieval.

## Architecture
- **Frontend (React)**: Provides a seamless user experience for customers to browse the menu and place orders.
- **Backend (Golang)**: Handles order processing, user authentication, and order management.
- **RabbitMQ**: Facilitates communication between backend services and ensures real-time order updates.
- **MongoDB**: Stores order history, user information, and restaurant data.
- **Docker & Kubernetes**: Docker containers for microservices, with Kubernetes ensuring load balancing and auto-scaling.

## Getting Started

### Prerequisites
- [Docker](https://www.docker.com/)
- [Kubernetes](https://kubernetes.io/)
- [RabbitMQ](https://www.rabbitmq.com/)
- [MongoDB](https://www.mongodb.com/)
- [Golang](https://golang.org/)
- [Node.js](https://nodejs.org/) (for React)

### Setup Instructions
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/food-order-app.git
   cd food-order-app
   ```

2. **Run the Services Using Docker**:
   - Build and start the backend and frontend containers:
     ```bash
     docker-compose up --build
     ```

3. **Deploy with Kubernetes**:
   - Ensure your Kubernetes cluster is running.
   - Deploy the services:
     ```bash
     kubectl apply -f k8s/deployment.yaml
     ```

4. **Run MongoDB and RabbitMQ**:
   - MongoDB and RabbitMQ should be available within the cluster or as services:
     ```bash
     kubectl apply -f k8s/mongo.yaml
     kubectl apply -f k8s/rabbitmq.yaml
     ```

5. **Access the Application**:
   - Open the app on `http://localhost:3000` and start placing orders.

## API Endpoints
- **GET /orders**: Retrieve all orders.
- **POST /orders**: Place a new order.
- **GET /orders/{id}**: Get details of a specific order.

## Future Enhancements
- **Payment Integration**: Add support for online payments.
- **Admin Dashboard**: Create an admin interface for restaurant owners to manage orders.
- **Notifications**: Real-time order updates via SMS or email.

