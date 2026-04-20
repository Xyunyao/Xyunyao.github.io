# Yunyao's personal website

A minimal static site (HTML + CSS) for hosting on GitHub Pages.

## Files

- `index.html` — about / research / publications / contact
- `blog.html` — blog index
- `posts/hello-world.html` — sample blog post
- `style.css` — all styling
- `.nojekyll` — tells GitHub Pages to serve files as-is (no Jekyll processing)

## Deploy to GitHub Pages (5 minutes)

### 1. Create the repo

1. Go to <https://github.com/new>
2. Repository name: **`Xyunyao.github.io`** (must match your username exactly for a user site)
3. Set it to **Public**
4. Do **not** initialize with a README (we already have one)
5. Click **Create repository**

### 2. Push the files

Open a terminal in this folder and run:

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/Xyunyao/Xyunyao.github.io.git
git push -u origin main
```

If prompted to authenticate, use a **personal access token** instead of a password: <https://github.com/settings/tokens>

### 3. Enable GitHub Pages

1. Go to your repo → **Settings** → **Pages**
2. Under **Build and deployment**, set **Source** to `Deploy from a branch`
3. Branch: `main`, folder: `/ (root)` → **Save**
4. Wait about 1 minute

Your site will be live at:

**<https://xyunyao.github.io>**

## Editing content

Look for `TODO` comments in `index.html` — those mark spots to personalize:

- One-line tagline
- Bio paragraph
- Research interests (bullet list)
- Publications list
- Google Scholar / ORCID URLs
- Office location

Re-deploy after edits by running:

```bash
git add .
git commit -m "Update content"
git push
```

GitHub Pages re-deploys automatically within a minute.

## Adding a new blog post

1. Copy `posts/hello-world.html` to a new file, e.g. `posts/my-new-post.html`
2. Change the `<title>`, `<h1>`, date, and body content
3. Add an entry to the `<ul class="post-list">` in `blog.html`
4. Commit and push

## Using a custom domain (optional)

1. Add a `CNAME` file in the repo root containing just your domain (e.g. `yunyao.com`)
2. In your DNS, add a CNAME record pointing to `xyunyao.github.io`
3. In repo Settings → Pages, enter your custom domain
