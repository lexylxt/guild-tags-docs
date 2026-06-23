# Creating a tag

Before registering your server in the GuildTags directory, your Discord server must already have a clan tag set. This page explains how to set up a tag on Discord and then register it with GuildTags.

---

## Step 1 — Set a clan tag on Discord

Clan tags are configured through Discord's server settings. You must be the server owner or have the Manage Server permission.

1. Open your Discord server and go to **Server Settings**
2. Navigate to **Clan** in the left sidebar
3. Follow the prompts to enable the clan system and choose your tag (two to five characters)
4. Save your changes

Your chosen tag will now appear next to members' names in your server.

> [!NOTE]
> Discord's clan tag system may require your server to meet certain criteria such as a minimum member count or community status. Check Discord's documentation if the Clan section is not visible in your settings.

---

## Step 2 — Add the GuildTags bot

If the bot is not already in your server, add it from the [Discord Application Directory](https://discord.com/application-directory/1370457356554604727) or use the Add Bot button on the GuildTags website.

The bot needs the following permissions to function correctly:

- Read Messages and Message History
- Send Messages
- Use Slash Commands
- Read server member information

---

## Step 3 — Register your tag

Once the bot is in your server, use the following slash command:

```
/register
```

The bot will automatically read your server's current clan tag from Discord and submit it to the directory. You will receive a confirmation message with a link to your listing on the website.

> [!TIP]
> Only server administrators can run `/register`. If the command does not appear, check that the bot has the Use Application Commands permission in the channel you are using.

---

## What happens after registration

Your server tag will appear in the public directory within a few seconds of registration. The listing will include:

- Your clan tag
- Your server name and icon
- A secure join link routed through the GuildTags redirect system
- A like counter starting at zero

The listing is visible to any logged-in user on [guildtags.com](https://guildtags.com).

---

## Updating your tag

If you change your clan tag on Discord after registration, the bot will detect the change automatically at the next sync cycle. You can also force an immediate update using:

```
/update
```

See [Editing a tag](/documentation/en/tags/edit) for more details.

---

## Related pages

- [What is a tag?](/documentation/en/tags/what-is-a-tag)
- [Editing a tag](/documentation/en/tags/edit)
- [Bot setup](/documentation/en/bot/setup)
