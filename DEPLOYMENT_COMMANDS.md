# GitHub & Netlify Deployment Commands

## Complete Deployment Workflow

### Step 1: Create GitHub Repository

1. Go to https://github.com and create a new repository named `carolina-elite-sports`

### Step 2: Push to GitHub

```bash
# Add your GitHub repository URL (replace YOUR-USERNAME with actual username)
git remote add origin https://github.com/YOUR-USERNAME/carolina-elite-sports.git

# Verify remote was added
git remote -v

# Push to GitHub
git push -u origin main

# Enter your GitHub credentials when prompted
```

### Step 3: Deploy to Netlify

#### Option A: Via Netlify Dashboard (Easiest)

1. Go to https://app.netlify.com
2. Click "Add new site" → "Import an existing project"
3. Choose "GitHub"
4. Select your `carolina-elite-sports` repository
5. Leave build settings as default (netlify.toml will handle it)
6. Click "Deploy site"
7. Wait 1-2 minutes for deployment

#### Option B: Via Netlify CLI

```bash
# Install Netlify CLI globally
npm install -g netlify-cli

# Login to Netlify
netlify login

# Initialize and deploy
netlify init

# Or deploy directly
netlify deploy --prod
```

### Step 4: Configure After Deployment

```bash
# Get your site URL from Netlify dashboard
# Example: https://carolina-elite-sports.netlify.app

# Update sitemap.xml with actual URL
sed -i 's/your-site-url.netlify.app/carolina-elite-sports.netlify.app/g' sitemap.xml

# Update robots.txt
sed -i 's/your-site-url.netlify.app/carolina-elite-sports.netlify.app/g' robots.txt

# Commit and push changes
git add sitemap.xml robots.txt
git commit -m "Update: Site URL in sitemap and robots.txt"
git push origin main
```

### Step 5: Set Up Netlify Forms

1. In Netlify dashboard, go to "Forms"
2. After first form submission, it will appear
3. Click "Form notifications" → "Email notification"
4. Enter your email address
5. Save

## Quick Reference Commands

### Git Commands
```bash
# Check status
git status

# Add all changes
git add .

# Commit with message
git commit -m "Your message here"

# Push to GitHub
git push origin main

# View commit history
git log --oneline

# Check remote repository
git remote -v
```

### Making Updates After Deployment
```bash
# 1. Make your changes to HTML/CSS/JS files

# 2. Add and commit
git add .
git commit -m "Update: description of changes"

# 3. Push to GitHub
git push origin main

# 4. Netlify automatically deploys in ~2 minutes
```

### Testing Locally Before Push
```bash
# Start local server (Python 3)
python3 -m http.server 8000

# Or Python 2
python -m SimpleHTTPServer 8000

# Visit: http://localhost:8000
# Press Ctrl+C to stop server
```

### Netlify CLI Commands
```bash
# Check Netlify CLI version
netlify --version

# Login
netlify login

# Deploy to draft (test)
netlify deploy

# Deploy to production
netlify deploy --prod

# Open site in browser
netlify open:site

# Open admin dashboard
netlify open:admin

# View deploy logs
netlify logs

# Link to existing site
netlify link
```

## Troubleshooting

### If Push Rejected
```bash
# Pull latest changes first
git pull origin main --rebase

# Then push
git push origin main
```

### If Need to Update Remote URL
```bash
# Check current remote
git remote -v

# Update remote URL
git remote set-url origin https://github.com/YOUR-USERNAME/carolina-elite-sports.git
```

### If Forms Not Working
1. Ensure form has `data-netlify="true"` attribute
2. Ensure form has `name="contact"` attribute
3. Check Netlify dashboard → Forms section
4. Submit a test form to activate it

### If Deployment Fails
1. Check Netlify deploy logs
2. Ensure no syntax errors in HTML/CSS/JS
3. Check netlify.toml configuration
4. Try manual deploy via Netlify CLI

## Custom Domain Setup

### Purchase Domain
1. Buy from Netlify, Namecheap, GoDaddy, etc.

### Add to Netlify
```bash
# Via CLI
netlify domains:add yourdomain.com

# Or via dashboard:
# Go to Domain settings → Add custom domain → Enter domain → Verify
```

### Update DNS Records
At your domain registrar, add:

```
Type: A
Name: @
Value: 75.2.60.5

Type: CNAME
Name: www
Value: your-site-name.netlify.app
```

### Enable HTTPS
Netlify automatically provisions SSL certificate (free via Let's Encrypt)

## Contact Form Spam Protection

### Add reCAPTCHA
```html
<!-- Add to form tag -->
<form name="contact" method="POST" data-netlify="true" data-netlify-recaptcha="true">
  ...
  <!-- Add this before submit button -->
  <div data-netlify-recaptcha="true"></div>
  ...
</form>
```

### Enable Akismet
1. In Netlify dashboard → Forms
2. Click "Form settings"
3. Enable Akismet spam filtering

## Environment Variables (if needed)

```bash
# Set via CLI
netlify env:set KEY value

# Or via dashboard:
# Site settings → Environment variables → Add variable
```

## Useful Resources

- Netlify Docs: https://docs.netlify.com
- GitHub Docs: https://docs.github.com
- Git Cheat Sheet: https://training.github.com/downloads/github-git-cheat-sheet/

---

## Example Complete Workflow

```bash
# 1. Create GitHub repo at github.com

# 2. In your local project:
git remote add origin https://github.com/YOUR-USERNAME/carolina-elite-sports.git
git push -u origin main

# 3. Go to Netlify and connect GitHub repo

# 4. After deployment, update URLs:
# Replace YOUR-SITE in sitemap.xml and robots.txt

# 5. Commit and push
git add .
git commit -m "Update: site URLs"
git push

# 6. Configure form notifications in Netlify dashboard

# 7. Add your images to /images folder

# 8. Test everything!

# Done! 🎉
```
