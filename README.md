# FTS Site

## How to add a member

Open `members.json` and add a new block.

```json
[
  {
    "name": "8rahski",
    "rank": "Founder"
  },
  {
    "name": "NewPersonHere",
    "rank": "Member"
  }
]
```

Commas between blocks, no comma after the last one.

## How to set up the Join page (IMPORTANT)

The Join page has a form that sends applications to your Discord. You need to set up a webhook first:

### Step 1: Create the Discord webhook

1. Open your Discord server
2. Right-click the channel where you want applications to appear, then click Edit Channel
3. Click Integrations in the left sidebar
4. Click Webhooks then New Webhook
5. Name it whatever (like "FTS Applications")
6. Click Copy Webhook URL

### Step 2: Add the URL to your site

1. Open `join.html`
2. Find this line near the bottom (around line 175):

```js
const WEBHOOK_URL = "PASTE_YOUR_WEBHOOK_URL_HERE";
```

3. Replace PASTE_YOUR_WEBHOOK_URL_HERE with the URL you copied
4. Save the file and upload to your repo

It should look like:

```js
const WEBHOOK_URL = "https://discord.com/api/webhooks/123456789/abcdefg-very-long-string";
```

Now when someone fills out the form, it'll post their application to your Discord channel with their info and skin head as a thumbnail.

### Security note

The webhook URL will be visible in your site's code (since GitHub Pages is public). This is fine for low-stakes stuff like a clan application form, but it means trolls could spam your Discord if they find the URL. If that happens, just delete the webhook in Discord settings and make a new one.

## Files in this site

- index.html - home page
- roster.html - members list
- join.html - application form
- members.json - edit this to add/remove members
- style.css - styling
- README.md - this file
