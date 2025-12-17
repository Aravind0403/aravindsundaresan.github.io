# How to Update Your Portfolio

This portfolio is built with [Hugo](https://gohugo.io/) and the [Hugo Book Theme](https://github.com/alex-shpak/hugo-book). It is designed to be easily updated by editing simple text files.

## 1. Prerequisites

You do not need to install Hugo globally if you use the provided `npx` commands, but you will need `Node.js` installed.
Alternatively, you can install [Hugo Extended](https://gohugo.io/installation/) on your machine.

## 2. Editing Content

All content is located in the `content/` directory. Files are written in **Markdown**.

### Edit Home / Bio
Edit `content/_index.md`.
- **Title**: Change the `title` in the front matter (top of file).
- **Bio**: Update the text below the header.

### Edit Experience
Edit `content/experience.md`.
- Add new roles using standard Markdown headers (`##`, `###`).
- Follow the existing format for consistency.

### Edit Projects
Edit `content/projects.md`.
- Add new projects as new sections.

### Edit Sidebar/Menu
The sidebar is automatically generated from the files in `content/`.
- To change the order, edit the `weight` parameter in the front matter of each file. Lower numbers appear first.

## 3. Previewing Changes via GitHub/Netlify

If you deploy this repo to **Netlify** or **GitHub Pages**:
1.  Commit your changes to the `main` branch.
2.  Push to GitHub.
3.  The site will automatically rebuild (if you have CI/CD set up).

## 4. Previewing Locally

To preview the site on your computer:

```bash
# Verify you are in the portfolio directory
cd portfolio

# Run the server (using npx to avoid global install issues)
npx hugo-extended server
```

Open your browser to `http://localhost:1313`.

## 5. Deployment Info

**Netlify:**
- **Build command:** `hugo --gc --minify` (Ensure you select a Hugo version with "Extended" support in Netlify settings, or it defaults to standard).
- **Publish directory:** `public`

**GitHub Pages:**
- Use the standard Hugo GitHub Actions workflow.
