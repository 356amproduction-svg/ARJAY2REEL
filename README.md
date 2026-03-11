# ARJAY2REEL — Visual Production Portfolio

Live site: `https://<your-username>.github.io/ARJAY2REEL-SITE`

## Repo Structure
```
ARJAY2REEL-SITE/
├── index.html          ← The entire site (HTML + CSS + JS in one file)
├── .gitignore
├── README.md
└── assets/
    ├── images/         ← All 88 photos (GitHub-friendly names)
    │   ├── img-9667.jpg        ← hero image
    │   ├── img-9286.jpg        ← work card 1
    │   ├── img-9538.jpg        ← gallery slot 1
    │   └── ...
    ├── logo.jpg
    └── logo-v1.jpg
```

## How to Refresh / Swap a Photo

### Replace a photo (same slot, new image):
1. Rename your new photo to match the existing filename — e.g. `img-9667.jpg`
2. Drop it into `assets/images/`
3. Commit and push — GitHub Pages updates automatically

### Change which photo appears in which slot:
Open `index.html` and search for `Photo config` to find this block:

```js
const PHOTOS = {
  hero:    'assets/images/img-9667.jpg',
  work: [
    'assets/images/img-9286.jpg',   // work card 1 — Studio Session
    'assets/images/img-9289.jpg',   // work card 2 — Golden Hour
    'assets/images/img-9300.jpg',   // work card 3 — Motion
    'assets/images/img-9305.jpg',   // work card 4 — Event
    'assets/images/img-9332.jpg',   // work card 5 — Commercial
    'assets/images/img-9374.jpg',   // work card 6 — Music Video
    'assets/images/img-9422.jpg',   // work card 7 — Documentary
    'assets/images/img-9425.jpg',   // work card 8 — BTS
  ],
  gallery: [
    'assets/images/img-9538.jpg',   // gallery 1 — Photography
    'assets/images/img-9549.jpg',   // gallery 2 — Music Video
    'assets/images/img-9572.jpg',   // gallery 3 — BTS
    'assets/images/img-9578.jpg',   // gallery 4 — Photography
    'assets/images/img-9593.jpg',   // gallery 5 — Music Video
    'assets/images/img-9596.jpg',   // gallery 6 — BTS
    'assets/images/img-9600.jpg',   // gallery 7 — Photography
    'assets/images/img-9626.jpg',   // gallery 8 — Music Video
    'assets/images/img-9633.jpg',   // gallery 9 — BTS
  ],
  about: 'assets/images/img-8694-edited.jpg',
};
```

Swap any filename to any file in `assets/images/`, commit, and push.

## Deploy to GitHub Pages

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Source: **Deploy from a branch** → `main` → `/ (root)`
4. Save — site goes live at `https://<username>.github.io/<repo-name>`

## Run Locally
```bash
python3 -m http.server 8080
# open http://localhost:8080
```

## Photo Naming Convention
All images use lowercase-with-hyphens naming:
- `img-XXXX.jpg` — camera photos
- `img-XXXX-alt.jpg` — alternate version of same shot
- `img-XXXX-edited.jpg` — edited/retouched version
- `photo-001.jpg` — unlabeled shots (originally UUID filenames)
- `ai-render-01.png` — AI-generated renders
- `design-cover.jpg` — graphic design assets

## Notes
- Video reel (`.mov`/`.mp4`) is excluded from git — exceeds GitHub's 100MB file limit.
  Host on YouTube or Vimeo and paste the embed link into the HTML.
- You can still click any image slot in the browser to temporarily override it (saves to localStorage).
