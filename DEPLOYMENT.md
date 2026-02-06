# Portfolio with Profile Photo - Updated Deployment Guide

## 📸 What's New

Your portfolio now includes your professional photo in the hero section with:
- Modern card-style presentation
- Subtle gradient overlay effect
- Hover animation
- Responsive design (looks great on mobile)
- Accent decoration element

## 📦 Files You Need

```
Your Portfolio Package:
├── index.html          - Your website (updated with photo)
├── Ankit_photo.png     - Your professional photo
├── README.md           - Documentation
├── DEPLOYMENT.md       - Deployment guide
└── DESIGN.md           - Design documentation
```

## 🚀 Deployment Options

### Option 1: GitHub Pages (Most Common)

**Important**: You need to upload BOTH files!

#### Via GitHub Web Interface:

1. **Create Repository**
   - Go to https://github.com/new
   - Name: `ankitIitg.github.io`
   - Public repository
   - Create

2. **Upload Files**
   - Click "uploading an existing file"
   - Drag and drop BOTH:
     - `index.html`
     - `Ankit_photo.png`
   - Commit: "Initial deployment with photo"

3. **Enable GitHub Pages**
   - Settings → Pages
   - Source: Deploy from branch
   - Branch: main / (root)
   - Save

4. **Visit Your Site**
   - Wait 2-3 minutes
   - Go to: https://ankitIitg.github.io

#### Via Git Command Line:

```bash
# Create directory
mkdir my-portfolio
cd my-portfolio

# Initialize git
git init

# Copy both files
cp /path/to/index.html .
cp /path/to/Ankit_photo.png .

# Verify both files are there
ls -la
# Should show: index.html and Ankit_photo.png

# Add and commit
git add .
git commit -m "Initial deployment with profile photo"

# Add remote
git remote add origin https://github.com/ankitIitg/ankitIitg.github.io.git

# Push
git branch -M main
git push -u origin main
```

### Option 2: Vercel (Recommended for Custom Domain)

```bash
# Install Vercel CLI
npm install -g vercel

# Navigate to your folder with BOTH files
cd portfolio

# Verify files
ls
# Should show: index.html and Ankit_photo.png

# Deploy
vercel

# Follow prompts
```

### Option 3: Netlify (Easiest)

1. Go to https://app.netlify.com/drop
2. Create a folder containing BOTH files
3. Drag the entire folder to Netlify
4. Done! Your site is live

## 🖼️ About Your Photo

### Current Setup
- **Format**: PNG (high quality, transparent background support)
- **Position**: Right side of hero section on desktop
- **Size**: Auto-scaled for responsiveness
- **Effects**: 
  - Subtle gradient overlay (blue/purple)
  - Rounded corners (20px radius)
  - Shadow effect for depth
  - Hover lift animation
  - Decorative accent element

### Mobile Behavior
- Photo appears ABOVE the text on mobile
- Centered, smaller size (300px max-width)
- All effects maintained

### If You Want to Replace the Photo Later

1. **Keep the same name**: `Ankit_photo.png`
2. **Or update in HTML** (line ~1380):
   ```html
   <img 
       src="your-new-photo.png"  <!-- Change here -->
       alt="Ankit Kumar - Data Scientist" 
       className="hero-image"
   />
   ```
3. Re-deploy

### Recommended Photo Specs

✅ Your current photo is perfect, but for future reference:
- **Aspect Ratio**: Square or portrait (1:1 or 3:4)
- **Resolution**: 800x800px minimum
- **Format**: PNG or JPG
- **Size**: Under 500KB for fast loading
- **Background**: Professional setting (yours is great!)
- **Attire**: Professional (formal/business casual)

## 🎨 Photo Styling Customization

If you want to adjust the photo appearance, edit these CSS sections:

### Change Border Radius (Make it circular)
```css
/* Line ~275 */
.hero-image-wrapper {
    border-radius: 50%;  /* Makes it circular */
    /* or 20px for current rounded square */
}
```

### Adjust Size
```css
/* Line ~265 */
.hero-grid {
    grid-template-columns: 1fr 400px;  /* Change 400px */
}
```

### Change Overlay Color
```css
/* Line ~285 */
.hero-image-wrapper::before {
    background: linear-gradient(135deg, 
        rgba(59, 130, 246, 0.1) 0%,  /* Blue */
        rgba(139, 92, 246, 0.1) 100%  /* Purple */
    );
}
```

