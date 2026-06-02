# Cattle Cash — Brand Deck (static site)

A zero-build static site. Just static files — deploy as-is.

## Structure
```
cattle-cash-site/
├── index.html      the deck (open in a browser, or deploy)
├── images/         all real art (logo, coin, characters, locations, Flipcash)
└── video/          put the trailer here as trailer.mp4 (shown in the hero)
```

## Add the trailer
Drop your video file into `video/` named **exactly** `trailer.mp4`:
```
video/trailer.mp4
```
- **21:9 recommended** (the brand's cinematic ratio — the hero frame is set to 21:9).
  If your file is **16:9**, change `aspect-ratio:21/9` to `16/9` in the `.video-frame`
  rule inside `index.html`.
- Optional: update the `poster="…"` image on the hero `<video>` to a still from the trailer.

## Deploy to Vercel (no config needed)
**Dashboard:** New Project → drag this folder in (or import the repo). Framework preset
**"Other"**, no build command, output directory **`./`**. Done — `index.html` serves at the root.

**CLI:**
```
npm i -g vercel
cd cattle-cash-site
vercel
```
Follow the prompts; accept the defaults (static, no build).
