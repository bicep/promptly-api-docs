# Speech Generation API

Convert text into natural-sounding speech.

## Endpoint
POST `/v1/speech/generate`

## Authentication
All requests require a Bearer token in the `Authorization` header.

```http
Authorization: Bearer YOUR_API_KEY
Content-Type: application/json
```

## Request Body
```json
{
  "text": "Welcome to Promptly API!",
  "voice": "alloy",
  "format": "mp3"
}
```

## Response
```json
{
  "id": "sp-789",
  "object": "speech_generation",
  "audio_url": "https://cdn.promptly.ai/audio/sp-789.mp3"
}
```

## Errors
- `401 Unauthorized` → Invalid API key
- `429 Too Many Requests` → Rate limit exceeded
- `400 Bad Request` → Invalid parameters
