# Rocco Fazio Real Estate

Personal real estate site — Pittsburgh North Hills.

## Stack
Static HTML/CSS/JS. Hosted on Netlify, source on GitHub.

## How to upload to GitHub (web, no command line)

1. Go to https://github.com/new and create a repo (e.g. `rocco-fazio-site`). Don't tick any "initialize" boxes.
2. On the empty repo page, click **uploading an existing file**.
3. Drag every file and the `assets/` folder from this bundle onto the page.
4. Commit message: "Initial site" → Commit.

## How to connect Netlify (automatic deploys)

1. https://app.netlify.com → Add new site → Import an existing project → GitHub
2. Authorize Netlify, pick the repo
3. Build settings: leave **build command blank**, publish directory = `.`
4. Deploy. Every future commit on `main` auto-deploys in ~30 seconds.

## How to edit after launch

- Quick text changes: open the file on github.com, click the pencil icon, edit, commit. Site rebuilds automatically.
- Big changes: clone the repo locally and use VS Code / GitHub Desktop.

## TODO before going fully live

1. **Google Reviews button** — in `index.html`, search for `YOUR_GOOGLE_REVIEW_LINK` and paste your real Google Business Profile review URL.
2. **CRM webhook** — bottom of `index.html`, find `CRM_ENDPOINT = ''` and paste a Zapier/Follow Up Boss/HubSpot webhook URL. Otherwise form submissions just log to the browser console.
3. **Social media links** — footer Instagram/Facebook/LinkedIn/YouTube links are placeholder `#`. Replace with real URLs.
4. **Neighborhood reel video** — currently a clickable thumbnail. To activate:
   - Upload your reel to YouTube (unlisted is fine)
   - Copy the video ID (the part after `v=` in the URL)
   - In `index.html`, search for `REPLACE_WITH_NEIGHBORHOOD_VIDEO_ID` and paste it in
   - Do the same for the three `REPLACE_WITH_TOUR_VIDEO_ID_*` placeholders if/when you add property tour videos

## Why no .mov file in this bundle?

The original `neighborhood-reel.mov` was 48 MB. GitHub's web upload caps at 25 MB per file and large binaries bloat your repo forever. Upload it to YouTube and embed via the video ID above — page loads faster, costs nothing, and works on every device (the `.mov` format only plays in Safari on iOS).

## File structure

```
/
├── index.html          # homepage
├── listings.html       # listings page
├── netlify.toml        # caching + security headers
├── .gitignore          # files to exclude from git
├── README.md           # this file
└── assets/             # images
    ├── highland-ave.jpeg
    ├── maitland-exterior.jpeg
    ├── maitland-kitchen.jpeg
    ├── mcaleer-aerial.jpeg
    ├── mcaleer-interior.jpeg
    └── negley-ave.jpeg
```
