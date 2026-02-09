<h1 align="center">
  Langbly
</h1>

<p align="center">
  <strong>Google Translate v2 compatible API — powered by LLMs, 5x cheaper</strong>
</p>

<p align="center">
  <a href="https://langbly.com">Website</a> &bull;
  <a href="https://langbly.com/docs">Docs</a> &bull;
  <a href="https://langbly.com/pricing">Pricing</a>
</p>

---

**Langbly** is a drop-in replacement for the Google Translate v2 API. Same request format, same response shape — just change the endpoint URL.

### Why Langbly?

- **5-10x cheaper** — $4/1M characters vs Google's $20/1M
- **Better quality** — LLM-powered translations that understand context, tone, and locale conventions
- **Drop-in replacement** — Same API shape as Google Translate v2. Switch in one PR
- **European languages** — Especially strong for Dutch, German, and French

### Quick Start

```bash
# Just change the base URL — your existing code works
curl -X POST https://api.langbly.com/language/translate/v2 \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"q": "Hello world", "target": "nl"}'
```

### SDKs

| Package | Install |
|---------|---------|
| [langbly-python](https://github.com/Langbly/langbly-python) | `pip install langbly` |
| [langbly-js](https://github.com/Langbly/langbly-js) | `npm install langbly` |

### Pricing

| Plan | Price | Characters | Per 1M chars |
|------|-------|------------|--------------|
| Free | $0 | 500K trial | — |
| Starter | $19/mo | 5M | $3.80 |
| Growth | $69/mo | 25M | $2.76 |
| Scale | $199/mo | 100M | $1.99 |

Annual plans: **20% off**. Overage: $4/1M characters.

---

<p align="center">
  <sub>Built by <a href="https://github.com/jasperdewinter">Jasper de Winter</a></sub>
</p>
