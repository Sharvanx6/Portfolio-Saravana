# Saravana — Portfolio

A single-file modern portfolio. No build step, no dependencies — drop on any static host.

## Structure
```
site/
├── index.html          ← The whole site (~120 KB inc. CSS + JS)
├── README.md
└── assets/
    └── images/          ← Drop your images here
```

## Routes (hash-based)
| Page | URL |
|---|---|
| About (default) | `#about` |
| Projects listing | `#projects` |
| Ford VSU | `#projects/vsu` |
| JPMC Loan App | `#projects/loan-app` |
| Wells Fargo MIS | `#projects/smis` |
| QikPod Smart Locker | `#projects/smart-locker` |
| Livfit | `#projects/livfit` |
| Artworks | `#artworks` |
| Resume | `#resume` |

## Adding your images

### Profile photo
Save as `assets/images/profile.jpg` (any reasonable size; will be cropped to fit).

### Project case-study images
Each `<div class="case-img">` has a `<div class="case-img__caption">` describing what it represents. To swap a placeholder with a real image, change:
```html
<div class="case-img"><div class="case-img__caption">Visual sequence flow</div></div>
```
to:
```html
<div class="case-img"><img src="assets/images/ford-visual-sequence.png" alt="Visual sequence flow"></div>
```

(Add this CSS line once at the top of the case-img styles if it isn't already there: `.case-img img { width: 100%; height: 100%; object-fit: cover; }`.)

### Artwork images
Same pattern — replace `<div class="art-card__label">…</div>` inside each `.art-card`.

## Deploy
Drop the `site/` folder onto:
- **Netlify** — drag the folder onto their drop zone
- **GitHub Pages** — push to a repo, enable Pages
- **Vercel** — drag & drop, or git push
- **Cloudflare Pages** — zero config

That's it.
