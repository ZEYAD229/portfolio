# Zeyad Elsaid — Portfolio | بورتفوليو زياد السعيد

Static, single-page personal brand site (HTML/CSS/JS, no build step).
موقع ثابت من صفحة واحدة، مفيش خطوات build.

## Structure | الهيكل
```
index.html          # the site + editable data block (CONFIG, PROJECTS)
favicon.svg
assets/profile  events  media  production  branding  music  logos
.github/workflows/pages.yml   # auto-deploy to GitHub Pages
```

## Run locally | التشغيل محليًا
Open `index.html` in a browser, or: `python3 -m http.server 8000` then visit http://localhost:8000

## Deploy on GitHub Pages | النشر
1. Create a repo, upload all files (keep the `.github` folder), push to `main`.
2. Repo **Settings → Pages → Source: GitHub Actions**.
3. Every push to `main` redeploys. URL: `https://<username>.github.io/<repo>/`
   (name the repo `<username>.github.io` for a root URL).

## Edit content | التعديل
Everything editable is in the script at the bottom of `index.html`, between `EDIT HERE` markers.

- **Portrait:** put the photo in `assets/profile/`, then set `CONFIG.portrait:"assets/profile/zeyad.jpg"`.
- **Add a project:** add an object to `PROJECTS`:
  `{t:"Title",c:"Category",y:"2026",l:"Cairo",img:"assets/events/photo.jpg"}`
  Add only documented facts; leave out role if unconfirmed.
- **Showreel:** set `CONFIG.showreel` to an embed URL, e.g. `https://www.youtube.com/embed/VIDEO_ID` or `https://player.vimeo.com/video/ID`.
- **Music:** put the file in `assets/music/`, set `CONFIG.audio:"assets/music/track.mp3"`.
- **Social links:** fill `CONFIG.social` (LinkedIn, Instagram, YouTube).
- **Logos:** drop files in `assets/logos/` (logo wall currently shows names only).
- **Social preview:** add a 1200×630 image at `assets/branding/og.jpg`.
- Compress images before upload (≈200–400 KB each) for speed.

## Notes
- Impactra and "لما تلاقي" are presented as in development. Do not mark them as delivered/aired unless true.
- Not yet built: Arabic language switch, per-project gallery pages.
