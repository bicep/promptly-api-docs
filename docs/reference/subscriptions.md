# Subscriptions API

Manage and monitor subscriptions for your account.

## Endpoints
- GET `/v1/subscriptions` → List all subscriptions
- POST `/v1/subscriptions` → Create a new subscription
- DELETE `/v1/subscriptions/{id}` → Cancel a subscription

## Authentication
All requests require a Bearer token in the `Authorization` header.

```http
Authorization: Bearer YOUR_API_KEY
Content-Type: application/json
```

## Example: List Subscriptions
```bash
curl -X GET "https://api.promptly.ai/v1/subscriptions" \
  -H "Authorization: Bearer YOUR_API_KEY"
```

## Example Response
```json
{
  "subscriptions": [
    {
      "id": "sub-001",
      "plan": "Pro",
      "status": "active",
      "start_date": "2025-09-20"
    }
  ]
}
```

## Errors
- `401 Unauthorized` → Invalid API key
- `429 Too Many Requests` → Rate limit exceeded
- `404 Not Found` → Subscription ID does not exist
