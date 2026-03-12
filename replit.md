# Railway Ticket Booking System

## Overview
A Java-based Railway Ticket Booking System that simulates real-world railway reservation behavior. The system includes seat allocation, ticket confirmation, RAC (Reservation Against Cancellation) and waiting list management, ticket cancellation, and automatic promotion of passengers when seats become available.

## Project Structure
```
src/
  main/
    java/
      com/railway/
        model/          # Entity classes (User, Train, Seat, Booking)
        dao/            # Data Access Objects for database operations
        service/        # Business logic services
        servlet/        # HTTP request handlers
        util/           # Utility classes (DatabaseConnection, DatabaseInitializer)
        RailwayApp.java # Main application entry point
    webapp/
      css/              # Stylesheets
      index.html        # Main HTML page
lib/                    # JAR dependencies (PostgreSQL JDBC driver)
```

## Technologies Used
- **Backend**: Java (JDK 11+)
- **Database**: PostgreSQL (connected via JDBC)
- **Frontend**: HTML5, CSS3, JavaScript
- **HTTP Server**: Java's built-in HttpServer

## Features
1. **User Registration & Login** - Secure authentication system
2. **Train Management** - Multiple trains with different classes (AC, Sleeper, General)
3. **Ticket Booking** - Automatic seat allocation with fare calculation
4. **RAC System** - Reservation Against Cancellation queue
5. **Waiting List** - Managed waiting list with position tracking
6. **Ticket Cancellation** - Cancel tickets with automatic promotion
7. **PNR Status** - Check booking status by PNR number
8. **My Bookings** - View all user bookings

## OOP Principles Applied
- **Encapsulation**: Private fields with public getters/setters
- **Abstraction**: DAO pattern abstracts database operations
- **Inheritance**: Model classes implement Serializable
- **Polymorphism**: Service layer handles different booking statuses

## Database Schema
- **users**: User registration and authentication
- **trains**: Train details and fare information
- **seats**: Individual seats for each train
- **bookings**: Booking records with status tracking

## Running the Application
The application runs on port 5000 and automatically:
1. Connects to PostgreSQL database
2. Creates necessary tables
3. Inserts sample train data
4. Starts the HTTP server

## Recent Changes
- Initial project setup (December 2024)
- Implemented complete booking system with RAC and waiting list
- Created responsive HTML/CSS frontend
