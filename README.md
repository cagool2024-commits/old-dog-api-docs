# Old Dog AI - API Integration Guide 🐕

Welcome to the Old Dog AI developer documentation. Our API provides a unified, low-latency routing layer for premium LLMs (Large Language Models) using a pay-as-you-go token model.

## 🚀 Quick Start

Old Dog AI is 100% compatible with the official OpenAI SDK format. You don't need to learn a new syntax.

### 1. Base URL Configuration
Simply point your existing OpenAI client to our routing endpoint:
`BASE_URL = "https://go.olddog.shop/v1"`

### 2. Authentication
Use the Token Credit Key generated from your dashboard:
`Authorization: Bearer od_live_xxxxxxxxxxxxx`

### 3. Example Request (Python)
```python
import openai

client = openai.OpenAI(
    api_key="od_live_your_token_key",
    base_url="[https://api.your-domain.xyz/v1](https://go.olddog.shop/v1)"
)

response = client.chat.completions.create(
    model="gpt-4",
    messages=[{"role": "user", "content": "Hello, Old Dog AI!"}]
)
print(response.choices[0].message.content)

```

## 🔒 Security & Rate Limiting

* Token credits never expire.
* Abusive high-concurrency requests will be automatically blocked by our WAF.
* We DO NOT log your prompts or fine-tune models on your data.

