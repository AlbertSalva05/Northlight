# Northlight Camera Co. — v1.0.0
Static site: the homepage (`index.html`) and a 404 page. Built from `Northlight.dc.html` by `build/build-deploy.js`; never hand-edit.

## Files
- `index.html`: homepage (rendered in the browser by `assets/js/support.js`; needs JavaScript).
- `404.html`: static, noindex.
- `assets/css/northlight-tokens.css`, `assets/js/support.js`: linked with `?v=` content hashes.
- `assets/icons/`, `favicon.ico`, `site.webmanifest`, `assets/img/common/img_og_01.png` (1200×630 share image).
- `robots.txt`, `sitemap.xml`, `_headers` (cache rules for Netlify / Cloudflare Pages), `.gitignore`, `.gitattributes`.

## Before launch
- Replace `https://www.northlightcamera.example` with the live domain in `index.html`, `robots.txt` and `sitemap.xml` (set `SITE` in `build/build-deploy.js` and rebuild).
- Replace the placeholder logo mark and share image with final brand artwork.

## Deploy
1. Delete the old files in the repo (keep `.git`).
2. Copy in everything from this folder, including the dotfiles.
3. Push with Git (not web drag-and-drop).
4. Clear the host's build cache and redeploy.
5. Check that `<meta name="build" content="v1.0.0">` appears in the live page source.
- Host: any static host. `_headers` works on Netlify and Cloudflare Pages; on another host, set the same rules (assets cached for a year, immutable; HTML no-cache).
