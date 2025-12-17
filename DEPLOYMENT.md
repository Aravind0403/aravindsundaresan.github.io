# Deployment Guide

Since this is a static site built with Hugo, you have several excellent free hosting options. The two best choices are **Netlify** (easiest) and **GitHub Pages** (standard).

## Option 1: Netlify (Recommended)

Netlify is generally easier because it auto-detects Hugo settings and handles build versions automatically.

### Steps:
1.  **Push to GitHub:** Ensure your project is pushed to a GitHub repository.
2.  **Log in to Netlify:** Go to [netlify.com](https://www.netlify.com/) and log in with your GitHub account.
3.  **New Site:** Click **"Add new site"** > **"Import from an existing project"**.
4.  **Connect GitHub:** Select GitHub and choose your portfolio repository.
5.  **Configure Build:** Netlify should auto-detect these, but verify:
    *   **Build Command:** `hugo --gc --minify`
    *   **Publish Directory:** `public`
6.  **Environment Variable (Crucial):**
    *   Click "Show advanced" or go to "Environment variables".
    *   Key: `HUGO_VERSION`
    *   Value: `0.110.0` (or newer - check your local version with `hugo version`). This ensures it uses the "Extended" version needed for SCSS.
7.  **Deploy:** Click "Deploy Site".
8.  **Domain:** You can change the default `random-name.netlify.app` to `aravind.netlify.app` or connect your own custom domain in "Domain Settings".

---

## Option 2: GitHub Pages

Ideal if you want your site at `aravind0403.github.io`.

### Steps:

1.  **Create Repository:** Name your repository `username.github.io` (replace `username` with your GitHub username).
2.  **Push Code:** Push this entire project to the `main` branch.
3.  **GitHub Actions:**
    *   Go to your repository on GitHub.
    *   Click **Settings** > **Pages**.
    *   Under **Build and deployment**, switch "Source" to **GitHub Actions**.
    *   GitHub will likely suggest a "Hugo" workflow. Click "Configure".
    *   Commit the suggested `hugo.yml` file.
4.  **Wait:** The Action will run and deploy your site in a few minutes.

## Option 3: Vercel

Similar to Netlify.
1.  Import project from GitHub.
2.  Framework Preset: Select **Hugo**.
3.  Build Command: `hugo --gc --minify`
4.  Output Directory: `public`
5.  Deploy.
