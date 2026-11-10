# Event Horizon

`index.html` is the whole site (about 0.4 MB). Each game is its own file in `games/`, and a game is only downloaded when someone opens it.
`event-horizon-full.html` is the same site as one self-contained file (the Download button hands this out).

## Put it online (GitHub Pages)
1. Make a new repository on GitHub and upload everything in this folder (keep the folder structure; the 16 folders inside `games/` can each be dragged in on their own).
2. Repository **Settings > Pages**, set **Source** to your main branch, root folder. Save.
3. Your site will be at `https://YOUR-NAME.github.io/YOUR-REPO/`. In Google Sites use **Embed > By URL** with that address.

## Use jsDelivr for the games (optional)
Open `index.html` in a text editor and change this line near the top:

    <meta name="eh-games" content="games/">

to a jsDelivr address, e.g.

    <meta name="eh-games" content="https://cdn.jsdelivr.net/gh/YOUR-NAME/YOUR-REPO@COMMIT/games/">

Use a commit hash (or a tag) instead of `main`: jsDelivr caches branch links for 12 hours, but commit links are cached essentially forever.
You can list several, separated by commas, and they are tried in order: `games/,https://cdn.jsdelivr.net/gh/...`.
Note: jsDelivr serves HTML as plain text, so only the games can come from it. `index.html` itself has to be on GitHub Pages (or any normal web host).
