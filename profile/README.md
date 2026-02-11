<h1 align="center">
  Langbly
</h1>

<p align="center">
  <strong>Translation API — drop-in Google Translate v2 replacement, powered by LLMs</strong>
</p>

<p align="center">
  <a href="https://pypi.org/project/langbly/"><img src="https://img.shields.io/pypi/v/langbly?label=pypi&color=blue" alt="PyPI"></a>
  <a href="https://www.npmjs.com/package/langbly"><img src="https://img.shields.io/npm/v/langbly?color=blue" alt="npm"></a>
  <a href="https://langbly.com"><img src="https://img.shields.io/badge/website-langbly.com-orange" alt="Website"></a>
  <a href="https://langbly.com/docs"><img src="https://img.shields.io/badge/docs-langbly.com%2Fdocs-green" alt="Docs"></a>
</p>

<p align="center">
  <a href="https://langbly.com">Website</a> ·
  <a href="https://langbly.com/docs">Documentation</a> ·
  <a href="https://langbly.com/pricing">Pricing</a> ·
  <a href="https://langbly.com/compare">Compare</a> ·
  <a href="https://langbly.com/signup">Get Free API Key</a>
</p>

---

**Langbly** is a translation API that's a drop-in replacement for Google Translate v2. Same request format, same response shape — switch in one PR. Powered by LLMs for higher quality translations at a fraction of the cost.

### Why developers switch to Langbly

| | Google Translate | DeepL | **Langbly** |
|---|---|---|---|
| **Price per 1M chars** | $20 | $25 | **$1.99–$4** |
| **API compatibility** | — | Own format | **Google Translate v2** |
| **Translation quality** | Statistical | Neural | **LLM (context-aware)** |
| **Free tier** | None | 500K/mo | **500K trial** |
| **Locale formatting** | ❌ | ❌ | **✅ Automatic** |

### Install

```bash
pip install langbly          # Python
npm install langbly          # JavaScript / TypeScript
```

### Quick Start

```python
from langbly import Langbly

client = Langbly(api_key="your-api-key")
result = client.translate("Hello world", target="nl")
print(result.text)  # "Hallo wereld"
```

```typescript
import { Langbly } from "langbly";

const client = new Langbly({ apiKey: "your-api-key" });
const result = await client.translate("Hello world", { target: "nl" });
console.log(result.text); // "Hallo wereld"
```

### Migrate from Google Translate in 2 minutes

Already using Google Translate v2? Just change the base URL:

```bash
# Before: https://translation.googleapis.com/language/translate/v2
# After:  https://api.langbly.com/language/translate/v2

curl -X POST https://api.langbly.com/language/translate/v2 \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"q": "Hello world", "target": "nl"}'
```

→ Full migration guide: [langbly.com/docs/migrate-google](https://langbly.com/docs/migrate-google)

### SDKs & Resources

| Repository | Description | Install |
|------------|-------------|---------|
| [langbly-python](https://github.com/Langbly/langbly-python) | Python SDK — async support, auto-retry, typed errors | `pip install langbly` |
| [langbly-js](https://github.com/Langbly/langbly-js) | JS/TS SDK — native fetch, zero dependencies, TypeScript | `npm install langbly` |
| [examples](https://github.com/Langbly/examples) | curl examples, migration guides, code samples | — |

### Features

- **Google Translate v2 compatible** — same `/language/translate/v2` endpoint
- **LLM-powered** — understands context, tone, idioms, and locale conventions
- **Auto-retry** — exponential backoff with Retry-After support in both SDKs
- **Locale formatting** — automatic decimal, date, and currency formatting per target language
- **Batch translation** — translate multiple texts in a single request
- **Language detection** — identify source language automatically
- **HTML support** — translate HTML while preserving tags and attributes

### Pricing

| Plan | Price | Characters | Per 1M chars |
|------|-------|------------|--------------|
| Free | $0 | 500K trial | — |
| Starter | $19/mo | 5M | $3.80 |
| Growth | $69/mo | 25M | $2.76 |
| Scale | $199/mo | 100M | $1.99 |

Annual plans: **20% off**. Overage: $4/1M characters.

→ [Start free](https://langbly.com/signup) — no credit card required

---

<p align="center">
  <sub>Built by <a href="https://github.com/jasperdewinter">Jasper de Winter</a> · <a href="https://langbly.com">langbly.com</a></sub>
</p>
