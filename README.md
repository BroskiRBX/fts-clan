# FTS Clan Site

Minecraft clan site built with Astro. Deploys to GitHub Pages automatically.

## Setup steps

### 1. Make a GitHub repo

Create a new repo on GitHub. Name it whatever, like `fts-clan`.

### 2. Update the config

Open `astro.config.mjs` and change two lines:

```js
site: 'https://YOURUSERNAME.github.io',  // your GitHub username
base: '/fts-clan',                         // your repo name
```

If you name your repo exactly `YOURUSERNAME.github.io`, then change `base: '/fts-clan'` to `base: '/'` instead.

### 3. Upload the files

Upload everything in this folder to your new repo. You can do this through the GitHub website by clicking "uploading an existing file" or use git from your computer.

### 4. Turn on GitHub Pages

In your repo, go to **Settings → Pages**. Under "Source" pick **GitHub Actions** (not "Deploy from branch"). That's it.

### 5. Wait

The workflow file in `.github/workflows/deploy.yml` will run automatically on every push. Give it about a minute. Check the **Actions** tab to watch it build. When it finishes, your site is live.

## Adding members

Open `src/data/members.js` and add a new block in the array:

```js
{
  id: "002",
  username: "TheirMcName",
  tag: "MEMBER",
  status: "ACTIVE",
  quote: "Their tag line here.",
},
```

The skin head pulls automatically from their Minecraft Java Edition username using the Mineatar API.

Push the change and it'll auto rebuild and deploy.

## Tag ideas

Any text works. Some suggestions:
- FOUNDER
- CO-LEADER
- OG
- VETERAN
- MEMBER
- INITIATE
- PVPER
- BUILDER
- REDSTONER

## Running locally (optional)

If you want to preview the site on your computer before pushing:

```bash
npm install
npm run dev
```

Then open `http://localhost:4321` in your browser.

## File structure

```
src/
  data/members.js       <- edit this to add members
  layouts/Base.astro    <- shared nav and footer
  pages/
    index.astro         <- home page
    members.astro       <- roster page
  styles/global.css     <- global styling
.github/workflows/
  deploy.yml            <- auto-deploy config
astro.config.mjs        <- edit this with your GitHub info
```
