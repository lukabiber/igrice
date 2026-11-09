# Brunoli

Little games for little hands, in English and Croatian. Plain HTML, CSS and JS with no build step, hosted on GitHub Pages at https://lukabiber.github.io/igrice/ and added to the iPhone Home Screen as a full screen app.

## What's here

| Path | What it is |
|---|---|
| `index.html` | The list of games (the app's home page) |
| `prstici/` | Prstići: count to ten on your fingers |
| `boje/` | Boje: colors. Paint (tap to splash a color) and Find (pop the balloon the voice asks for) |
| `manifest.webmanifest`, `icons/` | Home Screen name and icon |
| `sw.js` | Offline support |

## Croatian pronunciation

Each game has the Croatian words twice: the real spelling (read by a Croatian voice such as Lana) and a phonetic spelling (read by the English voice when the phone has no Croatian voice). In Prstići that's `HR_SAY` and `HR_SOUND`; in Boje it's the `hr` and `sound` fields in `COLORS`.

## Adding a game

1. Make a folder with an `index.html`, for example `oblici/index.html`. Copy the `<head>` tags from `boje/index.html` so it stays full screen on the phone, and add a link back to `../`.
2. Add a tile for it to the list in `index.html`.
3. Add the folder (`'oblici/'`) to `CORE` in `sw.js` and bump `CACHE` (`brunoli-v3`) so it works offline too.
4. Commit and push to `main`. GitHub Pages publishes it within a minute or two, and the app picks it up the next time it opens online.

## Trying it locally

Any static server works, for example `npx serve .` from this folder.
