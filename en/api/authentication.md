# Authentication

Some GuildTags API endpoints are publicly accessible without authentication. Others require an API key to identify your application and enforce rate limits.

---

## Public endpoints

Read-only endpoints that return public tag and leaderboard data do not require authentication. You can query them directly:

```
GET https://ufncqneiavsfunaffqes.supabase.co/functions/v1/getTagCount
```

Public endpoints are subject to anonymous rate limits (30 requests per minute).

---

## Authenticated endpoints

Endpoints that write data, access protected resources, or require higher rate limits require an API key.

---

## Getting an API key

API access is currently available to developers on request. To request a key:

1. Join the [GuildTags Discord server](https://discord.com/invite/9CqvbP6Yfx)
2. Open a ticket in the developer support channel
3. Describe your use case and the endpoints you need access to

API keys are issued manually and reviewed on a case-by-case basis.

---

## Using your API key

Include your API key in the `Authorization` header of every authenticated request:

```
Authorization: Bearer YOUR_API_KEY
```

**Example request:**

```
GET /functions/v1/tags HTTP/1.1
Host: ufncqneiavsfunaffqes.supabase.co
Authorization: Bearer YOUR_API_KEY
Content-Type: application/json
```

---

## Keeping your key secure

- Do not expose your API key in client-side code, public repositories, or browser console output
- Store it in an environment variable on your server
- If your key is compromised, contact GuildTags immediately to have it revoked and reissued

---

## OAuth2 (Discord login)

The GuildTags website uses Discord OAuth2 for user authentication. If you are building an application that needs to act on behalf of a GuildTags user (for example, to like servers or register a tag), you will need to implement the OAuth2 flow using Discord's API.

The OAuth2 redirect URI for GuildTags is:

```
https://guildtags.com/tags/
```

The Discord Client ID for GuildTags is:

```
1370457356554604727
```

Required OAuth2 scopes: `identify`

---

## Related pages

- [API Introduction](/documentation/en/api/introduction)
- [Endpoints](/documentation/en/api/endpoints)
