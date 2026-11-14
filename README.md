# Dog Dash

A browser canvas runner game. Open `index.html` in a browser, or serve the folder with GitHub Pages.

- 13 levels (Classic Meadow up to Crystal Cave), getting harder level by level, plus the gold **Chaos in the Mix** level (Insanity difficulty, 50 bones per run)
- Portals switch you between 7 forms: dog, ship, spider, flappy, balloon, frog and drone
- Bones are earned by playing (+1 every 400 points, golden bones, balloons, the drone star) and spent on skins, revives and Chaos runs. There is no real money anywhere in the game
- 29 dog skins, including patterned and accessory skins (Dalmatian, Beagle, Panda Pup, Pirate Pup, Royal Corgi…)
- A best score is kept for every level
- Keyboard: Space / ↑ / W jump · Esc or P pause · M mute · Enter play / retry
- Works offline once it has been opened from a hosted copy, and can be added to an iPad/iPhone home screen

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole game: markup, styles and script |
| `audio-data.js` | The embedded audio loops (base64 WAV, ~2.3 MB). Loaded before the game script; if it's missing, the game falls back to synthesized music |
| `sw.js` | Offline support. It fetches fresh files first and only uses its cache with no connection, so updates show up without changing anything here |
| `apple-touch-icon.png` | Home-screen icon and favicon |

## Working on it

`index.html` is small enough to open and edit normally. Don't edit `audio-data.js` by hand.

Saved progress lives in `localStorage` under keys starting with `dogdash_` (bones, skins, per-level bests, selected level, mute).
