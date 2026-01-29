# FitScout — Prototype

This is a static, client-side prototype of FitScout — an AI-powered sports talent assessment UI.

Open `index.html` in a browser to explore the prototype. Features implemented:
- Landing page with animated CTA
- Login (dummy, stored in localStorage)
- Home with big animated cards
- Take Test: upload video -> fake analysis -> dummy results
- Practice Mode: webcam preview + placeholder feedback
- Dashboard: dummy history, animated badges, progress bar

Notes:
- No backend. Auth is simulated via `localStorage`.
- Browser must allow webcam access for Practice Mode.

Theme and logo
- A simple SVG logo is at `img/logo.svg` and used in the navbar.
- Toggle the Light/Dark theme using the moon button in the top-right; theme preference is saved in `localStorage`.

View on any phone (LAN / GitHub Pages / ngrok)

Option 1 — Quick LAN server (Windows PowerShell):

1. Open PowerShell in this folder: `c:\Users\DELL\Desktop\prototype`
2. Run the helper script: `.\serve-local.ps1`
3. The script will print a `http://localhost:8000` URL and one or more `http://<your-lan-ip>:8000` URLs.
4. On your phone (connected to same Wi‑Fi), open the LAN URL printed by the script.

Option 2 — npm http-server:

1. Install `http-server` temporarily and run:

```powershell
npx http-server -p 8000 -a 0.0.0.0
```

2. Open `http://<your-lan-ip>:8000` on your phone.

Option 3 — ngrok (public URL):

1. Install ngrok and run your local server (from option 1 or 2).
2. Run: `ngrok http 8000` and use the https URL it provides on any device.

Option 4 — GitHub Pages (host for free):

1. Push this repository to GitHub.
2. Enable GitHub Pages in the repository settings (use the `main` branch / `root` folder).
3. Visit the GitHub Pages URL from any phone.

Notes on webcam: some browsers require HTTPS to use the camera. Using ngrok gives an `https://` URL which will allow camera access from your phone.

