# Resume Hosting Setup

Your shareable link will be: **https://tjay27.github.io/resume**

---

## One-time setup (5 minutes)

### 1. Create the GitHub repo
- Go to https://github.com/new
- Name it exactly: `resume`
- Set it to **Public**
- Do NOT initialise with a README
- Click **Create repository**

### 2. Push this folder to the repo
Open Terminal in this `resume-site` folder and run:

```bash
git init
git add .
git commit -m "initial resume setup"
git branch -M main
git remote add origin https://github.com/tjay27/resume.git
git push -u origin main
```

### 3. Enable GitHub Pages
- Go to your repo → **Settings** → **Pages**
- Under **Source**, select **Deploy from a branch**
- Branch: `main` / Folder: `/docs`
- Click **Save**

After ~1 minute your resume is live at:
**https://tjay27.github.io/resume**

---

## How to update the resume

1. Edit `resume.tex` (ask Claude to make changes, or edit directly)
2. Push the updated file:
```bash
git add resume.tex
git commit -m "update resume"
git push
```

GitHub Actions automatically compiles the `.tex` to `docs/resume.pdf` and the link updates within ~2 minutes. No manual PDF export needed.

---

## For different recruiters

Since the link is always the same, you can:
- Keep a **general version** on the link (what's live now)
- Ask Claude to tweak bullets for a specific company, download that PDF locally, and attach it to the application — without overwriting the hosted version
