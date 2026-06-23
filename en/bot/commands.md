# Commands

All GuildTags bot commands are slash commands. Type `/` in any channel where the bot has permission to see a full list of available commands with descriptions.

---

## Registration commands

### /register

Registers your server in the GuildTags directory. The bot reads your current clan tag and server details from Discord and creates a public listing.

**Required permission:** Administrator

**Usage:**
```
/register
```

---

### /unregister

Removes your server's listing from the GuildTags directory. The bot will ask for confirmation before proceeding.

**Required permission:** Administrator

**Usage:**
```
/unregister
```

> [!WARNING]
> This action is permanent. All likes accumulated on your listing will be lost.

---

### /update

Forces an immediate sync of your server's tag and details to the directory. Useful if you recently changed your clan tag on Discord and do not want to wait for the automatic sync.

**Required permission:** Administrator

**Usage:**
```
/update
```

---

## Configuration commands

### /setinvite

Sets or updates the invite link associated with your directory listing. Use a permanent invite to avoid broken links.

**Required permission:** Administrator

**Usage:**
```
/setinvite <invite-url>
```

**Example:**
```
/setinvite https://discord.gg/your-invite-code
```

---

### /setchannel

Designates a channel for GuildTags bot notifications. After running this command, the bot will send all status messages and update confirmations to the specified channel.

**Required permission:** Administrator

**Usage:**
```
/setchannel #channel-name
```

---

## Information commands

### /status

Displays the current registration status of your server, including the active tag, invite link, last sync time, and like count.

**Required permission:** None (visible to all members)

**Usage:**
```
/status
```

---

### /info

Shows general information about the GuildTags bot, including its version and a link to this documentation.

**Required permission:** None

**Usage:**
```
/info
```

---

### /help

Displays a summary of all available commands.

**Required permission:** None

**Usage:**
```
/help
```

---

## Command availability

Slash commands are only available in servers where the bot has been added with the Use Application Commands permission. If a command does not appear in your command list, check the bot's channel-level permissions.

---

## Related pages

- [Bot setup](/documentation/en/bot/setup)
- [Permissions](/documentation/en/bot/permissions)
- [Editing a tag](/documentation/en/tags/edit)
