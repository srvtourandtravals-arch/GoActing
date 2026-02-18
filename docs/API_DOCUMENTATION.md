# API Documentation

## Authentication
### Login
- **POST** `/api/login`
  - Description: Authenticates a user and returns a token.
  - Request Body: `{ "username": "string", "password": "string" }`
  - Responses:
    - 200: `{ "token": "string" }`
    - 401: `Unauthorized`

### Register
- **POST** `/api/register`
  - Description: Registers a new user and returns a confirmation.
  - Request Body: `{ "username": "string", "password": "string", "email": "string" }`
  - Responses:
    - 201: `User created successfully`
    - 400: `Bad Request`

## Bookings
### Create Booking
- **POST** `/api/bookings`
  - Description: Creates a new booking.
  - Request Body: `{ "driverId": "string", "date": "string", "pickupLocation": "string", "dropoffLocation": "string" }`
  - Responses:
    - 201: `Booking created successfully`
    - 400: `Bad Request`

### Get Booking
- **GET** `/api/bookings/{id}`
  - Description: Retrieves booking details by ID.
  - Responses:
    - 200: `{ "id": "string", "driverId": "string", "date": "string", "pickupLocation": "string", "dropoffLocation": "string" }`
    - 404: `Not Found`

## Drivers
### Get All Drivers
- **GET** `/api/drivers`
  - Description: Retrieves a list of all drivers.
  - Responses:
    - 200: `[ { "id": "string", "name": "string" } ]`

### Get Driver
- **GET** `/api/drivers/{id}`
  - Description: Retrieves a specific driver by ID.
  - Responses:
    - 200: `{ "id": "string", "name": "string", "vehicle": "string" }`
    - 404: `Not Found`

## Payments
### Make Payment
- **POST** `/api/payments`
  - Description: Processes a payment for a booking.
  - Request Body: `{ "bookingId": "string", "amount": "number" }`
  - Responses:
    - 200: `Payment successful`
    - 400: `Bad Request`

## Admin Operations
### Get All Bookings
- **GET** `/api/admin/bookings`
  - Description: Retrieves a list of all bookings.
  - Responses:
    - 200: `[ { "id": "string", "pickupLocation": "string", "dropoffLocation": "string" } ]`

### Get All Users
- **GET** `/api/admin/users`
  - Description: Retrieves a list of all registered users.
  - Responses:
    - 200: `[ { "id": "string", "username": "string" } ]`