# Clarke's Pro Tree Service - Website

Professional website for Clarke's Pro Tree Service, Tampa's backyard tree specialists.

## Project Structure

```
clarkes-pro-site/
├── index.html          # Main homepage
├── css/
│   └── styles.css      # All styling with brand colors
├── js/
│   └── main.js         # Mobile menu, smooth scroll, interactions
├── images/             # Image assets (to be added)
│   ├── clarkes-pro-logo.png
│   ├── hero-equipment.jpg
│   ├── nifty-narrow-lift.jpg
│   ├── articulated-bobcat.jpg
│   └── [other project photos]
└── README.md           # This file
```

## Brand Colors (From Logo)

- **Orange**: #D97C3F (Primary CTA, accents)
- **Dark Green**: #2D5016 (Headings, footer, secondary buttons)
- **Medium Green**: #4A7C2B (Supporting elements)
- **Cream**: #FFF8F0 (Section backgrounds)
- **White**: #ffffff (Primary background)

## Features

- **Responsive Design**: Mobile-first, works on all devices
- **Fast Loading**: Optimized for local SEO
- **Contact Forms**: Formspree integration (needs setup)
- **Smooth Scrolling**: Professional user experience
- **Sticky Navigation**: Always accessible
- **Google Reviews**: Ready for integration
- **Call Tracking**: Click-to-call on mobile

## Setup Instructions

### 1. Add Images

Upload the following images to the `/images` directory:

- `clarkes-pro-logo.png` - Main logo (the one with mature tree in orange ring)
- `hero-equipment.jpg` - Nifty Narrow lift or equipment showcase
- `nifty-narrow-lift.jpg` - Close-up of the lift
- `articulated-bobcat.jpg` - Bobcat equipment
- Additional before/after photos as available

### 2. Configure Formspree

1. Go to https://formspree.io/
2. Create a free account
3. Create a new form
4. Copy your form endpoint ID
5. In `index.html`, replace `YOUR_FORM_ID` with your actual ID on line 313:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```

### 3. Update Contact Information

Verify these details in `index.html`:

- Phone number: (813) 516-6973 (appears multiple times)
- Email: info@clarkespro.com
- Google Reviews link (line 422)

## GitHub Pages Deployment

### Option 1: Direct Upload to GitHub

1. Create new repository: `clarkespro-website`
2. Upload all files maintaining the directory structure
3. Go to Settings > Pages
4. Set source to `main` branch
5. Save and wait for deployment

### Option 2: Using GitHub CLI

```bash
# From this directory
git init
git add .
git commit -m "Initial Clarke's Pro website"
git branch -M main
git remote add origin https://github.com/[username]/clarkespro-website.git
git push -u origin main

# Then enable GitHub Pages in repository settings
```

### Custom Domain Setup

1. In repository settings, add custom domain: `clarkespro.com`
2. In domain registrar (GoDaddy), add DNS records:
   ```
   Type: A
   Host: @
   Points to: 185.199.108.153
   
   Type: A
   Host: @
   Points to: 185.199.109.153
   
   Type: A
   Host: @
   Points to: 185.199.110.153
   
   Type: A
   Host: @
   Points to: 185.199.111.153
   
   Type: CNAME
   Host: www
   Points to: [username].github.io
   ```
3. Wait for DNS propagation (24-48 hours)
4. Enable HTTPS in GitHub Pages settings

## Testing Checklist

Before going live:

- [ ] All images display correctly
- [ ] Logo appears in nav and footer
- [ ] Phone numbers are click-to-call on mobile
- [ ] Contact form submits successfully
- [ ] All links work (especially Google Reviews)
- [ ] Mobile menu opens/closes
- [ ] Smooth scrolling works
- [ ] Site loads fast (test on mobile)
- [ ] All text is accurate (no placeholder content)

## Content Updates

### To Update Services:
Edit the `.services-grid` section in `index.html` (starting around line 229)

### To Update Service Areas:
Edit the `.areas-list` section in `index.html` (starting around line 339)

### To Change Colors:
Edit CSS variables in `css/styles.css` (lines 3-15)

### To Add Pages:
Create new HTML file, copy header/nav from `index.html`, link from navigation

## Phase 2: Neighborhood Pages

Future enhancement:
- `/neighborhoods/new-suburb-beautiful.html`
- `/neighborhoods/forest-hills.html`
- `/neighborhoods/temple-terrace.html`
- etc.

Each will follow same structure as main page but with neighborhood-specific content.

## Performance Optimization

Current setup is optimized for:
- Google PageSpeed: Target 90+
- Mobile-first loading
- Minimal JavaScript
- Optimized images (use WebP when possible)
- Local SEO signals

## Support

For questions or updates:
- Contact: Mike Goetz / RageDesigner
- Framework: Strategic Intelligence Operating System
- Deployment: GitHub Pages autonomous system

---

**Built**: January 2026  
**Status**: Production Ready (pending image upload and Formspree setup)  
**Hosting**: GitHub Pages  
**Domain**: clarkespro.com
