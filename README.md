# Musfiq Rahman — 3D Scroll Portfolio

An episodic, scroll-driven self-introduction portfolio built with plain **HTML, CSS and JavaScript** plus **Three.js** (loaded from a CDN). No build step.

## Features
- Fixed 3D scene (wireframe torus knot, orbiting spheres, 2,200-star particle field) that glides and recolors as you scroll through 8 "episodes"
- Mouse parallax, cursor glow, 3D tilt cards, typed role headline, animated counters, blur-in reveals
- Episode dots + progress bar navigation
- Responsive layout, `prefers-reduced-motion` support, graceful fallback if WebGL is unavailable

## Run locally
Open `index.html` in a browser (internet is needed for Three.js and the font), or serve it:

```bash
npx serve .
# or
python -m http.server 8000
```

## Deploy on Vercel
This is a static site, so there is no build step.

1. Push the project to a GitHub repo with these files at the **root**: `index.html`, `style.css`, `vercel.json`, `README.md` (plus an optional `videos/` folder).
2. Go to [vercel.com/new](https://vercel.com/new), sign in with GitHub, and **Import** the repo.
3. Settings: **Framework Preset = Other**, leave **Build Command** and **Output Directory** empty, **Root Directory = ./**.
4. Click **Deploy**. You get a live `https://<project>.vercel.app` URL, and every `git push` to `main` redeploys automatically.
5. Optional: **Project → Settings → Domains** to add a custom domain.

Tip: keep each video under about 50 MB (GitHub rejects files over 100 MB). Compress with HandBrake or `ffmpeg -i in.mp4 -vcodec libx264 -crf 28 out.mp4`.

## Deploy on GitHub Pages
1. Create a repo named `musfiq180214.github.io` (or any repo) and add `index.html`, `style.css`, `README.md`.
2. Repo → **Settings → Pages** → deploy from the `main` branch, root folder.
3. Visit `https://musfiq180214.github.io`.

## Project videos
The **Projects** episode has a framed video player with a playlist. Edit the `VIDEOS` array in `index.html`; for each project set one of:

- `mp4: 'videos/demo.mp4'` — put the file in a `videos/` folder; it plays natively in the frame (most reliable).
- `embed: 'https://www.linkedin.com/embed/feed/update/urn:li:ugcPost:XXXX'` — on the LinkedIn post click **••• → Embed this post** and copy the `src` URL from the code.

If neither is set, the Play button opens the LinkedIn post in a new tab.

## Customize
- Text and links: edit the `<section>` blocks in `index.html`.
- Colors: CSS variables at the top of `style.css` and the `palette` array in the script.
- Object positions per episode: the `kf` keyframe array in the script.

## Contact
[Email](mailto:musfiq677@gmail.com) · [GitHub](https://github.com/musfiq180214) · [LinkedIn](https://www.linkedin.com/in/mrs180214/) · [Codeforces](https://codeforces.com/profile/musfiqrahman) · [LeetCode](https://leetcode.com/u/musfiq180214/)
