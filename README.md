# sc-blueprint-bot

The ultimate Star Citizen (tm) blueprint companion. Snap a Fabrication Kiosk screenshot — AI extracts everything: materials, quantities, stats, fabrication times. Query your crew's shared database by name, category, or material. Blueprint-styled PDF reports. Crafter tracking. Per-server setup in seconds.

# Adding SC Blueprint Bot to Your Server

Welcome! This guide walks you through adding SC Blueprint Bot to your Discord server and getting it set up in a few minutes.

**You will need:** the **Manage Server** permission on the Discord server you want to add the bot to.

---

## Step 1 — Invite the bot

Click the invite link provided by the bot owner (or find it on the project page).

You will be taken to Discord's authorisation page:

1. Select your server from the **Add to Server** dropdown
2. Click **Continue**
3. Review the permissions — these are all required for the bot to work:
   - *View Channels* — to read messages in your channels
   - *Send Messages* — to post responses and embeds
   - *Embed Links* — to send rich blueprint cards
   - *Attach Files* — to attach PDF reports
   - *Read Message History* — to read channel history
   - *Manage Messages* — to auto-delete upload screenshots after processing
4. Click **Authorise**
5. Complete the CAPTCHA if prompted

The bot will join your server. You should see a welcome message appear shortly.

---

## Step 2 — Create your channels

The bot needs three dedicated text channels. You can use existing channels or create new ones — the names are completely up to you. You will need:

| Channel | Purpose |
|---|---|
| **Upload channel** | Where members post Fabrication Kiosk screenshots |
| **Query channel** | Where members search for blueprints |
| **Database channel** | Where the bot posts results and confirmations |

> 💡 **Tip:** Consider restricting posting in the database channel to the bot only — this keeps the output clean and easy to read.

---

## Step 3 — Configure the bot

Run the `/blueprint-config` command and select your three channels using the channel pickers:

```
/blueprint-config upload_channel:#your-upload query_channel:#your-query database_channel:#your-database
```

The bot will reply with a confirmation showing the channels that have been saved. This response is only visible to you.

> `/blueprint-config` requires the **Manage Server** permission. Regular members cannot change the bot's channel settings.

---

## Step 4 — Start using the bot

**Upload a blueprint:**
Post a Star Citizen Fabrication Kiosk screenshot in your upload channel. The bot will process the image automatically and post a confirmation embed in your database channel. The original screenshot is deleted.

**Search for a blueprint:**
Type any item name, category, or material in your query channel. Examples:

| You type | Bot returns |
|---|---|
| `S-38 Pistol` | Full blueprint card + PDF |
| `Armor` | All armor blueprints + PDF |
| `Titanite` | All blueprints using Titanite + PDF |
| `S-38 Pistol quality analysis` | Quality impact analysis PDF |

**Use slash commands:**
Type `/blueprint` to see all available commands. Key ones to start with:

| Command | What it does |
|---|---|
| `/blueprint-help` | Show all commands and usage examples |
| `/blueprint-stats` | Live database summary |
| `/blueprint-search` | Search by item name with autocomplete |
| `/blueprint-category` | Browse by category |
| `/blueprint-config` | View or update your channel setup |

---

## Changing your channel setup

You can update any channel at any time by running `/blueprint-config` again. You only need to supply the channels you want to change — the others stay as they are:

```
/blueprint-config upload_channel:#new-channel
```

To view your current configuration without making changes, run `/blueprint-config` with no parameters.

---

## Troubleshooting

| Problem | Fix |
|---|---|
| Bot joined but no slash commands appear | Wait up to 1 minute and refresh Discord (Cmd+R / Ctrl+R) |
| Bot doesn't respond in channels | Run `/blueprint-config` to set up your channels |
| Upload processed but confirmation went to wrong channel | Re-run `/blueprint-config database_channel:#correct-channel` |
| `/blueprint-config` not visible to you | You need the **Manage Server** permission |
| Bot processed the image but found no blueprint data | Make sure the screenshot shows the full Fabrication Kiosk panel clearly |

---

*SC Blueprint Bot is a community project for Star Citizen players. It is not affiliated with or endorsed by Cloud Imperium Games.*

---

Try before you try? Come and join us on the development server to try it out: https://discord.gg/tHumPB9d 

---

If you like what you see,  follow the link below to install the bot on your own server or on that of your Org.

Discord Invite Link: https://discord.com/oauth2/authorize?client_id=1493936820143259720
