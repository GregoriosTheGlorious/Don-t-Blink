# Don’t Blink

A one-tap timing game. Stop the dot inside the green zone. Every hit gets faster and tighter.

Plain HTML, CSS and JavaScript. No build step, no backend, no accounts, no tracking.
Best score is saved on the player’s own device.

## Put it online with GitHub Pages (free)

1. On github.com, create a new **public** repository (for example `dont-blink`).
2. Click **Add file → Upload files**, drag in everything from this folder (`index.html`, `manifest.webmanifest`, `sw.js`, the `.png` files and this README), then **Commit changes**.
3. Go to **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, and save.
4. After a minute or two, your game is live at `https://YOUR-USERNAME.github.io/dont-blink/`.
5. Open `index.html` in GitHub, click the pencil icon, and change `og:image` to the full address of the preview image, for example `https://YOUR-USERNAME.github.io/dont-blink/og-image.png`. Commit. This is what makes the link show a nice preview when you text or post it.

## Try it on a phone

Open the link, then use **Share → Add to Home Screen** on iPhone, or the browser menu → **Install app / Add to Home screen** on Android. It opens fullscreen and works offline.

## Good to know

- Best scores are stored per web address. If you move the game to a new address, players start again from zero.
- Vibration works on Android. iPhone browsers don’t allow it.
- After you edit `index.html`, players see the update the next time they open the game (the second open, because of the offline cache).

## Tuning the difficulty

Everything lives near the top of the script in `index.html`, between `LOGIC_START` and `LOGIC_END`:

- `difficulty()`: zone size and speed per round.
- `BLOCK`: the pattern of wide, normal and tight zones in each block of five rounds.
- `markerScale()`: how fast the ball shrinks.
- `scoreFor()`: points per hit.
- `shieldEarned()`: how many perfect hits earn a shield.
