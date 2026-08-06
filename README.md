# حافظوا — Store pages (Privacy & Support)

Static pages for **App Store** and **Google Play** listing URLs.

## Contents

| File | Purpose |
|---|---|
| `index.html` | Landing page |
| `privacy.html` | Privacy Policy (Arabic + English summary) |
| `support.html` | Support / FAQ |
| `styles.css` | Shared styles |

## Before you publish

1. Replace **every** `SUPPORT_EMAIL_HERE` in `privacy.html` and `support.html` with your real support email.
2. Optionally set the same email in `mailto:` links.

```bash
# from this folder
grep -R "SUPPORT_EMAIL_HERE" .
```

## Upload to GitHub Pages

### Option A — this repo (`/docs` or `/store-site`)

1. Commit the `store-site` folder (or move it to `/docs` at the repo root).
2. GitHub → **Settings** → **Pages**.
3. Source: Deploy from branch → `/docs` (or root if you put files there).
4. After deploy, your URLs will look like:

```
https://<user>.github.io/<repo>/privacy.html
https://<user>.github.io/<repo>/support.html
```

If the site is served from `store-site/`:

```
https://<user>.github.io/<repo>/store-site/privacy.html
https://<user>.github.io/<repo>/store-site/support.html
```

### Option B — dedicated repo (recommended for clean URLs)

1. Create a repo named `<user>.github.io` **or** any repo with Pages enabled.
2. Copy these files to the repo root (or `/docs`).
3. Enable Pages.
4. Use:

```
https://<user>.github.io/privacy.html
https://<user>.github.io/support.html
```

## Store Console fields

| Store field | URL |
|---|---|
| Privacy Policy | `…/privacy.html` |
| Support URL | `…/support.html` |
| Marketing (optional) | `…/index.html` |

## Local preview

```bash
cd store-site
python3 -m http.server 8080
# open http://localhost:8080
```