### Remove Effects (Minimal Look)
```css
/* Delete or comment out */
.hero-image-wrapper::before { /* Delete this */ }
.hero-image-accent { /* Delete this */ }
.hero-image-wrapper:hover { transform: none; }
```

## 📱 Testing Your Photo

After deployment:

1. **Desktop View**
   - Photo should be on the right
   - Hover should lift it slightly
   - Sharp and clear quality

2. **Mobile View**
   - Photo should be at top, centered
   - Smaller size, still clear
   - All effects working

3. **Load Speed**
   - Photo should load within 1 second
   - Use PageSpeed Insights to test

## 🐛 Troubleshooting Photo Issues

### Photo not showing
**Problem**: See broken image icon
**Solutions**:
1. Check both files uploaded to GitHub
2. Verify file name is exactly `Ankit_photo.png` (case-sensitive)
3. Check image path in HTML
4. Clear browser cache

### Photo too large/small
**Solution**: Adjust in CSS (line ~265)
```css
.hero-grid {
    grid-template-columns: 1fr 350px;  /* Make smaller */
    /* or 450px for larger */
}
```

### Photo quality poor
**Problem**: Blurry or pixelated
**Solutions**:
1. Use higher resolution image (800x800px+)
2. Save as PNG for better quality
3. Compress without losing quality (use TinyPNG)

### Photo not responsive on mobile
**Problem**: Overflows or too small
**Solution**: Check mobile CSS (line ~1160)
```css
@media (max-width: 768px) {
    .hero-image-container {
        max-width: 300px;  /* Adjust this */
    }
}
```

### Effects not working
**Problem**: No hover, no gradient
**Solutions**:
1. Check CSS is not overridden
2. Clear browser cache
3. Test in different browser
4. Check browser console for errors

## 🎯 File Structure (Important!)

Your files MUST be in the same directory:

```
ankitIitg.github.io/     (or your project folder)
├── index.html           ← Website
└── Ankit_photo.png      ← Photo (MUST be in same folder)
```

**NOT like this** (won't work):
```
ankitIitg.github.io/
├── index.html
└── images/
    └── Ankit_photo.png   ← Wrong! Different folder
```

## 🔄 Updating Your Photo Later

### Method 1: GitHub Web Interface
1. Go to repository
2. Click on `Ankit_photo.png`
3. Click edit (pencil icon)
4. Upload new photo
5. Commit changes

### Method 2: Git Command Line
```bash
# Replace the file
cp /path/to/new-photo.png Ankit_photo.png

# Commit and push
git add Ankit_photo.png
git commit -m "Update profile photo"
git push
```

### Method 3: Keep Both Photos
```bash
# Add new photo with different name
cp /path/to/new-photo.png professional-photo-2.png

# Update HTML (line ~1380)
<img src="professional-photo-2.png" ... />

# Commit
git add .
git commit -m "Update to new photo"
git push
```

## 🎨 Alternative Photo Layouts

If you want to try different layouts:

### Circular Photo (Classic)
```css
.hero-image-wrapper {
    border-radius: 50%;
    width: 300px;
    height: 300px;
    overflow: hidden;
}

.hero-image {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
```

### Photo Above Name (Centered)
```css
.hero-grid {
    grid-template-columns: 1fr;
    text-align: center;
}

.hero-image-container {
    max-width: 300px;
    margin: 0 auto 3rem;
}
```

### Photo in About Section Instead
Move the entire image code to the About section for a different layout.

## ✅ Final Checklist

Before deploying:
- [ ] Both files in same folder
- [ ] File names exact: `index.html` and `Ankit_photo.png`
- [ ] Photo looks good when you open `index.html` locally
- [ ] Photo is professional quality
- [ ] File size reasonable (<500KB)

After deploying:
- [ ] Photo loads on website
- [ ] Photo looks good on desktop
- [ ] Photo looks good on mobile
- [ ] Hover effects work
- [ ] No console errors

## 🚀 Deploy Now!

You have everything you need:
1. Updated `index.html` with photo integration
2. Your professional photo `Ankit_photo.png`
3. All documentation

Choose your deployment method above and go live! 🎉

---

**Need help?** Email: ankit22off@gmail.com

**Pro Tip**: Test locally first by opening `index.html` in your browser. If the photo shows up and looks good, it will work when deployed!
