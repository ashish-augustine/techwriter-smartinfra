# Deployment Guide

## Overview

This documentation site is built with MkDocs and can be deployed to various hosting platforms. The static site files are generated in the `site/` directory after building.

## Build Process

```bash
# Install dependencies (if not already done)
pip install -r requirements.txt

# Build the static site
mkdocs build

# Site files are generated in: site/
```

## Deployment Options

### Option 1: GitHub Pages (Recommended - Automated)

**Prerequisites:**

- Repository on GitHub
- Repository settings: Enable "GitHub Pages" under Settings → Pages
- Set source to "GitHub Actions"

**Setup:**

1. The `.github/workflows/deploy.yml` workflow automatically:
   - Builds the documentation on every push to `main`/`master`
   - Deploys to GitHub Pages

2. Configure your repository:
   - Go to Settings → Pages
   - Select "GitHub Actions" as the deployment source

**Deployment:** Just push to main/master - GitHub Actions handles the rest!

```bash
git add .
git commit -m "Update documentation"
git push origin main
```

### Option 2: Netlify (Free Tier Available)

1. **Connect Repository:**
   - Go to [Netlify](https://www.netlify.com/)
   - Click "New site from Git"
   - Select your GitHub repository

2. **Configure Build Settings:**
   - Build command: `mkdocs build`
   - Publish directory: `site`

3. **Deploy:**
   - Netlify automatically deploys on every push to main

### Option 3: Vercel

1. **Connect Repository:**
   - Go to [Vercel](https://vercel.com/)
   - Import your GitHub repository

2. **Configure:**
   - Framework: "Other"
   - Build Command: `mkdocs build`
   - Output Directory: `site`

3. **Deploy:**
   - Automatic deployment on push

### Option 4: Manual Deployment (Any Web Server)

#### AWS S3 + CloudFront

```bash
# Build the site
mkdocs build

# Sync to S3
aws s3 sync site/ s3://your-bucket-name --delete

# Invalidate CloudFront cache (if using CloudFront)
aws cloudfront create-invalidation --distribution-id YOUR_DIST_ID --paths "/*"
```

#### Traditional Server (Apache, Nginx, etc.)

```bash
# Build the site
mkdocs build

# Copy to server
scp -r site/* user@your-server:/var/www/html/docs

# Or use SFTP, FTP, or SSH
```

#### Docker Deployment

```bash
# Build Docker image with documentation
docker build -t my-docs .
docker run -p 8000:80 my-docs
```

### Option 5: Azure Static Web Apps

1. **Create Static Web App:**
   - Go to Azure Portal
   - Create "Static Web App"
   - Connect GitHub repository

2. **Configure Workflow:**
   - Azure automatically creates `.github/workflows/azure-static-web-apps-*.yml`
   - Edit build settings:
     ```yaml
     app_build_command: "mkdocs build"
     app_location: "site"
     ```

3. **Deploy:**
   - Automatic on push to configured branch

## Pre-Deployment Checklist

- [ ] All markdown files are well-formed
- [ ] All images and assets are properly linked
- [ ] Navigation in `mkdocs.yml` is complete
- [ ] Local build succeeds: `mkdocs build`
- [ ] Local preview works: `mkdocs serve`
- [ ] No broken links
- [ ] SEO metadata is set in `mkdocs.yml`

## Post-Deployment Verification

After deploying, verify:

1. **Site loads correctly** - Check main page loads
2. **Navigation works** - Click through several pages
3. **Search functionality** - Test the search feature
4. **Responsive design** - Test on mobile/tablet
5. **Diagrams render** - Check Mermaid diagrams display
6. **Custom CSS applied** - Verify styling looks correct

## Performance Optimization

### Compression

Most hosting platforms automatically compress assets. Verify with:

```bash
# Check file sizes
du -sh site/
```

### CDN Integration

- **GitHub Pages** - Uses GitHub's CDN automatically
- **Netlify** - Includes global CDN
- **Vercel** - Includes global CDN
- **AWS** - Add CloudFront for CDN

## Monitoring & Updates

### GitHub Pages

- Workflow status visible in repository Actions tab
- Automatic rollback if build fails

### Netlify/Vercel

- Build logs available in dashboard
- Preview deployments for PR reviews

### Custom Servers

- Monitor disk usage of `site/` directory
- Set up log rotation for web server logs

## Troubleshooting

### Build Fails

```bash
# Check locally first
mkdocs build

# Review error messages
mkdocs build --verbose
```

### Site Not Updating

- Clear browser cache
- Check deployment workflow status
- Verify branch is correct (main vs master)

### Broken Links After Deploy

- Check asset paths in markdown
- Ensure `site_url` is set correctly in `mkdocs.yml`

## Maintenance

### Regular Updates

```bash
# Update dependencies
pip install --upgrade -r requirements.txt

# Update MkDocs
pip install --upgrade mkdocs mkdocs-material mkdocs-mermaid2-plugin
```

### Backup

Always maintain a git backup of your repository.

## Additional Resources

- [MkDocs Deployment Guide](https://www.mkdocs.org/user-guide/deploying-your-docs/)
- [GitHub Pages Documentation](https://pages.github.com/)
- [Netlify Documentation](https://docs.netlify.com/)
- [Material for MkDocs Guide](https://squidfunk.github.io/mkdocs-material/)
