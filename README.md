# AI Type Detective — Skills Bank | GitHub Pages (fixed)

Single `index.html`, no build, no keys. Upload `index.html` and `.nojekyll` to the root of a **public** GitHub repo, then Settings → Pages → Deploy from branch `main` / root.

## Trainer workflow
1. Open the published link → **Trainer Dashboard** → code `2026`.
2. A session is created automatically. Copy the **player link** (or the Arabic one) and send it. Press **New live session** for every class.
3. Watch players appear. **Reveal ranking** shows the leaderboard on the players' screens (your dashboard stays visible). **Refresh** rebuilds everything from the relay history. **Export CSV** at the end.

## What was fixed
- Game can start **without a session link** (solo mode, shown as `◌ SOLO`). Before, it refused with "Invalid session code".
- The code box accepts the **whole pasted link** (it used to be cut at 40 characters).
- The page no longer breaks when the browser **blocks storage** (in-app browsers, some privacy modes, iframes).
- Sending **retries automatically** instead of losing an answer; the `finish` message also carries all answers.
- If the live stream (SSE) is blocked, the dashboard falls back to **polling**; players only open the live stream when they finish (fewer connections to ntfy.sh).
- The dashboard shows **why** it is offline. The trainer's ranking overlay no longer covers the dashboard.
- Optional: `?relay=https://your-ntfy-server` on the link uses your own ntfy server.

## Limits
- Uses the free public relay `ntfy.sh`. Free limits are tight (per IP), so a big class on one Wi-Fi can hit them. Rehearse with 2 devices; keep **Download backup result** / **Import** as the safety net.
- Do not open the page inside a sandboxed preview (e.g. an artifact viewer): it blocks network calls to other sites. Use the GitHub Pages link.
- The `2026` code only hides the UI. Use fictional training data only.
