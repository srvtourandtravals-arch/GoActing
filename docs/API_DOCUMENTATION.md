# API Documentation

## Authentication

### Login
- **Endpoint:** `POST /api/auth/login`
- **Description:** Authenticates a user and returns a token.
- **Request Body:**
  - `username`: string
  - `password`: string
- **Response:**
  - `token`: string

### Register
- **Endpoint:** `POST /api/auth/register`
- **Description:** Registers a new user.
- **Request Body:**
  - `username`: string
  - `password`: string
  - `email`: string
- **Response:**
  - `userId`: string

## Booking

### Create Booking
- **Endpoint:** `POST /api/bookings`
- **Description:** Creates a new booking.
- **Request Body:**
  - `userId`: string
  - `tripDetails`: object
- **Response:**
  - `bookingId`: string

### Get Booking
- **Endpoint:** `GET /api/bookings/:id`
- **Description:** Retrieves booking details.
- **Response:**
  - `booking`: object

## Driver Management

### Add Driver
- **Endpoint:** `POST /api/drivers`
- **Description:** Adds a new driver.
- **Request Body:**
  - `name`: string
  - `vehicle`: string
- **Response:**
  - `driverId`: string

### Get Driver
- **Endpoint:** `GET /api/drivers/:id`
- **Description:** Retrieves driver details.
- **Response:**
  - `driver`: object

## Payment

### Process Payment
- **Endpoint:** `POST /api/payments`
- **Description:** Processes payment for a booking.
- **Request Body:**
  - `bookingId`: string
  - `amount`: number
- **Response:**
  - `transactionId`: string

## Admin Operations

### Get All Users
- **Endpoint:** `GET /api/admin/users`
- **Description:** Retrieves a list of all users.
- **Response:**
  - `users`: array

### Delete User
- **Endpoint:** `DELETE /api/admin/users/:id`
- **Description:** Deletes a user.
- **Response:**
  - `message`: string

---

_Last Updated: 2026-02-15 08:14:06 UTC_