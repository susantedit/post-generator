# 🚀 Deployment Guide

## GitHub Pages Deployment (Recommended)

Your invoice generator is now ready to deploy on GitHub Pages!

### Step 1: Enable GitHub Pages

1. Go to your repository: https://github.com/susantedit/invoicegenerator
2. Click on **Settings** (top right)
3. Scroll down to **Pages** section (left sidebar)
4. Under **Source**, select:
   - Branch: `main`
   - Folder: `/ (root)`
5. Click **Save**

### Step 2: Wait for Deployment

- GitHub will automatically build and deploy your site
- This usually takes 1-3 minutes
- You'll see a green checkmark when ready

### Step 3: Access Your Site

Your invoice generator will be live at:
```
https://susantedit.github.io/invoicegenerator/
```

## Alternative Deployment Options

### 1. Netlify (Free)

**Quick Deploy:**
1. Go to https://app.netlify.com/drop
2. Drag and drop your project folder
3. Get instant URL like: `your-site.netlify.app`

**GitHub Integration:**
1. Sign up at https://netlify.com
2. Click "New site from Git"
3. Connect your GitHub repository
4. Deploy settings:
   - Build command: (leave empty)
   - Publish directory: `/`
5. Click "Deploy site"

**Custom Domain (Optional):**
- Go to Site settings → Domain management
- Add your custom domain
- Update DNS records as instructed

### 2. Vercel (Free)

1. Go to https://vercel.com
2. Click "Import Project"
3. Connect GitHub repository
4. Deploy settings:
   - Framework Preset: Other
   - Build Command: (leave empty)
   - Output Directory: `./`
5. Click "Deploy"

Your site will be live at: `your-project.vercel.app`

### 3. Cloudflare Pages (Free)

1. Go to https://pages.cloudflare.com
2. Click "Create a project"
3. Connect GitHub repository
4. Build settings:
   - Build command: (leave empty)
   - Build output directory: `/`
5. Click "Save and Deploy"

### 4. Firebase Hosting (Free)

```bash
# Install Firebase CLI
npm install -g firebase-tools

# Login to Firebase
firebase login

# Initialize Firebase
firebase init hosting

# Select options:
# - Use existing project or create new
# - Public directory: .
# - Single-page app: No
# - GitHub auto-deploy: Yes (optional)

# Deploy
firebase deploy
```

### 5. Surge.sh (Free)

```bash
# Install Surge
npm install -g surge

# Deploy (from project directory)
surge

# Follow prompts:
# - Email: your@email.com
# - Password: (create one)
# - Domain: invoicegenerator.surge.sh (or custom)
```

## Custom Domain Setup

### For GitHub Pages:

1. Buy domain from Namecheap, GoDaddy, etc.
2. Add `CNAME` file to repository:
   ```
   yourdomain.com
   ```
3. In domain registrar, add DNS records:
   ```
   Type: A
   Host: @
   Value: 185.199.108.153
   
   Type: A
   Host: @
   Value: 185.199.109.153
   
   Type: A
   Host: @
   Value: 185.199.110.153
   
   Type: A
   Host: @
   Value: 185.199.111.153
   
   Type: CNAME
   Host: www
   Value: susantedit.github.io
   ```
4. In GitHub Settings → Pages, add custom domain
5. Enable "Enforce HTTPS"

## Performance Optimization

### Enable Caching
Add `.htaccess` (for Apache servers):
```apache
<IfModule mod_expires.c>
  ExpiresActive On
  ExpiresByType image/png "access plus 1 year"
  ExpiresByType text/css "access plus 1 month"
  ExpiresByType application/javascript "access plus 1 month"
</IfModule>
```

### Compress Images
- Use TinyPNG or ImageOptim for logo.png
- Convert service provider images to WebP format

### CDN Integration
- GitHub Pages automatically uses CDN
- For other hosts, consider Cloudflare (free)

## Monitoring & Analytics

### Google Analytics (Optional)
Add before `</head>` in invoice.html:
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

### Uptime Monitoring
- UptimeRobot (free): https://uptimerobot.com
- Pingdom (free tier): https://pingdom.com

## Troubleshooting

### Images Not Loading
- Ensure all image paths are relative
- Check image files are committed to repository
- Verify CORS settings for external images

### GitHub Pages Not Working
- Check repository is public
- Verify Pages is enabled in Settings
- Wait 5-10 minutes after enabling
- Check Actions tab for build errors

### Custom Domain Issues
- DNS propagation takes 24-48 hours
- Use https://dnschecker.org to verify
- Clear browser cache
- Try incognito mode

## Security

### HTTPS
- GitHub Pages: Automatic
- Other hosts: Enable SSL certificate (usually free with Let's Encrypt)

### Content Security Policy
Add to `<head>` for extra security:
```html
<meta http-equiv="Content-Security-Policy" 
      content="default-src 'self' 'unsafe-inline' https:; img-src 'self' data: https:;">
```

## Updates

To update your deployed site:
```bash
# Make changes to files
git add .
git commit -m "Update description"
git push origin main

# GitHub Pages auto-deploys
# Other platforms may need manual trigger
```

## Support

- GitHub Pages Docs: https://docs.github.com/pages
- Netlify Docs: https://docs.netlify.com
- Vercel Docs: https://vercel.com/docs

---

🎉 Your invoice generator is now live and accessible worldwide!
