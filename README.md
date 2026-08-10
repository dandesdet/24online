# 24 ONLINE — Landing (Hero)

Hero landing page for **24 ONLINE** (24TTL). Static site, no build step.

## Structure
```
index.html          # the page (markup + styles + JS)
fonts/              # Graphik RBC (body font)
```
External: **Unbounded** headline font loaded from Google Fonts CDN. Brand & marketplace logos are inline SVG inside index.html (needed for CSS filters/gradients).

## Run locally
Must be served (fonts won't load via file://):

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Features
- Rotating yellow headline (fade) across 3 phrases
- Liquid-glass badges, pills, ask-bar, floating banner
- Infinite seamless marketplace marquee (JS-built, viewport-adaptive, 50px gaps, edge fade)
- Update banner: 3 slides, X closes them one-by-one (cascade)
- Ask-bar: focus reveals 3 random prompt chips (overlay, no layout shift); click fills input; send activates on input

## Deploy
Any static host (Vercel, Netlify, GitHub Pages, Railway static). Point it at the folder root — `index.html` is the entry.
