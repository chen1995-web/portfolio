# Chen Zhifeng — Portfolio Site

A static, zero-dependency portfolio site. Deploys to **GitHub Pages for free**.

## What's in here

- `index.html` — landing page (positioning + 4 project cards + contact)
- `projects/*.html` — showcase pages for each project, with real numbers and screenshots
- `assets/` — screenshots + the agentree agent-tree diagram
- `.github/workflows/deploy.yml` — auto-deploys to GitHub Pages on every push to `main`

The **saas-billing** and **webvitals** pages include fully client-side interactive demos —
they work on GitHub Pages with no backend. The agentree & rag-doc-chat showcases are static
(the live apps need a local FastAPI backend; see the project READMEs).

## Deploy (5 minutes, free)

1. Create a new empty GitHub repo, e.g. `portfolio`.
2. Push this folder to it:

   ```bash
   cd portfolio-site
   git init
   git add -A
   git commit -m "portfolio site"
   git branch -M main
   git remote add origin https://github.com/<YOUR-USERNAME>/portfolio.git
   git push -u origin main
   ```

3. On GitHub: **Settings → Pages → Build and deployment → Source = GitHub Actions**.
   (The workflow already has the right permissions; you just enable Pages.)
4. Wait ~30s. Your site is live at:

   ```
   https://<YOUR-USERNAME>.github.io/portfolio/
   ```

5. Share that link. Update `index.html` / `projects/*.html` and push again — it redeploys automatically.

## Before you share — edit these

- **Email** — `chenzf1995@gmail.com` in `index.html`.
- **GitHub link** — `index.html` and each `projects/*.html` link to `https://github.com/`; point them at
  your actual repos (or remove until they exist).
- **Name** — `Chen Zhifeng` is used as a default; change to whatever you go by.

## Custom domain (optional)

GitHub → Settings → Pages → Custom domain. Add a CNAME record pointing at
`<YOUR-USERNAME>.github.io`. Free.

## Preview locally

```bash
cd portfolio-site
python3 -m http.server 8000
# open http://127.0.0.1:8000
```
