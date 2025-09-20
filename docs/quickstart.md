# Quick Start Guide

## Step 1: Install dependencies

## Step 2: Create an account and get your API key
Sign up at [https://promptly.ai/signup](https://promptly.ai/signup)

## Step 3: Generate Text
```python
import requests
url = "https://api.promptly.ai/v1/generate/text"
headers = {"Authorization": "Bearer YOUR_API_KEY"}
data = {"model":"promptly-gpt-3","prompt":"Write a haiku about AI","max_tokens":50}

resp = requests.post(url, headers=headers, json=data)
print(resp.json())

url = "https://api.promptly.ai/v1/generate/image"
data = {"model":"promptly-dalle", "prompt":"Futuristic city skyline", "size":"1024x1024"}
resp = requests.post(url, headers=headers, json=data)
print(resp.json())
