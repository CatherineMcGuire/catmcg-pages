# Setting Up a Blog with GitHub Pages

Using [MkDocs](https://www.mkdocs.org/) and [Material for MkDocs theme](https://squidfunk.github.io/mkdocs-material/).

## Features

- Markdown-based posts
- Syntax highlighting for code
- A clean interface
- Free hosting on GitHub Pages


## Requirements

- A GitHub account
- Python installed (3.7 or higher)
- Basic terminal/command line usage

## Instructions

### 1. Create a folder for your blog

```bash
mkdir my-tech-blog
cd my-tech-blog
```

### 2. Create a Python virtual environment

```bash
python -m venv .venv
```

Activate it:

- On Mac/Linux:
  ```bash
  source .venv/bin/activate
  ```
- On Windows:
  ```bash
  .venv\Scripts\activate
  ```

### 3. Install MkDocs and the Material theme

```bash
pip install mkdocs-material
```

### 4. Create your site

```bash
mkdocs new .
```

### 5. Change the theme

Edit the `mkdocs.yml` file:

```yaml
site_name: My Tech Blog
theme:
  name: material

nav:
  - Home: index.md
```

### 6. Add your first post

Create a file at `docs/2025-05-19-first-post.md` with the contents of this tutorial!

### 7. Add each post to the navigation menu

nav:
  - Home: index.md
  - Blog:
      - "Getting Started": 2025-05-19-first-post.md
      - "Another Post": 2025-06-01-another-post.md
      - "My Latest Post": 2025-07-14-my-latest-post.md


### 8. Preview your site locally

```bash
mkdocs serve
```

Visit http://127.0.0.1:8000 in your browser.

### 9. Push to GitHub and deploy

1. Create a GitHub repo.
2. Push your code:
```bash
git init
git add .
git commit -m "initial blog"
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git push -u origin main
```

3. Deploy:

```bash
mkdocs gh-deploy
```

This command builds your site and automatically creates or updates a branch named gh-pages that holds the compiled HTML, CSS, and assets. GitHub Pages then serves your site directly from that branch (so you never have to merge your source files into it yourself).

Your site should now be live at `https://your-username.github.io/your-repo-name/`

---
