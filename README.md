# Ankit Kumar - Professional Portfolio Website

A modern, production-ready portfolio website built with React showcasing AI/ML engineering experience, projects, and technical expertise.

## 🎯 Features

- **Modern Design**: Technical brutalism meets minimalist aesthetics
- **Fully Responsive**: Mobile-first design that works on all devices
- **Performance Optimized**: Single-file React application with fast load times
- **SEO Friendly**: Proper meta tags and semantic HTML
- **Production Ready**: Clean code, organized structure, professional presentation

## 🚀 Quick Start

### Option 1: Direct Deployment to GitHub Pages (Recommended)

1. **Create a new repository** on GitHub named `username.github.io` (replace `username` with your GitHub username)

2. **Upload the file**:
   ```bash
   git clone https://github.com/yourusername/yourusername.github.io.git
   cd yourusername.github.io
   cp /path/to/index.html .
   git add index.html
   git commit -m "Initial portfolio deployment"
   git push origin main
   ```

3. **Access your site** at `https://yourusername.github.io`

### Option 2: Deploy to Vercel

1. Install Vercel CLI:
   ```bash
   npm install -g vercel
   ```

2. Deploy:
   ```bash
   cd portfolio
   vercel
   ```

3. Follow the prompts and your site will be live in seconds!

### Option 3: Local Testing

Simply open `index.html` in any modern web browser. No build process required!

## 📁 Project Structure

```
portfolio/
├── index.html          # Complete single-file application
└── README.md          # This file
```

## 🎨 Customization Guide

### Updating Content

All content is embedded in the HTML file. Search for these sections to update:

#### Personal Information
```javascript
// Line ~450: Hero section
<h1>Ankit <span className="gradient-text">Kumar</span></h1>

// Update email, GitHub, LinkedIn links
<a href="mailto:your.email@gmail.com">
<a href="https://github.com/yourusername">
```

#### Experience
```javascript
// Line ~750: Experience section
<div className="experience-card">
  <h3>Your Job Title</h3>
  <div className="experience-company">Company Name</div>
  // Update achievements, metrics, tech stack
</div>
```

#### Projects
```javascript
// Line ~950: Projects section
<div className="project-card">
  <h3 className="project-title">Project Name</h3>
  // Update description, solution, results
</div>
```

#### Skills
```javascript
// Line ~1100: Skills section
<div className="skill-category">
  <span className="skill-item">Your Skill</span>
</div>
```

### Color Scheme

To change colors, modify CSS variables (around line 25):

```css
:root {
    --primary: #0F172A;        /* Main dark color */
    --accent: #3B82F6;         /* Accent blue */
    --success: #10B981;        /* Success green */
    /* ... modify other colors ... */
}
```

### Typography

Fonts are loaded from Google Fonts (line 13). To change:

```html
<!-- Replace with your preferred fonts -->
<link href="https://fonts.googleapis.com/css2?family=YourFont&display=swap" rel="stylesheet">
```

Then update CSS variables:
```css
--font-display: 'YourDisplayFont', sans-serif;
--font-body: 'YourBodyFont', sans-serif;
```

## 🔧 Adding New Projects

To add a new project, copy this template in the Projects section:

```javascript
<div className="project-card">
    <div className="project-header">
        <div className="project-type">PROJECT TYPE</div>
        <h3 className="project-title">Project Name</h3>
        <div className="project-org">Organization | Date</div>
    </div>
    <p className="project-description">
        Brief description of the project
    </p>
    <div className="project-details">
        <div className="project-section">
            <h4>Solution</h4>
            <ul>
                <li>Key point 1</li>
                <li>Key point 2</li>
            </ul>
        </div>
        <div className="project-result">
            <p><strong>Results:</strong></p>
            <p>✓ Achievement 1</p>
            <p>✓ Achievement 2</p>
        </div>
    </div>
    <div className="tech-stack">
        <span className="tech-tag">Tech 1</span>
        <span className="tech-tag">Tech 2</span>
    </div>
    <div className="project-links">
        <a href="https://github.com/..." className="project-link">
            <IconGithub />
            View Code
        </a>
    </div>
</div>
```

## 🌐 Domain Configuration

### Custom Domain with GitHub Pages

1. Go to repository Settings → Pages
2. Add your custom domain (e.g., `ankitkumar.dev`)
3. Create a `CNAME` file in your repository:
   ```
   ankitkumar.dev
   ```
4. Configure DNS settings at your domain provider:
   ```
   Type: A
   Name: @
   Value: 185.199.108.153
   Value: 185.199.109.153
   Value: 185.199.110.153
   Value: 185.199.111.153
   
   Type: CNAME
   Name: www
   Value: yourusername.github.io
   ```

### Custom Domain with Vercel

Vercel handles DNS automatically. Just add your domain in project settings.

## 📱 Mobile Responsiveness

The site is fully responsive with breakpoints at:
- Desktop: 1200px max-width
- Tablet: 768px
- Mobile: 480px

Test on different devices or use browser DevTools.

## ⚡ Performance Optimization

Current optimizations:
- Single HTML file (no additional requests)
- Minimal external dependencies (fonts + React CDN)
- CSS animations using GPU acceleration
- Lazy loading where possible

### Further Optimizations (Optional)

1. **Self-host fonts**: Download Google Fonts and include locally
2. **Inline React**: Bundle React locally instead of CDN
3. **Minify**: Use HTML minifier for production
4. **Image optimization**: If adding images, use WebP format

## 🐛 Troubleshooting

### Links not working
- Ensure all `href` attributes are updated with correct URLs
- Check that external links have `target="_blank"`

### Styling issues
- Clear browser cache (Ctrl/Cmd + Shift + R)
- Check browser console for errors
- Ensure all CSS variables are defined

### Deployment issues on GitHub Pages
- Repository must be named `username.github.io`
- File must be named `index.html`
- Branch must be set to `main` (or `master`) in Settings → Pages

## 📊 Analytics (Optional)

Add Google Analytics by inserting before `</head>`:

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

## 🔒 SEO Best Practices

Already implemented:
- ✅ Meta description
- ✅ Meta keywords
- ✅ Semantic HTML structure
- ✅ Alt texts for icons
- ✅ Fast load time
- ✅ Mobile responsive

To improve further:
1. Add `sitemap.xml`
2. Create `robots.txt`
3. Add Open Graph tags for social sharing
4. Submit to Google Search Console

## 📝 License

This portfolio template is open source. Feel free to use and modify for your own portfolio.

## 🤝 Support

For issues or questions:
- Create an issue on GitHub
- Email: ankit22off@gmail.com

## 🚀 Future Enhancements

Potential additions:
- [ ] Blog section with MDX support
- [ ] Dark/Light theme toggle
- [ ] Dynamic GitHub stats integration
- [ ] Project filtering by technology
- [ ] Animated page transitions
- [ ] Contact form with backend

---

**Built with ❤️ using React**

Last Updated: February 2026
