# BUG-43 — Courier with an active order can be deleted

## Summary

The API allows deleting a courier who has an active order.

## Priority

Critical

## Status

Open

## Preconditions

1. A courier exists in the system.
2. The courier has an active order assigned to them.

## Steps to Reproduce

1. Obtain the courier ID of a courier with an active order.
2. Send a `DELETE` request to `/api/v1/courier/{id}`.
3. Specify the courier ID in the request.
4. Send the request.

## Expected Result

The API does not allow deleting a courier who has an active order and returns an appropriate error response.

The courier remains in the system.

## Actual Result

The API successfully deletes the courier even though an active order is assigned to them.

## Request

**Method:** `DELETE`

**Endpoint:** `/api/v1/courier/{id}`

## Environment

- Postman
- Yandex Practicum test stand
- REST API

## Additional Information

The defect was identified during negative testing of the courier deletion endpoint.
