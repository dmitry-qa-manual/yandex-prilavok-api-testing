# BUG-42 — Courier can be authorized without a password

## Summary

The API allows courier authorization when the password is not provided.

## Priority

Standard

## Status

Open

## Preconditions

A courier account exists in the system.

## Steps to Reproduce

1. Send a `POST` request to `/api/v1/courier/login`.
2. Specify a valid courier login.
3. Do not provide the `password` field.
4. Send the request.

## Expected Result

The API rejects the request and returns an appropriate validation error indicating that the password is required.

The courier is not authorized.

## Actual Result

The API accepts the request without a password and returns a successful response.

## Request

**Method:** `POST`

**Endpoint:** `/api/v1/courier/login`

## Environment

- Postman
- Yandex Practicum test stand
- REST API

## Additional Information

The defect was identified during negative testing of the courier authorization endpoint.
