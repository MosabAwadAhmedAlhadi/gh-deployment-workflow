# 📦 GitHub Pages Deployment Workflow

This is Project 3 in my hands-on [roadmap.sh DevOps Projects series](https://roadmap.sh/projects/github-actions-deployment-workflow), where I’m learning by building — one project at a time.

In this project, I set up a complete **GitHub Actions workflow** that automatically deploys an `index.html` file to **GitHub Pages** whenever changes are pushed to the `main` branch.

---

## 🚀 Project Goals

- ✅ Learn GitHub Actions basics.
- ✅ Trigger workflows on specific file changes.
- ✅ Automate deployment to GitHub Pages.
- ✅ Understand OIDC and GitHub's permissions model.

---

## 🧠 What I Learned

### 🛎️ Step-by-step highlights:
- **Workflow Triggers:** Set up the workflow to only run when `index.html` is updated in the `main` branch.
- **Using Actions:** Used built-in GitHub Actions like:
  - `actions/checkout` – to fetch code
  - `actions/configure-pages` – to configure deployment
  - `actions/upload-pages-artifact` – to prepare the content
  - `actions/deploy-pages` – to publish to GitHub Pages
- **GITHUB_TOKEN Permissions:** Understood and configured the required permissions:
  - `contents: read` – to read repo files
  - `pages: write` – to publish to GitHub Pages
  - `id-token: write` – for OIDC-based authentication

---

## 📂 File Structure

```bash
.
├── .github
│   └── workflows
│       └── deploy.yml     # GitHub Actions workflow file
└── index.html             # The HTML page to be deployed
```

## 🔄 Deployment Process

Whenever I push a change to index.html in the main branch:

    - The GitHub Action is triggered.

    - The page is deployed automatically to GitHub Pages.

    - No manual steps needed!

## 🌐 Live Demo

🔗 Visit the deployed page here:
https://mosabawadahmedalhadi.github.io/gh-deployment-workflow/