# Image Generation API

Generate images dynamically from text prompts.

## Endpoint
POST `/v1/image/generate`

## Authentication
All requests require a Bearer token in the `Authorization` header.

```http
Authorization: Bearer YOUR_API_KEY
Content-Type: application/json
```

## Request Body
```json
{
  "prompt": "A futuristic cityscape at sunset",
  "width": 1024,
  "height": 1024,
  "num_images": 1
}
```

## Response
```json
{
  "id": "img-456",
  "object": "image_generation",
  "images": [
    "https://cdn.promptly.ai/images/img-456.png"
  ]
}
```

## Errors
- `401 Unauthorized` → Invalid API key
- `429 Too Many Requests` → Rate limit exceeded
- `400 Bad Request` → Invalid parameters
