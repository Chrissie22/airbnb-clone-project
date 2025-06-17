# AirBnB Clone Project

![AirBnB Logo](img/airbnb_logo.png)

## 🌍 Overview

The **AirBnB Clone Project** is a comprehensive full-stack web application inspired by the popular property rental platform, AirBnB. It was developed to simulate real-world software engineering practices, focusing on robust backend architecture, secure APIs, optimized databases, and modern DevOps workflows. This project showcases the collaborative effort of a cross-functional engineering team and highlights our ability to build a scalable and secure property booking platform.

---

## 🎯 Objectives

- Implement secure and scalable user authentication and authorization
- Enable full CRUD functionality for property listings and bookings
- Integrate real-time payment processing
- Build a review and rating system for quality assurance
- Optimize data performance with caching and indexing strategies

---

## 🛠️ Technology Stack

This project uses a range of modern technologies to ensure scalability, performance, and developer productivity. Below is an overview of the tools and their purposes:

- **Django**  
  A high-level Python web framework used to build the backend of the application, including business logic, database models, and API endpoints.

- **Django REST Framework (DRF)**  
  A powerful and flexible toolkit that extends Django for building clean, maintainable RESTful APIs.

- **PostgreSQL**  
  An open-source relational database used to store structured data such as user profiles, bookings, properties, and reviews.

- **GraphQL**  
  A query language for APIs that allows clients to request only the data they need, reducing over-fetching and improving performance.

- **Celery**  
  An asynchronous task queue used to handle background jobs like sending emails and processing time-consuming operations.

- **Redis**  
  An in-memory data store used alongside Celery for task queuing and also for caching frequently accessed data.

- **Docker**  
  A containerization tool that packages the application and its dependencies into isolated containers for consistent development and deployment.

- **GitHub Actions**  
  A CI/CD tool used to automate testing, linting, and deployment pipelines to ensure code quality and continuous delivery.

- **Docker Compose**  
  A tool for defining and running multi-container Docker applications, used to manage the development and testing environment.

---

## 👥 Team Roles

This project was built through team collaboration across multiple engineering roles. Each role played a critical part in the overall development lifecycle.

### 🔹 Backend Developer  
Designed and implemented RESTful and GraphQL APIs, business logic, and integrations with third-party services such as payment providers. Ensured code scalability, maintainability, and testing coverage.

### 🔹 Database Administrator (DBA)  
Crafted and managed PostgreSQL schemas, ensured referential integrity, optimized performance through indexing and query tuning, and handled data migrations.

### 🔹 DevOps Engineer  
Managed containerized development using Docker, orchestrated CI/CD pipelines with GitHub Actions, automated deployment, and ensured seamless production delivery.

### 🔹 QA Engineer  
Led quality assurance by writing test cases, performing functional, integration, and regression tests. Monitored bug resolution and verified production readiness.

---

## ⚙️ Key Technologies Explained

- **Django**: Robust Python framework useful used to develop the backend logic and data models  
- **Django REST Framework (DRF)**: Extends Django for building clean and powerful RESTful APIs  
- **PostgreSQL**: Advanced open-source relational database system  
- **GraphQL**: Allows clients to fetch precise data, reducing over-fetching  
- **Celery**: Executes background tasks like emails and notifications  
- **Redis**: Used for caching and speeding up repeated data queries  
- **Docker**: Containerizes the app for consistent local and cloud deployments  
- **GitHub Actions**: Automates testing, linting, and deployment tasks

---

## 🗃️ Database Design

The database schema is designed to support core functionalities like user management, property listings, bookings, payments, and reviews. Below are the key entities and their relationships:

### 🧑‍💼 Users
Represents both guests and hosts who interact with the platform.

**Key Fields:**
- `id`: Unique identifier
- `username`: User's display name
- `email`: Contact email
- `password`: Hashed password
- `is_host`: Boolean flag to distinguish between guests and hosts

**Relationships:**
- A user can **own multiple properties**
- A user can **make multiple bookings**
- A user can **write reviews**

---

### 🏡 Properties
Represents listings available for rent.

**Key Fields:**
- `id`: Unique identifier
- `owner_id`: Foreign key to User
- `title`: Title of the property
- `description`: Detailed info
- `location`: Geographic location

**Relationships:**
- A property is **owned by one user**
- A property can have **many bookings**
- A property can receive **multiple reviews**

---

### 📅 Bookings
Represents a reservation made by a user for a property.

**Key Fields:**
- `id`: Unique identifier
- `user_id`: Foreign key to User
- `property_id`: Foreign key to Property
- `check_in_date`: Start date of booking
- `check_out_date`: End date of booking

**Relationships:**
- A booking is **linked to one user and one property**
- Each booking has an **associated payment**

---

### 💳 Payments
Handles payment details for bookings.

**Key Fields:**
- `id`: Unique identifier
- `booking_id`: Foreign key to Booking
- `amount`: Payment amount
- `payment_status`: Completed or pending
- `payment_date`: Date of transaction

**Relationships:**
- Each payment is **tied to a booking**

---

### ⭐ Reviews
Allows users to rate and comment on properties after their stay.

**Key Fields:**
- `id`: Unique identifier
- `user_id`: Foreign key to User
- `property_id`: Foreign key to Property
- `rating`: Numerical score (1–5)
- `comment`: Text feedback

**Relationships:**
- A review is **written by a user**
- A review is **associated with a property**


---

## 🚀 Feature Highlights

### ✅ User Authentication  
- Registration & login (JWT-based)  
- Profile roles: Guest or Host  
- Secure password hashing

### ✅ Property Management  
- Hosts can create, edit, and delete listings  
- Location-based search and filtering

### ✅ Booking Engine  
- Real-time booking availability  
- Conflict prevention on overlapping dates

### ✅ Payment Integration  
- Process and confirm payments securely  
- Payment status tracking per booking

### ✅ Review System  
- Star rating (1–5) and text feedback  
- Display average ratings on listings

### ✅ Developer-Friendly API Docs  
- REST and GraphQL API auto-generated documentation  
- Swagger & GraphiQL interfaces included

---

## 🔐 API Security Highlights

### 1. **Authentication (JWT)**  
Only authenticated users can access sensitive endpoints.

### 2. **Role-Based Access Control**  
Different permissions for Guests, Hosts, and Admins.

### 3. **Rate Limiting**  
Prevents abuse and denial-of-service attempts.

### 4. **Data Encryption**  
All sensitive data is encrypted during transmission (HTTPS) and securely stored.

---

## 🔄 CI/CD Pipeline

Automated testing and deployment enhance productivity and reduce errors.

### 🧰 Tools Used:
- **GitHub Actions**: Linting, unit tests, integration tests  
- **Docker Compose**: Multi-container orchestration for services  
- **PostgreSQL Service**: For testing and staging environments  

---

## 📌 Conclusion

This AirBnB Clone demonstrates the architecture, security, and features required for modern full-stack applications. It also showcases our ability to work collaboratively, write clean and scalable code, and deploy robust systems in a real-world simulation.

---

## 👤 Contributors 
**Christabel E. Ojobolo**  
- 🌐 [GitHub: Chrissie22](https://github.com/Chrissie22)  
- 💼 [LinkedIn: Christabel E. Ojobolo](https://www.linkedin.com/in/christabel-ojobolo)