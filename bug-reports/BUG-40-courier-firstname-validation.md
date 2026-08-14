# BUG-40 — Courier can be created with an invalid firstName

## Summary

The API allows creating a courier with an invalid `firstName` value.

## Priority

Standard

## Status

Open

## Preconditions

The API is available.

## Steps to Reproduce

1. Send a `POST` request to `/api/v1/courier`.
2. Use a `firstName` containing only 1 character.
3. Send the request with valid values for the other fields.
4. Repeat the request with a `firstName` longer than the allowed maximum.
5. Repeat the request with digits in the `firstName`.
6. Repeat the request with an empty `firstName`.

## Expected Result

The API rejects invalid `firstName` values and returns an appropriate validation error.

The courier is not created.

## Actual Result

The API returns `201 Created` and creates a courier with an invalid `firstName` value.

## Request

**Method:** `POST`

**Endpoint:** `/api/v1/courier`

## Test Data

Examples of invalid values:

- `firstName` with 1 character
- `firstName` exceeding the allowed maximum length
- `firstName` containing digits
- Empty `firstName`

## Environment

- Postman
- Yandex Practicum test stand
- REST API

## Additional Information

The defect was identified during boundary value and negative testing of the courier creation endpoint.
