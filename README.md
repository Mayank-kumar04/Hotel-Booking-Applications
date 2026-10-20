# Hotel Booking Application

## Overview

A full-stack hotel booking and management system built with **React.js** on the frontend and **Spring Boot** on the backend.

The application provides separate functionality for **Users** and **Administrators**, allowing users to manage their hotel reservations while administrators manage rooms and bookings.

## Key Features

### User Features

* User registration and login
* Browse available rooms
* Book a room
* View personal booking history
* Cancel bookings

### Admin Features

* Admin authentication
* View all bookings
* Manage hotel rooms
* Add new rooms
* Update room information
* Delete rooms
* Manage booking records

## Technology Stack

### Frontend

* React.js
* Redux
* Axios
* JavaScript
* HTML5
* CSS3

### Backend

* Java
* Spring Boot
* Spring Security
* Spring Data JPA
* Hibernate

### Database

* MySQL

## Application Architecture

```text
React.js Frontend
       |
       | REST API
       ↓
Spring Boot Backend
       |
       | JPA / Hibernate
       ↓
     MySQL
```

## Project Structure

```text
Hotel-Booking-Applications/
│
├── frontend/
│   └── Hotel-booking-application/
│
├── backend/
│   └── HotelBookingApplication/
│
└── README.md
```

## Prerequisites

Before running the application, make sure you have installed:

* Node.js
* npm
* Java JDK 11 or later
* MySQL
* Maven

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Mayank-kumar04/Hotel-Booking-Applications.git
cd Hotel-Booking-Applications
```

### 2. Configure MySQL

Create a MySQL database for the application.

```sql
CREATE DATABASE hotel_booking;
```

Configure the database connection in:

```text
backend/HotelBookingApplication/src/main/resources/application.properties
```

Example:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/hotel_booking
spring.datasource.username=your_username
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
```

**Do not commit your actual database password to GitHub.**

### 3. Start the Backend

Navigate to the backend directory:

```bash
cd backend/HotelBookingApplication
```

Build the application:

```bash
./mvnw clean install
```

Start the Spring Boot server:

```bash
./mvnw spring-boot:run
```

On Windows, you can use:

```powershell
.\mvnw.cmd spring-boot:run
```

### 4. Start the Frontend

Open another terminal and navigate to:

```bash
cd frontend/Hotel-booking-application
```

Install the required dependencies:

```bash
npm install
```

Start the React development server:

```bash
npm start
```

The frontend will then be available through the local development server.

## User Workflow

```text
Register / Login
       ↓
Browse Rooms
       ↓
Select Room
       ↓
Create Booking
       ↓
View Booking
       ↓
Cancel Booking
```

## Admin Workflow

```text
Admin Login
     ↓
Admin Dashboard
     ↓
Manage Rooms
     ↓
Manage Bookings
     ↓
Update / Delete Records
```

## API

The backend exposes REST APIs for user and administrative operations.

### User Operations

```text
POST   /api/user/bookings
GET    /api/user/bookings
```

### Admin Operations

```text
GET    /api/admin/bookings
DELETE /api/admin/bookings/{bookingId}

POST   /api/admin/rooms
PUT    /api/admin/rooms/{roomId}
DELETE /api/admin/rooms/{roomId}
```

> API paths may vary depending on the current backend implementation.

## Future Enhancements

Some possible improvements include:

* Hotel and room search
* Advanced room filtering
* Room availability validation
* Online payment integration
* Email booking notifications
* Booking status tracking
* Admin analytics dashboard
* Improved responsive UI

## Author

**Mayank Kumar**

B.Tech Computer Science and Engineering

---

## License

This project is intended for educational and development purposes.
