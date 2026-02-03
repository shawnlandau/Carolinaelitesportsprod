# Quick Deployment Guide

## 🚀 Deploy to Netlify in 5 Minutes

### Step 1: Prepare Your Files
1. Download/clone this entire project folder
2. Replace placeholder images in `/images/` folder with your actual photos
3. Make sure all files are ready

### Step 2: Create GitHub Repository
```bash
git init
git add .
git commit -m "Initial commit - Carolina Elite Sports"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
git push -u origin main
```

### Step 3: Deploy to Netlify
1. Go to https://app.netlify.com/
2. Click "Add new site" → "Import an existing project"
3. Choose "GitHub"
4. Select your repository
5. Click "Deploy site" (no build settings needed)
6. Done! Your site is live

### Step 4: Add Custom Domain
1. In Netlify dashboard → "Domain settings"
2. Click "Add custom domain"
3. Enter: `carolinaelitesports.com`
4. Update DNS records at your domain registrar:
   - Add Netlify's nameservers OR
   - Add A record pointing to Netlify's load balancer
5. Wait for DNS propagation (up to 48 hours)

### Step 5: Test Contact Form
1. Visit your deployed site
2. Fill out contact form
3. Check Netlify dashboard → "Forms" to see submission
4. Set up email notifications in Netlify

---

## ✅ Deployment Checklist

Before deploying:
- [ ] All HTML files present
- [ ] CSS and JS files in place
- [ ] Images replaced (or keep placeholders temporarily)
- [ ] Contact information updated
- [ ] Social media links verified
- [ ] External booking links working

After deploying:
- [ ] Test all pages load correctly
- [ ] Test mobile responsiveness
- [ ] Submit contact form test
- [ ] Verify all links work
- [ ] Check on multiple browsers
- [ ] Set up form notifications
- [ ] Add Google Analytics (optional)

---

## 🆘 Troubleshooting

**Forms not working?**
- Make sure `netlify.toml` is in root directory
- Check form has `data-netlify="true"` attribute
- Verify form name matches Netlify dashboard

**Images not loading?**
- Check image file paths are correct
- Ensure images are in `/images/` folder
- Verify image filenames match HTML references

**CSS not applied?**
- Check `css/style.css` exists
- Verify `<link>` tag in HTML is correct
- Clear browser cache and refresh

**Mobile menu not working?**
- Check `js/main.js` is loaded
- Open browser console for errors
- Ensure JavaScript is enabled

---

## 📞 Need Help?

Refer to the main README.md file for detailed documentation.

For Netlify-specific issues:
- Visit: https://docs.netlify.com/
- Support: https://answers.netlify.com/

---

**You're all set! Deploy with confidence! 🎉**
