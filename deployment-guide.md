# 🚀 Deployment Guide for prashunkc.com.np

## Quick Start Options

### Option 1: Netlify (Recommended - Free & Easy)

1. **Visit**: https://netlify.com
2. **Sign up** with GitHub, GitLab, or email
3. **Drag & drop** your `prashunkc-portfolio.html` file
4. **Rename** to `index.html` after upload
5. **Connect domain**:
   - Go to Domain settings
   - Add custom domain: `prashunkc.com.np`
   - Update your domain's DNS records

### Option 2: Traditional Hosting

1. **Purchase hosting** from a provider
2. **Access cPanel/File Manager**
3. **Upload files** to `public_html` or `www` folder
4. **Rename** `prashunkc-portfolio.html` to `index.html`

### Option 3: GitHub Pages

1. **Create GitHub repository** named `prashunkc.github.io`
2. **Upload** your HTML file as `index.html`
3. **Enable Pages** in repository settings
4. **Configure custom domain** in settings

## DNS Configuration

When connecting your domain, you'll need to update DNS records:

**For Netlify:**
```
Type: CNAME
Name: www
Value: your-site-name.netlify.app

Type: A
Name: @
Value: 75.2.60.5
```

**For other hosts:**
Check with your hosting provider for specific DNS settings.

## Before Deployment Checklist

- [ ] Test website locally in browser
- [ ] Check all links work
- [ ] Verify responsive design on mobile
- [ ] Optimize images (if any added later)
- [ ] Test contact form
- [ ] Update meta tags for SEO

## File Structure for Hosting

```
your-website/
├── index.html (your main file)
├── assets/ (optional - for future)
│   ├── images/
│   ├── css/
│   └── js/
└── robots.txt (optional - for SEO)
```

## Next Steps After Deployment

1. **SSL Certificate** - Most modern hosts provide free SSL
2. **Google Analytics** - Track visitors
3. **Search Console** - Submit to Google
4. **Performance optimization** - Use tools like GTmetrix
5. **Regular backups** - Keep your code safe

## Troubleshooting

**Common Issues:**
- **404 Error**: Check file is named `index.html`
- **Styling not loading**: Check file paths
- **Domain not working**: DNS changes take 24-48 hours
- **Mobile layout issues**: Test responsive design

## Cost Estimates

**Free Options:**
- Netlify: Free tier available
- GitHub Pages: Free
- Vercel: Free tier available

**Paid Hosting:**
- Shared hosting: $3-10/month
- VPS: $10-50/month
- Premium hosts: $5-20/month

Choose based on your needs and budget!