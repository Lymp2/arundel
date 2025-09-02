# Netlify Deployment Guide

This guide will help you deploy your Liberal Democrats Local Division website to Netlify.

## 🚀 Quick Deploy

### Option 1: Drag & Drop (Easiest)

1. **Build your site locally:**
   ```bash
   hugo --minify
   ```

2. **Deploy to Netlify:**
   - Go to [netlify.com](https://netlify.com)
   - Sign up/Login
   - Drag the `public/` folder to the deploy area
   - Your site will be live in seconds!

### Option 2: Git Integration (Recommended)

1. **Push to GitHub:**
   ```bash
   git add .
   git commit -m "Initial website setup"
   git push origin main
   ```

2. **Connect to Netlify:**
   - Go to [netlify.com](https://netlify.com)
   - Click "New site from Git"
   - Choose your repository
   - Set build settings:
     - **Build command:** `hugo --minify`
     - **Publish directory:** `public`
   - Click "Deploy site"

## ⚙️ Configuration

### Build Settings

The `netlify.toml` file is already configured with:
- Hugo version: 0.146.7
- Build command: `hugo`
- Publish directory: `public`

### Environment Variables

You can set these in Netlify's dashboard:
- `HUGO_ENV=production`
- `HUGO_BASEURL` (will be set automatically)

## 🔧 Customization Before Deployment

### 1. Update Site Information

Edit `hugo.toml`:
```toml
baseURL = 'https://your-actual-site-name.netlify.app/'
title = 'Liberal Democrats - [Your Local Division Name]'
```

### 2. Update Contact Information

Edit these files with your actual details:
- `content/councils/sarah-johnson.md`
- `content/donate/_index.md`
- `content/join/_index.md`
- `content/get-involved/_index.md`

### 3. Update Social Media Links

Edit these files:
- `themes/lybdems-theme/layouts/index.html`
- `themes/lybdems-theme/layouts/partials/footer.html`

### 4. Add Your Logo

Replace the placeholder favicon:
- Add your logo to `static/favicon.ico`
- Add any other images to `static/images/`

## 📱 Domain & SSL

### Custom Domain

1. **In Netlify dashboard:**
   - Go to Site settings > Domain management
   - Click "Add custom domain"
   - Enter your domain (e.g., `libdems.yourtown.org.uk`)

2. **DNS Configuration:**
   - Add CNAME record pointing to your Netlify site
   - Netlify will automatically provision SSL certificate

### SSL Certificate

- Netlify provides free SSL certificates automatically
- HTTPS will be enabled by default
- No additional configuration needed

## 🔄 Continuous Deployment

### Automatic Updates

Once connected to Git:
- Every push to main branch triggers automatic rebuild
- Your site updates automatically
- No manual deployment needed

### Preview Deployments

- Pull requests get preview URLs
- Test changes before merging
- Perfect for content reviews

## 📊 Analytics & Monitoring

### Built-in Features

- **Page views:** Available in Netlify dashboard
- **Build status:** Monitor deployment success
- **Performance:** Core Web Vitals tracking

### Google Analytics

Add to `themes/lybdems-theme/layouts/_default/baseof.html`:
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

## 🚨 Troubleshooting

### Common Issues

1. **Build fails:**
   - Check Hugo version compatibility
   - Verify all files are committed
   - Check build logs in Netlify dashboard

2. **Styling issues:**
   - Ensure CSS files are in `static/css/`
   - Check file paths in templates
   - Verify CSS syntax

3. **Content not showing:**
   - Check front matter in markdown files
   - Verify file structure in `content/` folder
   - Check Hugo build logs

### Support

- **Netlify docs:** [docs.netlify.com](https://docs.netlify.com)
- **Hugo docs:** [gohugo.io](https://gohugo.io)
- **Build logs:** Available in Netlify dashboard

## 🎯 Post-Deployment Checklist

- [ ] Site loads correctly
- [ ] All pages accessible
- [ ] Navigation works
- [ ] Mobile responsive
- [ ] Contact forms working
- [ ] Social media links correct
- [ ] Custom domain configured
- [ ] SSL certificate active
- [ ] Analytics tracking
- [ ] Performance optimized

## 🔒 Security & Compliance

### Data Protection

- Update privacy policy with actual details
- Ensure GDPR compliance for forms
- Review cookie policy

### Electoral Law

- Verify donation compliance
- Check campaign finance rules
- Ensure proper disclaimers

## 📈 Performance Optimization

### Built-in Features

- **CDN:** Global content delivery
- **Compression:** Automatic gzip
- **Caching:** Smart browser caching
- **Minification:** Hugo handles this

### Additional Optimizations

- Optimize images before upload
- Use WebP format where possible
- Minimize external dependencies

---

**Your Liberal Democrats website is now ready for Netlify deployment! 🎉**

For questions or support, check the Netlify documentation or contact your local party's web team.
