# Dmytro Markey — personal site

A one-page personal site with a matchday / soccer-programme look. Plain HTML + CSS, plus a 10-line inline script for the match clock.
**No build step, no dependencies.**

```
index.html    the whole site
styles.css    everything visual, incl. scroll animations
images/       photos (see below)
```

## Run locally
Open `index.html` in a browser, or serve it:

```sh
python3 -m http.server 8000   # then open http://localhost:8000
```

## Add photos
Put these in `images/` with these exact names. Anything missing shows a mini-pitch "photo goes here" tile.

| file | where |
|---|---|
| `me.jpg` | player card at the top |
| `soccer.jpg`, `poker.jpg`, `hiking.jpg`, `friends.jpg` | the line-up |

Frames crop to 4:5, so portrait-orientation photos look best. Keep each under ~500 KB.

## Animations
- On load: pitch lines draw themselves, name rises, player card is dealt in (all browsers).
- On scroll (Chrome/Edge, Safari 26+, via CSS scroll-driven animations):
  progress line, sections open up, the four interests run into formation.
  Other browsers show the page static. Everything turns off for `prefers-reduced-motion`.

## Deploy to GitHub Pages
1. Create a repo named `<your-username>.github.io`
2. Push the contents of this folder
3. Live at `https://<your-username>.github.io` in a minute or two

## TODO
- [ ] Add the 5 photos
- [ ] Replace the placeholder interest captions with real details
- [ ] Add `paper.pdf` and uncomment the link in the Work section
