# Deployment Guide for Carolina Elite Sports Website

## Prerequisites

Before deploying, you'll need:
- A GitHub account (free)
- A Netlify account (free)
- Your website files (already prepared)
- Carolina Rays logo and images (to be added)

## Step-by-Step Deployment Instructions

### Step 1: Prepare Your Images

1. Create the following images and add them to the `/images` folder:
   - `carolina-rays-logo.png` - Your team logo (300x100px recommended)
   - Staff photos (400x400px, square format)
   - Alumni photos (600x450px, 4:3 aspect ratio)
   - Sponsor logos (300x200px or proportional)

2. Save images with descriptive names:
   - `images/carolina-rays-logo.png`
   - `images/staff-john-smith.jpg`
   - `images/alumni-player-name.jpg`
   - `images/sponsor-company-name.png`

### Step 2: Create GitHub Repository

1. **Go to GitHub:**
   - Visit https://github.com
   - Sign in or create an account

2. **Create New Repository:**
   - Click the "+" icon in top right
   - Select "New repository"
   - Name it: `carolina-elite-sports`
   - Keep it Public (or Private if you prefer)
   - Do NOT initialize with README (we already have one)
   - Click "Create repository"

3. **Connect Your Local Files:**
   ```bash
   # In your project directory
   git init
   git add .
   git commit -m "Initial commit - Carolina Elite Sports website"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/carolina-elite-sports.git
   git push -u origin main
   ```

### Step 3: Deploy to Netlify

#### Method A: Connect GitHub Repository (Recommended)

1. **Go to Netlify:**
   - Visit https://app.netlify.com
   - Sign in (use GitHub account for easy integration)

2. **Create New Site:**
   - Click "Add new site" → "Import an existing project"
   - Choose "Deploy with GitHub"
   - Authorize Netlify to access your GitHub repositories
   - Select your `carolina-elite-sports` repository

3. **Configure Build Settings:**
   - Site name: Choose a name (e.g., `carolina-elite-sports`)
   - Branch to deploy: `main`
   - Build command: Leave blank (static site)
   - Publish directory: Leave blank or enter `.`
   - Click "Deploy site"

4. **Wait for Deployment:**
   - Netlify will build and deploy your site (takes 1-2 minutes)
   - You'll get a URL like: `https://carolina-elite-sports.netlify.app`

#### Method B: Drag & Drop (Quick Test)

1. Go to https://app.netlify.com/drop
2. Drag your entire project folder onto the page
3. Site deploys instantly with a random URL

### Step 4: Configure Netlify Forms

1. **In Netlify Dashboard:**
   - Go to your site
   - Click "Forms" in the left sidebar
   - Your contact form should appear after first submission
   
2. **Set Up Email Notifications:**
   - Click on the "contact" form
   - Go to "Form notifications"
   - Click "Add notification"
   - Select "Email notification"
   - Enter your email address
   - Save

3. **Enable Spam Protection (Optional):**
   - Go to "Form settings"
   - Enable reCAPTCHA or Akismet

### Step 5: Add Custom Domain (Optional)

1. **Purchase a Domain:**
   - Use Netlify Domains, Namecheap, GoDaddy, or any registrar
   - Example: `carolinaelitesports.com`

2. **Add to Netlify:**
   - In Netlify dashboard, go to "Domain settings"
   - Click "Add custom domain"
   - Enter your domain name
   - Click "Verify"

3. **Update DNS Records:**
   - At your domain registrar, add these records:
   ```
   Type: A
   Name: @
   Value: 75.2.60.5
   
   Type: CNAME
   Name: www
   Value: your-site-name.netlify.app
   ```
   - Or use Netlify DNS for automatic configuration

4. **Enable HTTPS:**
   - In Netlify, go to "Domain settings" → "HTTPS"
   - Click "Verify DNS configuration"
   - Click "Provision certificate" (automatic, free SSL)

### Step 6: Update Site URLs

After deployment, update these files with your actual URL:

1. **robots.txt:**
   - Replace `your-site-url.netlify.app` with your actual URL

2. **sitemap.xml:**
   - Replace all instances of `your-site-url.netlify.app` with your actual URL

3. **Social Media Links:**
   - Update Facebook, Twitter, Instagram links in all HTML files
   - Update social media profile URLs in the footer

### Step 7: Test Your Site

1. **Test All Pages:**
   - Visit each page and check for broken links
   - Test on mobile devices
   - Verify images load correctly

2. **Test Contact Form:**
   - Submit a test message
   - Check if you receive the email notification
   - Verify form appears in Netlify dashboard

3. **Test External Links:**
   - Swift Login button
   - eSoft Login button
   - Social media links

### Step 8: Connect to GitHub for Continuous Deployment

Once connected to GitHub, any changes you push will automatically deploy:

```bash
# Make changes to your files
# Then commit and push:
git add .
git commit -m "Update: description of changes"
git push origin main
```

Netlify will automatically rebuild and deploy your site (takes 1-2 minutes).

## Updating Content

### Update Text Content

1. Edit the relevant HTML file
2. Commit changes: `git commit -am "Update: description"`
3. Push to GitHub: `git push`
4. Netlify auto-deploys in 1-2 minutes

### Add New Images

1. Add images to `/images` folder
2. Update HTML to reference new images
3. Commit: `git add . && git commit -m "Add: new images"`
4. Push: `git push`

### Update Contact Information

Edit these sections in all HTML files:
- Footer contact details
- Contact page info
- Phone numbers and addresses

## Troubleshooting

### Form Not Working
- Check Netlify Forms dashboard
- Ensure form has `data-netlify="true"` attribute
- Verify form name matches in Netlify

### Images Not Loading
- Check file names match exactly (case-sensitive)
- Verify images are in `/images` folder
- Check image paths in HTML

### Site Not Updating
- Check GitHub repository has latest changes
- Verify Netlify deployment logs
- Clear browser cache

### CSS Not Loading
- Check `styles.css` path is correct
- Verify file was committed to GitHub
- Check Netlify deploy logs for errors

## Support Resources

- **Netlify Docs:** https://docs.netlify.com
- **Netlify Support:** https://www.netlify.com/support/
- **GitHub Docs:** https://docs.github.com

## Maintenance Checklist

- [ ] Add your logo to `/images` folder
- [ ] Add staff photos
- [ ] Add alumni photos
- [ ] Add sponsor logos
- [ ] Update social media links
- [ ] Test contact form
- [ ] Verify all external links work
- [ ] Test on mobile devices
- [ ] Set up form email notifications
- [ ] Add custom domain (if desired)
- [ ] Update sitemap.xml with actual URL
- [ ] Update robots.txt with actual URL

---

**Your site is now live and ready to accept visitors!**

Any changes you make and push to GitHub will automatically deploy to your live site within minutes.
