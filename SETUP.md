# Sikuan Yan — Personal Website (al-folio)

This site is built on the [al-folio](https://github.com/alshedivat/al-folio) Jekyll theme,
already personalized with your CV.

## What's customized
- **`_config.yml`** — name, description, site URL (`https://yansikuan.github.io`).
- **`_pages/about.md`** — homepage bio.
- **`_news/`** — News items (shown on the homepage and `/news/`).
- **`_bibliography/papers.bib`** — your 7 publications (top 3 marked `selected` show on the homepage).
- **`_pages/service.md`** — Talks & Service page.
- **`_data/cv.yml`** + **`_pages/cv.md`** — rendered CV page (also links to `assets/pdf/cv_sikuanyan.pdf`).
- **`_data/socials.yml`** — email + CV link.
- Navbar trimmed to: **news · publications · talks & service · cv**.

## TODO (fill these in)
1. **Profile photo** — replace `assets/img/prof_pic.jpg` with your headshot (keep the filename).
2. **Google Scholar** — in `_data/socials.yml`, set `scholar_userid:` to the `user=` value from your Scholar URL.
3. **LinkedIn** — in `_data/socials.yml`, set `linkedin_username:` (and the same in `_data/cv.yml`).
4. **Invited talks** — add them to `_pages/service.md`.
5. (optional) Add paper links: `pdf`, `arxiv`, `code`, `html` fields per entry in `_bibliography/papers.bib`.

## Preview locally (Docker — recommended, no Ruby needed)
```bash
cd /Users/yansikuan/Desktop/personal-website
docker compose up
# open http://localhost:8080
```

## Deploy to GitHub Pages
al-folio deploys via the included GitHub Actions workflow (`.github/workflows/deploy.yml`).

```bash
cd /Users/yansikuan/Desktop/personal-website
git init && git add . && git commit -m "Personal website (al-folio)"
gh repo create yansikuan.github.io --public --source=. --push
```
Then in the repo: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
After the first Action run finishes, the site is live at **https://yansikuan.github.io**.

> Note: since the repo is `yansikuan.github.io` (root domain), `baseurl` in `_config.yml`
> is correctly left blank.
