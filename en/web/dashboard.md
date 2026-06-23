# Directory

The GuildTags directory is the core feature of the website. It displays all registered Discord servers sorted and searchable by their clan tag.

---

## Accessing the directory

The directory is available at [guildtags.com/tags](https://guildtags.com/tags). A Discord login is required to view listings. This prevents automated scraping of server invite links and ensures that join links are only accessible to real users.

---

## Logging in

Click the **Login with Discord** button on the directory page. You will be redirected to Discord's OAuth2 authorisation page. GuildTags only requests your public profile information (username and avatar) — it does not access your messages, servers, or any private data.

After logging in, you are returned to the directory and can browse all listings.

---

## Directory layout

Each server is displayed as a row in a table with the following columns:

- **Badge** — verified or featured status indicator
- **Tag** — the Discord clan tag registered for that server
- **Server** — the server name and icon
- **Join** — a button to join the server via the secure redirect
- **Server ID** — the Discord snowflake ID of the server
- **Likes** — the total number of likes from GuildTags users

---

## Adding your server

To add your server to the directory, paste a Discord invite link in the input bar at the top of the directory page and click Add Server, or use the `/register` bot command from within your Discord server.

See [Creating a tag](/documentation/en/tags/create) for full instructions.

---

## Secure join links

Clicking the Join button on any listing routes you through the GuildTags redirect at `/go/`. This system validates the destination before forwarding you to Discord, protecting invite links from being harvested in bulk by automated tools.

The redirect is nearly instantaneous. You will land on the Discord invite page after a brief check.

---

## Related pages

- [Leaderboard](/documentation/en/web/leaderboard)
- [Account](/documentation/en/web/account)
- [Tag list](/documentation/en/tags/list)
