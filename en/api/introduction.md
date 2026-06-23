# API Introduction

The GuildTags API provides programmatic access to tag data, server listings, and leaderboard information. It is designed for developers building integrations, bots, or tools that work with Discord clan tag data.

---

## Base URL

All API requests are made to the following base URL:

```
https://ufncqneiavsfunaffqes.supabase.co/functions/v1
```

---

## Format

The API returns JSON for all responses. Request bodies for POST and PATCH endpoints must also be sent as JSON with the `Content-Type: application/json` header.

---

## Versioning

The current API is v1. Breaking changes will result in a new version being introduced. The version is reflected in the endpoint paths where applicable.

---

## Rate limiting

The API enforces rate limits to protect the service. Current limits are:

| Tier | Requests per minute |
|---|---|
| Anonymous | 30 |
| Authenticated | 120 |

If you exceed the rate limit, the API returns a `429 Too Many Requests` response. The `Retry-After` header indicates how many seconds to wait before retrying.

---

## Errors

The API uses standard HTTP status codes:

| Code | Meaning |
|---|---|
| 200 | Success |
| 400 | Bad request — missing or invalid parameters |
| 401 | Unauthorised — missing or invalid API key |
| 404 | Not found — the requested resource does not exist |
| 429 | Rate limit exceeded |
| 500 | Server error |

Error responses include a JSON body with an `error` field describing the problem:

```json
{
  "error": "Tag not found"
}
```

---

## Getting started

1. Read the [Authentication](/documentation/en/api/authentication) page to get your API key
2. Browse the [Endpoints](/documentation/en/api/endpoints) reference
3. Make your first request using the examples provided

---

## Related pages

- [Authentication](/documentation/en/api/authentication)
- [Endpoints](/documentation/en/api/endpoints)
