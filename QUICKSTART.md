# Quick Start Guide - Carolina Elite Sports Website

## 🚀 What You Have

A complete, professional static website ready for deployment to Netlify!

### ✅ Completed Features

- **7 Complete Pages:**
  - Home (with hero, contact form, login buttons)
  - About (mission and facilities)
  - Staff (coaching team profiles)
  - Camps/Tryouts (programs and registration)
  - Academy (year-round training programs)
  - Alumni (success stories and statistics)
  - Sponsors (current sponsors and opportunities)

- **Mobile Responsive:** Works perfectly on all devices
- **Contact Form:** Integrated with Netlify Forms (collects submissions)
- **External Logins:** Swift and eSoft login buttons configured
- **Professional Design:** Blue/navy color scheme, smooth animations
- **SEO Ready:** Sitemap, robots.txt, semantic HTML
- **Performance Optimized:** Fast loading, lazy loading images

## 📁 What to Add Before Launch

### 1. Images (Priority)
Add these to the `/images` folder:
- `carolina-rays-logo.png` - Your logo (header)
- Staff photos (optional, has placeholders)
- Alumni photos (optional, has placeholders)
- Sponsor logos (optional, has placeholders)

### 2. Social Media Links
Update in all HTML files (search for these):
- Facebook: `href="#"` → `href="https://facebook.com/yourpage"`
- Twitter: `href="#"` → `href="https://twitter.com/yourhandle"`
- Instagram: `href="#"` → `href="https://instagram.com/yourhandle"`

## 🌐 Deploy to Netlify (3 Easy Options)

### Option 1: GitHub + Netlify (Recommended)
1. Create GitHub repo
2. Push code: `git remote add origin [your-repo-url]` then `git push -u origin main`
3. Connect to Netlify
4. Auto-deploys on every push!

### Option 2: Drag & Drop
1. Go to https://app.netlify.com/drop
2. Drag your project folder
3. Instant deployment!

### Option 3: Netlify CLI
```bash
npm install -g netlify-cli
netlify login
netlify deploy --prod
```

## 📋 Post-Deployment Checklist

After deploying:
- [ ] Test contact form (submit and check email)
- [ ] Add form email notifications in Netlify dashboard
- [ ] Update sitemap.xml with actual URL
- [ ] Update robots.txt with actual URL
- [ ] Test all external login links
- [ ] Test on mobile devices
- [ ] Add custom domain (optional)

## 📞 Contact Information Currently Set

- **Phone:** 843-286-8147
- **Address:** 4007 Belle Terre Blvd Unit H, Myrtle Beach, SC 29579
- **Indoor Facility:** 4770 Northgate Blvd, Myrtle Beach, SC 29577
- **Ripken Facility:** 3051 Ripken Way, Myrtle Beach, SC 29577
- **Hours:** Mon-Fri 3PM-9PM, Sat/Sun by Appointment

## 🛠️ Making Updates After Launch

1. Edit HTML/CSS/JS files
2. Commit: `git commit -am "Description of changes"`
3. Push: `git push`
4. Netlify auto-deploys in ~2 minutes!

## 📖 Documentation Files

- **README.md** - Full project documentation
- **DEPLOYMENT.md** - Step-by-step deployment guide
- **images/README.md** - Image requirements and tips

## 🎨 Customization Quick Tips

### Change Colors
Edit `css/styles.css` variables:
```css
:root {
    --primary-blue: #003d7a;    /* Main blue */
    --secondary-blue: #0066cc;   /* Lighter blue */
    --accent-gold: #ffd700;      /* Gold accent */
}
```

### Update Hours
Search all HTML files for "Hours" section

### Modify Content
Each HTML page is self-contained - edit directly!

## ⚡ Quick Commands

```bash
# View locally
python -m http.server 8000
# Then visit: http://localhost:8000

# Deploy to Netlify
netlify deploy --prod

# Push to GitHub
git add .
git commit -m "Your changes"
git push
```

## 🆘 Need Help?

Check these files:
1. `DEPLOYMENT.md` - Detailed deployment steps
2. `README.md` - Complete documentation
3. Netlify Docs: https://docs.netlify.com

---

**Your site is production-ready! Just add your images and deploy! 🎉**
