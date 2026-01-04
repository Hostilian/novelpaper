# NovelPaper - Quick Setup Guide

Welcome to NovelPaper! This guide will help you get started quickly.

## 🚀 Quick Start (2 minutes)

### View Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Hostilian/novelpaper.git
   cd novelpaper
   ```

2. **Open in browser:**
   - Simply double-click `index.html` or
   - Run a local server:
     ```bash
     python -m http.server 8000
     ```
   - Visit http://localhost:8000

That's it! No build process, no dependencies to install.

## 📝 Make It Yours

### Customize Content

1. **Edit text:** Open `index.html` and update the content
2. **Change colors:** Edit CSS variables in `styles.css` (line 12-20)
3. **Modify layout:** Adjust grid/flexbox properties in `styles.css`

### Example: Change Color Scheme

```css
/* In styles.css, find these lines: */
:root {
    --color-primary: #8B7355;     /* Change this */
    --color-secondary: #C9B896;    /* And this */
    --color-accent: #A67C52;       /* And this */
}
```

## 🌐 Deploy to GitHub Pages

1. Fork this repository
2. Go to **Settings** → **Pages**
3. Select source: **Deploy from a branch**
4. Choose **main** branch, **/ (root)** folder
5. Click **Save**
6. Your site will be live at: `https://yourusername.github.io/novelpaper/`

## 🤝 Contributing

Want to improve NovelPaper? See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## 📚 More Resources

- [Full README](README.md) - Complete documentation
- [CHANGELOG](CHANGELOG.md) - Version history
- [Security Policy](SECURITY.md) - Reporting vulnerabilities

## ❓ Need Help?

- [Open an issue](https://github.com/Hostilian/novelpaper/issues)
- [Start a discussion](https://github.com/Hostilian/novelpaper/discussions)

---

*Happy folding!* ✨
