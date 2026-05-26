# FTS Site

## How to add a member

Open `members.json` and add a new block. That's the only file you ever touch.

Right now it looks like this:

```json
[
  {
    "name": "8rahski",
    "rank": "Founder"
  }
]
```

To add a member, put a comma after the closing `}` and add another block:

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

## How to remove a member

Delete their block (including the comma before or after it). Make sure the rest of the file still has commas between blocks but NOT after the last one.

## Editing on GitHub directly

1. Go to your repo
2. Click `members.json`
3. Click the pencil icon (edit)
4. Make your changes
5. Scroll down, click Commit changes
6. Wait 30 seconds, refresh your live site

That's literally it. No HTML, no CSS, no code.

## Rules for names

- The `name` must be an exact Minecraft Java username so the skin head loads
- The `rank` can be any text you want (Founder, OG, Member, Builder, etc)
- Every block needs both `name` and `rank` in quotes
- Commas between blocks, no comma after the very last block
