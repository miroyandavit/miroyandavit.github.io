# Davit Miroyan — personal site (v2)

Plain HTML/CSS, no build tools. Three pages, matching the prototypes we
worked through together: About, Blog, Gallery.

## File map

```
index.html              About page — photo + intro, black accent, Blog/Gallery buttons
blog/index.html          "Davit's Blog" — list of posts
blog/first-post.html     sample post — copy this to write a new one
gallery.html             "Davit's Gallery" — 2-column photo grid, up to 10 photos, no captions
assets/css/style.css      all styling
assets/img/               photos live here
robots.txt, sitemap.xml   SEO plumbing
```

Fonts: Newsreader (serif, headings/name) + Work Sans (body/buttons), loaded
from Google Fonts — no local font files needed.

## 1. Add your real photos

- Save your headshot as `assets/img/profile.jpg`. The About page already
  points at this filename — no HTML edit needed, it just starts working.
- For the gallery, save up to 10 photos as `assets/img/gallery-1.jpg`,
  `gallery-2.jpg`, etc. `gallery.html` already references `gallery-1.jpg`
  through `gallery-5.jpg` — for more than 5, copy an `<img>` line in
  `gallery.html` and bump the number.
- Until real files exist, each `<img>` falls back to a placeholder
  automatically (via `onerror`), so the site never shows a broken image.

## 2. Put it on GitHub Pages

1. Create a public GitHub repo named exactly `miroyandavit.github.io`
   (this gives you the clean root URL instead of a `/repo-name/` path).
2. Push these files:
   ```
   cd personal-website-v2
   git init
   git add .
   git commit -m "initial site"
   git branch -M main
   git remote add origin https://github.com/miroyandavit/miroyandavit.github.io.git
   git push -u origin main
   ```
3. In the repo: **Settings → Pages** → Source: "Deploy from a branch",
   branch `main`, folder `/ (root)`.
4. Visit `https://miroyandavit.github.io/` after a minute or two.

## 3. Getting found in search

Same advice as before — a new site doesn't get crawled automatically for
a while, so ask for it directly:

1. Add the site to [Google Search Console](https://search.google.com/search-console).
2. Submit `sitemap.xml` (already included).
3. Use **URL Inspection** → **Request indexing** on the homepage.
4. Link to the site from somewhere already indexed (GitHub profile README,
   Google Scholar, etc.) — Google discovers new pages partly by following
   links from pages it already knows.

## Note on contact info

The approved design doesn't have a dedicated contact section, so I added
your email as a quiet footer link on every page (`mailto:miroyan7davit@gmail.com`)
so there's still a way to reach you. Delete the `<footer>` block from any
page if you'd rather not have it.
