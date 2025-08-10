# Minesweeper SFX Library

Put your sound files into the folders inside `sounds/`.
- You can have **multiple** files per folder (variants). Any mix of `.mp3`, `.wav`, `.ogg` is fine.
- After uploading files, update `manifest.json` so the site (and the Python game) knows what to load.

### Quick steps (GitHub web UI)
1. Create a new public repo named `Minesweeper-SFX`.
2. Click **Add file → Create new file** and paste the files from this scaffold (create each with the same paths/names).
3. Create the folders under `sounds/` and upload your audio files there (you can drag&drop in GitHub).
4. Either:
   - Manually edit `manifest.json` to list your files, **or**
   - Download `generator.html` (right‑click → Save as), open it locally, select your `sounds/` folder from your computer, copy the generated JSON back into `manifest.json` in GitHub.
5. (Optional) Enable **GitHub Pages**: Settings → Pages → Source: `Deploy from a branch` → `main` → `/root`. Your site will be at:
   `https://<your-user>.github.io/Minesweeper-SFX/`

### File tips
- Keep short SFX peaky but brief (100–500ms). Win/lose can be 0.5–2s. Ambient can loop (~30–120s).
- Normalize loudness so clips feel even.

### What Python will do
- Load `manifest.json` at startup.
- For each event (e.g., `flag`), pick a random file from that folder’s list, fetch it, and play.
