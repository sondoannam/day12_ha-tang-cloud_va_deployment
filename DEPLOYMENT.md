# Deployment Information

## Public URL
https://agentic-job-hunter-web-46xv.onrender.com

## Platform
Render

## Test Commands

### Health Check
```bash
curl https://agentic-job-hunter-web-46xv.onrender.com/health
# Expected: {"status": "ok"}
```

### API Test (with authentication)
```bash
curl -X POST https://agentic-job-hunter-web-46xv.onrender.com/ask \
  -H "X-API-Key: YOUR_KEY" \
  -H "Content-Type: application/json" \
  -d '{"user_id": "test", "question": "Hello"}'

`AGENT_API_KEY` is a secret you define yourself for this project. The app compares it against the incoming `X-API-Key` header on protected requests.

Recommended way to generate it:

```bash
openssl rand -hex 32
```

Then paste that value into Render as `AGENT_API_KEY`, and use the same value in your API requests.
```

## Environment Variables Set
- PORT
- REDIS_URL
- AGENT_API_KEY
- OPENAI_API_KEY
- GEMINI_API_KEY
- LOG_LEVEL

## Screenshots
- [Deployment dashboard](screenshots/dashboard.png)
- [Service running](screenshots/running.png)
- [Test results](screenshots/test.png)
