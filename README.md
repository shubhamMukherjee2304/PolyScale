

# PolyScale – Scalable Microservices E-commerce Backend

## Overview

**PolyScale** is a microservices-based e-commerce backend platform designed for scalability, modularity, and high performance. Built using modern technologies like **Golang**, **GraphQL**, **gRPC**, **PostgreSQL**, and **Elasticsearch**, it delivers a robust infrastructure capable of supporting real-world commerce applications.

Each core domain—**Accounts**, **Products**, and **Orders**—is implemented as an independent service, enabling clean separation of concerns, easier maintenance, and horizontal scalability.

---

## 🔧 Tech Stack

* **Golang** – Service development and business logic
* **GraphQL** – Unified API layer for efficient querying
* **gRPC** – Inter-service communication
* **PostgreSQL** – Transactional database for Accounts and Orders
* **Elasticsearch** – Fast, flexible search in the Product service
* **Docker** – Containerized services for consistent deployment

---

## 🧱 Microservice Architecture

### 1. Account Service

* Handles user registration, login, profile management
* Uses PostgreSQL for persistent and consistent user data
* Exposes APIs for authentication and user details

### 2. Product Service

* Manages product listings, categories, and inventory
* Integrated with Elasticsearch for full-text and filtered product search
* Supports creation, updates, and rich querying via GraphQL

### 3. Order Service

* Manages shopping cart, order placement, and payment tracking
* Ensures data integrity with PostgreSQL
* Maintains consistent communication with the account and product services via gRPC

---

## 🚀 Features

* 🔹 **GraphQL Gateway**: Unified API entry point for all services
* 🔹 **gRPC Communication**: Low-latency messaging between microservices
* 🔹 **Elasticsearch Search**: Fast and scalable product search functionality
* 🔹 **Modular Microservices**: Independently deployable services for better scalability
* 🔹 **Dockerized Deployment**: Consistent local and production environments

---

## 📦 Getting Started

### Prerequisites

* Docker & Docker Compose
* Go 1.20+
* PostgreSQL
* Elasticsearch 8+

### Clone the Repository

```bash
git clone https://github.com/your-username/polyscale.git
cd polyscale
```

### Start with Docker Compose

```bash
docker-compose up --build
```

> This will spin up the microservices, GraphQL gateway, PostgreSQL, and Elasticsearch containers.

---

## 🧪 API Endpoints

### GraphQL Gateway

```
POST /graphql
```

Example query:

```graphql
query {
  getUser(id: "123") {
    name
    email
  }
}
```

---

## 📁 Directory Structure

```
/polyscale
│
├── account-service/
├── product-service/
├── order-service/
├── graphql-gateway/
├── proto/              # gRPC proto files
├── docker-compose.yml
└── README.md
```

---

## ✅ Future Improvements

* JWT-based user authentication
* Distributed tracing and observability (Jaeger, Prometheus)
* CI/CD integration
* Kubernetes-based deployment

---

## 📌 Impact

Delivered a **scalable** backend architecture capable of handling:

* Complex inter-service operations
* Rapid, customizable product searches
* Reliable and consistent user and order workflows

---

## 🧑‍💻 Author

**Shubham Mukherjee**
[LinkedIn](https://www.linkedin.com/in/shubham-mukherjee-a851a420a) | [GitHub](https://github.com/shubhammukherjee1000)

---

Let me know if you’d like to include setup scripts, diagrams, API documentation (e.g. with Postman/OpenAPI), or Kubernetes configs!
