---
title: User Management REST API Reference
target_audience: Software Engineers, Integration Partners
last_updated: September 2026
document_owner: Technical Operations & Developer Experience
---

# REST API Reference: User Management Service v1.0

Welcome to the User Management API reference documentation. This service provides programmatic access to create, retrieve, and manage enterprise user profiles within the core portal platform.

---

## Overview & Base URL

All requests must be made over HTTPS. Plain HTTP requests will be rejected with a `301 Moved Permanently` redirect.

```text
Base URL: [https://api.enterpriseportal.com/v1](https://api.enterpriseportal.com/v1)
```

---

## Authentication

The User Management API uses Bearer Tokens to authenticate requests. Pass your API key in the `Authorization` header for every HTTP request.

```http
Authorization: Bearer YOUR_API_KEY
```

> **Security Note:** Never commit API keys to public repositories or expose them in client-side code.

---

## Endpoints Summary

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `GET` | `/users` | Retrieve a paginated list of active users. |
| `GET` | `/users/{id}` | Fetch a specific user profile by unique ID. |
| `POST` | `/users` | Create a new user record. |

---

## GET /users/{id}

Retrieves the detailed profile object for an individual user account.

### Path Parameters

| Parameter | Type | Required | Description |
| :--- | :--- | :--- | :--- |
| `id` | `string` | Yes | Unique user identifier (e.g., `usr_98765`). |

### Request Example

```bash
curl -X GET "[https://api.enterpriseportal.com/v1/users/usr_98765](https://api.enterpriseportal.com/v1/users/usr_98765)" \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Accept: application/json"
```

### Response Example (`200 OK`)

```json
{
  "status": "success",
  "data": {
    "id": "usr_98765",
    "name": "Jane Doe",
    "email": "jane.doe@enterpriseportal.com",
    "role": "administrator",
    "account_status": "active",
    "created_at": "2026-01-15T08:30:00Z"
  }
}
```

---

## Error Handling

The API returns standard HTTP status codes along with a structured JSON error body to help troubleshoot integration issues.

| HTTP Code | Error Type | Description |
| :--- | :--- | :--- |
| `401` | `Unauthorized` | Invalid, expired, or missing API token. |
| `404` | `Not Found` | The requested user ID does not exist in the database. |
| `500` | `Internal Server Error` | An internal service error occurred. Retry with backoff. |

### Sample Error Payload (`404 Not Found`)

```json
{
  "status": "error",
  "code": 404,
  "message": "User with ID 'usr_98765' was not found.",
  "timestamp": "2026-09-21T15:30:00Z"
}
```