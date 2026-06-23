# Permissions

When you add the GuildTags bot to your server, Discord will ask you to grant a set of permissions. This page explains what each permission is used for and why it is necessary.

---

## Required permissions

| Permission | Why it is needed |
|---|---|
| Read Messages / View Channels | The bot needs to read channels to respond to slash commands |
| Send Messages | Required to send confirmation messages, status updates, and error responses |
| Use Application Commands | Allows the bot's slash commands to appear and function in your server |
| Read Server Members | Used to verify that the user running a command has administrator status |

---

## Optional permissions

These permissions are not strictly required but improve the bot's functionality:

| Permission | Why it is useful |
|---|---|
| Manage Webhooks | Allows the bot to send formatted notifications via webhook rather than as a bot message |
| Embed Links | Needed to send rich embed messages with links to your listing |
| Attach Files | Used when the bot sends a summary card of your registration |

If you denied any of these during setup and want to re-enable them, go to **Server Settings > Integrations**, find the GuildTags bot, and edit its permissions.

---

## Administrator permission

The GuildTags bot does **not** require the Administrator permission. Granting it is not recommended. The bot can perform all its functions with the specific permissions listed above.

---

## Channel-level permissions

Some servers restrict bot activity to specific channels. If slash commands are not appearing, check that the GuildTags bot has the Use Application Commands permission in the channels where you want to use it. This can be set per-channel under **Channel Settings > Permissions**.

---

## What the bot does NOT do

The GuildTags bot does not:

- Read or store the content of your members' messages
- Access private channels unless explicitly granted permission
- Modify server settings, roles, or member data
- Send unsolicited messages or DMs to members

The bot's sole functions are to register and sync your tag listing, respond to slash commands, and send notifications about your directory entry.

---

## Related pages

- [Bot setup](/documentation/en/bot/setup)
- [Commands](/documentation/en/bot/commands)
- [Privacy Policy](/privacy)
