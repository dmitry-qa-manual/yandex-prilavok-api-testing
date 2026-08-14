# API Test Checklist

## 📋 Overview

The checklist was created as part of the Yandex Practicum Software Testing diploma project.

The API was tested using positive and negative scenarios, including input validation and boundary value checks.

## 🔌 Tested API Endpoints

### POST /api/v1/courier

Tested:

- Creating a courier with valid data
- Creating a courier with an existing login
- Missing required fields
- Invalid login length
- Invalid login characters
- Invalid firstName length
- Invalid firstName characters
- Empty firstName
- Invalid password length
- Boundary values for input fields

### POST /api/v1/courier/login

Tested:

- Authorization with valid credentials
- Authorization with an incorrect password
- Authorization without login
- Authorization without password

### DELETE /api/v1/courier/:id

Tested:

- Deleting an existing courier
- Deleting a non-existent courier
- Deleting a courier with an active order

### GET /api/v1/orders/track

Tested:

- Getting an existing order by track number
- Getting an order using a non-existent track number
- Request without the track parameter

## 🧪 Test Design Techniques

- Equivalence Partitioning
- Boundary Value Analysis
- Positive Testing
- Negative Testing
- Required field validation
- Input format validation

## 🛠️ Tools

- Postman
- Swagger
- REST API
- JSON
- HTTP methods

## 📊 Test Results

The checklist contained positive and negative checks for the tested API endpoints.

Failed checks were documented as separate bug reports.

## 🎯 Result

The checklist provided a structured approach to API testing and helped identify defects related to input validation, authorization and courier management.
