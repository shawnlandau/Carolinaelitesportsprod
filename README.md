# Carolina Elite Sports Website

A professional static website for Carolina Elite Sports, home of the Carolina Rays baseball training facility in Myrtle Beach, SC.

## Features

- 7 fully responsive pages (Home, About, Staff, Camps/Tryouts, Academy, Alumni, Sponsors)
- Mobile-first responsive design
- Netlify Forms integration for contact form
- Professional blue/navy color scheme
- Fast loading and optimized performance
- SEO-friendly semantic HTML
- Smooth animations and transitions
- Social media integration
- External login portals (Swift and eSoft)

## Pages

- **Home** - Hero section with mission statement and contact form
- **About** - Information about the facility and approach
- **Staff** - Coaching staff profiles
- **Camps/Tryouts** - Training programs and camps information
- **Academy** - Year-round academy program details
- **Alumni** - Success stories and player achievements
- **Sponsors** - Current sponsors and sponsorship opportunities

## Deployment to Netlify

### Option 1: Deploy via GitHub (Recommended)

1. **Create a GitHub Repository**
   ```bash
   # Initialize git (if not already done)
   git init
   
   # Add all files
   git add .
   
   # Commit
   git commit -m "Initial commit - Carolina Elite Sports website"
   
   # Add your GitHub repository as remote
   git remote add origin https://github.com/yourusername/carolina-elite-sports.git
   
   # Push to GitHub
   git push -u origin main
   ```

2. **Connect to Netlify**
   - Go to [Netlify](https://app.netlify.com)
   - Click "Add new site" → "Import an existing project"
   - Choose "GitHub" and authorize Netlify
   - Select your repository
   - Build settings will be automatically detected from `netlify.toml`
   - Click "Deploy site"

3. **Custom Domain (Optional)**
   - In Netlify dashboard, go to "Domain settings"
   - Add your custom domain
   - Update DNS records as instructed

### Option 2: Deploy via Drag & Drop

1. Go to [Netlify Drop](https://app.netlify.com/drop)
2. Drag and drop the entire project folder
3. Site will be instantly deployed

### Option 3: Deploy via Netlify CLI

```bash
# Install Netlify CLI
npm install -g netlify-cli

# Login to Netlify
netlify login

# Deploy
netlify deploy --prod
```

## File Structure

```
carolina-elite-sports/
├── index.html              # Home page
├── about.html              # About page
├── staff.html              # Staff page
├── camps-tryouts.html      # Camps & Tryouts page
├── academy.html            # Academy page
├── alumni.html             # Alumni page
├── sponsors.html           # Sponsors page
├── netlify.toml            # Netlify configuration
├── README.md               # This file
├── css/
│   └── styles.css          # Main stylesheet
├── js/
│   └── main.js             # Main JavaScript file
└── images/                 # Image directory (add your images here)
    ├── carolina-rays-logo.png       (placeholder - add your logo)
    ├── staff-placeholder.jpg        (placeholder - add staff photos)
    ├── alumni-placeholder.jpg       (placeholder - add alumni photos)
    └── sponsor-placeholder.png      (placeholder - add sponsor logos)
```

## Adding Images

Replace the placeholder images in the `/images` folder:

1. **Carolina Rays Logo** - `images/carolina-rays-logo.png`
   - Recommended size: 300x100px (or maintain aspect ratio)
   - Format: PNG with transparent background

2. **Staff Photos** - `images/staff-[name].jpg`
   - Recommended size: 400x400px (square)
   - Format: JPG or PNG

3. **Alumni Photos** - `images/alumni-[name].jpg`
   - Recommended size: 600x450px (4:3 aspect ratio)
   - Format: JPG or PNG

4. **Sponsor Logos** - `images/sponsor-[name].png`
   - Recommended sizes: 300x200px (or maintain aspect ratio)
   - Format: PNG with transparent background

## Netlify Forms Setup

The contact form is already configured for Netlify Forms. After deployment:

1. Go to your Netlify dashboard
2. Navigate to "Forms" section
3. You'll see the "contact" form
4. Set up email notifications under "Form notifications"
5. Optionally add spam filtering with Akismet

## Customization

### Update Contact Information

Edit the contact details in the footer and contact sections of each page:
- Phone: `843-286-8147`
- Address: Update facility addresses as needed
- Hours: Modify operating hours
- Social media: Update links to actual social media profiles

### Update Colors

Edit the CSS variables in `css/styles.css`:
```css
:root {
    --primary-blue: #003d7a;
    --secondary-blue: #0066cc;
    --navy: #001f3f;
    --accent-gold: #ffd700;
}
```

### Update Content

All content can be edited directly in the HTML files. Each page is self-contained and easy to modify.

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance

- Optimized CSS and JavaScript
- Lazy loading for images
- Minimal external dependencies
- Fast loading times
- Mobile-optimized

## Security

- Security headers configured in netlify.toml
- XSS protection
- HTTPS enforced by Netlify
- Form spam protection available

## Support

For questions or issues with the website, contact the web developer or refer to:
- [Netlify Documentation](https://docs.netlify.com)
- [MDN Web Docs](https://developer.mozilla.org)

## License

© 2023 Carolina Elite Sports | All Rights Reserved

---

**Built with HTML, CSS, and JavaScript**
**Optimized for Netlify deployment**
