# Deployment Guide

This guide covers various ways to deploy the NovelPaper website.

## 📋 Prerequisites

- A GitHub account (for GitHub Pages)
- Basic familiarity with git and command line
- No build tools or dependencies required!

## 🚀 Deployment Options

### Option 1: GitHub Pages (Recommended)

**Easiest and free hosting for static sites.**

#### Steps:

1. **Fork or Clone this repository to your GitHub account**

2. **Enable GitHub Pages:**
   - Go to your repository on GitHub
   - Click **Settings** → **Pages**
   - Under "Source", select:
     - Branch: `main`
     - Folder: `/ (root)`
   - Click **Save**

3. **Wait for deployment:**
   - GitHub Actions will automatically deploy your site
   - Check the Actions tab to see deployment progress
   - Your site will be available at: `https://yourusername.github.io/novelpaper/`

4. **Custom domain (optional):**
   - Add a `CNAME` file with your domain
   - Configure DNS settings with your domain provider
   - Update repository settings with custom domain

#### GitHub Pages Configuration

The repository includes a GitHub Actions workflow (`.github/workflows/deploy.yml`) that automatically deploys to GitHub Pages on every push to `main`.

### Option 2: Netlify

**Free tier with continuous deployment and custom domains.**

#### Steps:

1. **Sign up at [netlify.com](https://netlify.com)**

2. **Deploy from GitHub:**
   - Click "New site from Git"
   - Choose GitHub and authorize Netlify
   - Select your repository
   - Build settings:
     - Build command: (leave empty)
     - Publish directory: `/`
   - Click "Deploy site"

3. **Your site is live!**
   - Netlify provides a random URL
   - Configure custom domain if desired

#### Netlify Configuration File

Create `netlify.toml` in your repository root:

```toml
[build]
  publish = "."
  
[[headers]]
  for = "/*"
  [headers.values]
    X-Frame-Options = "DENY"
    X-Content-Type-Options = "nosniff"
    X-XSS-Protection = "1; mode=block"
    Referrer-Policy = "strict-origin-when-cross-origin"
```

### Option 3: Vercel

**Fast deployment with excellent performance.**

#### Steps:

1. **Sign up at [vercel.com](https://vercel.com)**

2. **Import project:**
   - Click "New Project"
   - Import from GitHub
   - Select your repository
   - Click "Deploy"

3. **Done!**
   - Automatic deployments on every push
   - Free SSL certificate
   - Custom domain support

### Option 4: Traditional Web Hosting

**Upload files via FTP/SFTP to any web host.**

#### Steps:

1. **Download/clone the repository**

2. **Upload files to your web host:**
   - Use FTP client (FileZilla, Cyberduck, etc.)
   - Upload all files to your `public_html` or `www` directory
   - Make sure index.html is in the root

3. **Access your site:**
   - Visit your domain
   - NovelPaper should load immediately

### Option 5: Cloud Storage (S3, Google Cloud Storage)

**Use cloud storage for static site hosting.**

#### AWS S3 + CloudFront:

1. **Create S3 bucket:**
   ```bash
   aws s3 mb s3://novelpaper-bucket
   ```

2. **Upload files:**
   ```bash
   aws s3 sync . s3://novelpaper-bucket --exclude ".git/*"
   ```

3. **Enable static website hosting:**
   - Set index document: `index.html`
   - Set error document: `index.html` (for SPA behavior)

4. **Configure CloudFront (optional):**
   - Create distribution
   - Point to S3 bucket
   - Enable HTTPS

## 🔧 Configuration

### Environment Variables

No environment variables required! This is a static site.

### Custom Domain

#### For GitHub Pages:

1. Add `CNAME` file with your domain:
   ```
   www.yourdomain.com
   ```

2. Configure DNS:
   ```
   CNAME www YOURUSERNAME.github.io
   A @ 185.199.108.153
   A @ 185.199.109.153
   A @ 185.199.110.153
   A @ 185.199.111.153
   ```

#### For Netlify/Vercel:

1. Add domain in dashboard
2. Follow DNS configuration instructions
3. SSL is automatically configured

## 🔒 Security Headers

Add these headers for better security (configure in your hosting platform):

```
X-Frame-Options: DENY
X-Content-Type-Options: nosniff
X-XSS-Protection: 1; mode=block
Referrer-Policy: strict-origin-when-cross-origin
Content-Security-Policy: default-src 'self'; style-src 'self' 'unsafe-inline'; script-src 'self' 'unsafe-inline'
```

## 📊 Analytics (Optional)

### Google Analytics:

Add before `</head>` in index.html:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Plausible (Privacy-friendly):

```html
<script defer data-domain="yourdomain.com" src="https://plausible.io/js/script.js"></script>
```

## ✅ Post-Deployment Checklist

- [ ] Site loads correctly
- [ ] All links work
- [ ] Images/assets load (if you add any)
- [ ] Mobile responsive
- [ ] Forms work (or show appropriate message)
- [ ] HTTPS enabled
- [ ] Custom domain configured (if applicable)
- [ ] Analytics configured (if desired)
- [ ] SEO meta tags are correct
- [ ] robots.txt accessible
- [ ] sitemap.xml accessible
- [ ] Favicon displays correctly

## 🐛 Troubleshooting

### Site not loading:

- Check deployment logs in your hosting platform
- Verify all files were uploaded
- Clear browser cache

### Styles not applying:

- Check file paths in index.html
- Verify CSS file was uploaded
- Check browser console for errors

### GitHub Pages not deploying:

- Check Actions tab for errors
- Verify Pages is enabled in repository settings
- Wait a few minutes for DNS propagation

## 📞 Support

Need help with deployment?

- [Open an issue](https://github.com/Hostilian/novelpaper/issues)
- [Check discussions](https://github.com/Hostilian/novelpaper/discussions)
- Review hosting platform documentation

---

*Happy deploying!* 🚀
