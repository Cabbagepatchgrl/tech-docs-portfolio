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
Base URL: https://api.enterpriseportal.com/v1
```
Authorization: Bearer YOUR_API_KEY
curl -X GET "https://api.enterpriseportal.com/v1/users/usr_98765" \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Accept: application/json"
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
{
  "status": "error",
  "code": 404,
  "message": "User with ID 'usr_98765' was not found.",
  "timestamp": "2026-09-21T15:30:00Z"
}