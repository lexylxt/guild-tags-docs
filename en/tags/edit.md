# Editing a tag

You can update your server's tag listing in the GuildTags directory at any time. This is useful when you change your clan tag on Discord, update your server name, or want to refresh your listing.

---

## Automatic sync

The GuildTags bot monitors your server for tag changes. When you update your clan tag through Discord's server settings, the bot will automatically sync the new tag to the directory within the next sync cycle (typically within a few minutes).

---

## Manual update

To force an immediate update without waiting for the sync cycle, use the following command in your server:

```
/update
```

This will re-read your server's current clan tag and server name from Discord and push the changes to the directory immediately. The bot will confirm once the update is complete.

> [!NOTE]
> Only server administrators can run `/update`. The command must be used in a channel where the bot has permission to send messages.

---

## What can be updated

The following information is automatically pulled from Discord when you run `/update`:

| Field | Source |
|---|---|
| Clan tag | Discord server settings |
| Server name | Discord server settings |
| Server icon | Discord server settings |
| Member count | Discord server data |

You cannot manually override these values — they always reflect what is set on Discord. This ensures the directory stays accurate.

---

## Updating your invite link

GuildTags uses a secure redirect system to protect server invite links from scrapers. The bot uses your server's default invite or the invite you provided at registration.

To update the invite link associated with your listing:

```
/setinvite <invite-link>
```

Replace `<invite-link>` with a valid Discord server invite URL. Permanent invites are recommended to avoid broken links.

---

## Featured status

If your server has a Featured plan, the featured badge and placement are managed through the GuildTags website. Contact support via the [Discord server](https://discord.com/invite/9CqvbP6Yfx) to manage your featured subscription.

---

## Related pages

- [Creating a tag](/documentation/en/tags/create)
- [Deleting a tag](/documentation/en/tags/delete)
- [Bot commands](/documentation/en/bot/commands)
