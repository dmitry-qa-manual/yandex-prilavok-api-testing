# Yandex Practicum — API Testing

## Project Overview

This project was completed as part of the Yandex Practicum Software Testing course.

The goal was to test the API of the Yandex Practicum application and verify its behavior with valid and invalid input data.

## API Testing Activities

- API requirements analysis
- Positive and negative testing
- Boundary value analysis
- Input validation testing
- Required field testing
- HTTP response code verification
- API endpoint testing
- Bug reporting

## Tested Endpoints

### POST /api/v1/courier

Courier creation testing:

- Valid data
- Existing login
- Missing login
- Missing password
- Missing login and password
- Login length validation
- Login character validation
- First name length validation
- First name character validation
- Empty first name
- Password length validation

### POST /api/v1/courier/login

Courier authorization testing:

- Login with valid credentials
- Login with an incorrect password
- Login without login
- Login without password

### DELETE /api/v1/courier/:id

Courier deletion testing:

- Deletion of a non-existent courier
- Deletion of an existing courier
- Deletion of a courier with an active order

### GET /api/v1/orders/track

Order retrieval testing:

- Existing track
- Non-existent track
- Request without the track parameter

## Tools

- Postman
- Swagger
- REST API
- HTTP methods
- JSON
- cURL

## Test Design Techniques

- Equivalence Partitioning
- Boundary Value Analysis
- Positive Testing
- Negative Testing

## Bug Reporting

During testing, defects were identified and documented with:

- Preconditions
- Steps to reproduce
- Expected result
- Actual result
- Environment
- Priority

## Result

The project provided practical experience in API testing, request validation, negative testing, boundary value analysis and documenting API defects.

## 📁 Project Materials

* [API Test Checklist](test-checklist/README.md)
* [Bug Reports](bug-reports/README.md)
