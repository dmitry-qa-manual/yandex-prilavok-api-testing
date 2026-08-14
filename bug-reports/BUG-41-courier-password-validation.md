# BUG-41 — Courier can be created with an invalid password

## Summary

The API allows creating a courier with a password that does not meet the required length restrictions.

## Priority

Standard

## Status

Open

## Preconditions

The API is available.

## Steps to Reproduce

1. Send a `POST` request to `/api/v1/courier`.
2. Use a password shorter than the minimum allowed length.
3. Send the request with valid values for the other required fields.
4. Repeat the request with a password longer than the maximum allowed length.

## Expected Result

The API rejects passwords that do not meet the required length restrictions and returns an appropriate validation error.

The courier is not created.

## Actual Result

The API returns `201 Created` and creates a courier with an invalid password.

## Request

**Method:** `POST`

**Endpoint:** `/api/v1/courier`

## Test Data

Examples of invalid values:

- Password shorter than the minimum allowed length
- Password longer than the maximum allowed length

## Environment

- Postman
- Yandex Practicum test stand
- REST API

## Additional Information

The defect was identified during boundary value and negative testing of the courier creation endpoint.
