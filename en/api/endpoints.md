# Endpoints

This page documents all available GuildTags API endpoints.

---

## Tags

### Get tag count

Returns the total number of tags registered in the GuildTags directory.

```
GET /functions/v1/getTagCount
```

**Authentication:** None required

**Response:**

```json
{
  "count": 1284
}
```

---

### List tags

Returns a paginated list of all registered tags with their server information.

```
GET /functions/v1/tags
```

**Authentication:** API key required

**Query parameters:**

| Parameter | Type | Description |
|---|---|---|
| limit | integer | Number of results to return (default: 50, max: 100) |
| offset | integer | Number of results to skip for pagination (default: 0) |
| search | string | Filter results by tag or server name |
| sort | string | Sort order: `likes` or `created_at` (default: `created_at`) |

**Response:**

```json
{
  "data": [
    {
      "id": "1369767412995457034",
      "tag": "GT",
      "server_name": "Guild Tags",
      "likes": 42,
      "created_at": "2025-04-01T12:00:00Z"
    }
  ],
  "total": 1284,
  "limit": 50,
  "offset": 0
}
```

---

### Get a single tag

Returns details for a single registered server by its Discord server ID.

```
GET /functions/v1/tags/:server_id
```

**Authentication:** API key required

**Path parameters:**

| Parameter | Description |
|---|---|
| server_id | The Discord snowflake ID of the server |

**Response:**

```json
{
  "id": "1369767412995457034",
  "tag": "GT",
  "server_name": "Guild Tags",
  "likes": 42,
  "invite": "https://guildtags.com/go/?id=1369767412995457034",
  "created_at": "2025-04-01T12:00:00Z",
  "updated_at": "2025-06-01T08:30:00Z"
}
```

---

## Leaderboard

### Get leaderboard

Returns the top servers ranked by likes.

```
GET /functions/v1/leaderboard
```

**Authentication:** None required

**Query parameters:**

| Parameter | Type | Description |
|---|---|---|
| limit | integer | Number of results (default: 50, max: 50) |
| tab | string | `most_liked` or `most_voted` (default: `most_liked`) |

**Response:**

```json
{
  "data": [
    {
      "rank": 1,
      "id": "1369767412995457034",
      "tag": "GT",
      "server_name": "Guild Tags",
      "likes": 42
    }
  ]
}
```

---

## OAuth

### Exchange OAuth code

Exchanges a Discord OAuth2 authorization code for a GuildTags session token. Used after the Discord login redirect.

```
POST /functions/v1/oauth
```

**Authentication:** None required

**Request body:**

```json
{
  "code": "discord_authorization_code",
  "redirect_uri": "https://guildtags.com/tags/"
}
```

**Response:**

```json
{
  "user": {
    "id": "123456789012345678",
    "username": "alex",
    "avatar": "https://cdn.discordapp.com/avatars/..."
  },
  "role": "member"
}
```

---

## Related pages

- [Authentication](/documentation/en/api/authentication)
- [API Introduction](/documentation/en/api/introduction)
