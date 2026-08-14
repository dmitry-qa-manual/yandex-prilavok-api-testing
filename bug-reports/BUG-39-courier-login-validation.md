# BUG-39 — Courier can be created with an invalid login

## Summary

The API allows creating a courier with a login that does not meet the required length or format restrictions.

## Priority

Standard

## Status

Open

## Preconditions

The API is available.

## Steps to Reproduce

1. Send a `POST` request to `/api/v1/courier`.
2. Use a login containing only 1 character.
3. Send the request with valid values for the other required fields.
4. Repeat the request with a login longer than the allowed maximum.
5. Repeat the request using a login written in Russian.

## Expected Result

The API rejects invalid login values and returns an appropriate validation error.

The courier is not created.

## Actual Result

The API returns `201 Created` and creates a courier with an invalid login value.

## Request

**Method:** `POST`

**Endpoint:** `/api/v1/courier`

## Test Data

Examples of invalid values:

- Login with 1 character
- Login longer than the allowed maximum
- Login containing Russian characters

## Environment

- Postman
- Yandex Practicum test stand
- REST API

## Additional Information

The defect was identified during boundary value and negative testing of the courier creation endpoint.
