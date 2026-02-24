# 🚀 Quick Start & Deployment Guide

## ⚡ 5-Minute Setup

### Prerequisites
- Ruby 2.7+ installed
- Git installed
- GitHub account

### Step 1: Install Dependencies
```bash
cd c:\Users\AnkhbayarDelgerchulu\Documents\Admin\portfolia\ankhbayar
bundle install
```

### Step 2: Run Locally
```bash
bundle exec jekyll serve --livereload
# Visit http://localhost:4000
```

### Step 3: View in Browser
- Home: http://localhost:4000/
- Archive: http://localhost:4000/archive/
- CV: http://localhost:4000/cv/

---

## 📝 Content Updates

### Update Your Information

**File: `index.md`** (Hero & Featured Projects)
- Line 7: Change "Ankhbayar Delgerchuluun" to your name
- Line 8: Update subtitle (e.g., "Full Stack Developer")
- Line 9-11: Update professional description
- Line 16: Change email in "Get in Touch" button
- Line 31-38: Update Aral Sea project details
- Line 45-52: Update thesis/portfolio project details

**File: `cv.md`** (Experience & Education)
- Lines 10-68: Update 3 experience entries (dates, companies, descriptions)
- Lines 75-84: Modify skill pills (add/remove skills)
- Lines 88-105: Update education entries
- Lines 110-125: Edit language proficiencies

**File: `archive.md`** (GitHub Projects)
- Lines 20-63: Update 6 repository entries
- Change names, descriptions, stars, languages

**File: `_layouts/default.html`** (Navigation & Contact)
- Line 22: Update email address (appears in nav)
- Line 9: Update page title if needed

---

## 🎨 Design Customization

### Change Colors (Edit `assets/css/style.scss`)

**Background Gradient** (Lines 16-18):
```scss
--grad-blue: #e0f2fe;      // Change this for different blue
--grad-peach: #fdf2f8;     // Change for different peach
--grad-pink: #fce7f3;      // Change for different pink
```

**Accent Colors** (Lines 23-25):
```scss
--accent-blue: #0ea5e9;    // Primary button & links
--accent-pink: #ec4899;    // Secondary buttons
--accent-green: #10b981;   // Stats & accents
```

**Example: Dark Mode Gradient**:
```scss
--grad-blue: #1e3c72;
--grad-peach: #2a5298;
--grad-pink: #0f2027;
```

### Adjust Spacing (Lines 29-37)
```scss
--space-lg: 2rem;          // Card padding (increase for more breathing room)
--space-xl: 2.5rem;        // Larger sections
```

### Change Border Radius (Lines 41-43)
```scss
--radius-lg: 32px;         // Main cards (decrease for less rounded)
--radius-md: 20px;         // Medium elements
```

### Modify Backdrop Blur (Line 223)
```scss
backdrop-filter: blur(25px);  // Increase to 30px for more blur, 15px for less
```

---

## 🖼️ Add Project Images

### 1. Create Images Folder
```bash
mkdir assets/images
```

### 2. Add Image Files
- Place `.png` or `.jpg` files in `assets/images/`
- Recommended size: 600×400px minimum
- Optimize using TinyPNG or Squoosh

### 3. Update Featured Cards in `index.md`

Replace emoji placeholders (Lines 36 & 53):
```html
<!-- Before: -->
<div class="project-image">🛰️</div>

<!-- After: -->
<div class="project-image">
    <img src="{{ '/assets/images/aral-sea.jpg' | relative_url }}" alt="Aral Sea Monitoring">
</div>
```

### 4. Add CSS for Images (in `assets/css/style.scss`)
```scss
.project-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 12px;
}
```

---

## 🔗 GitHub Pages Deployment

### Step 1: Initialize Git (if needed)
```bash
git init
git add .
git commit -m "Initial portfolio website"
```

### Step 2: Push to GitHub
```bash
git remote add origin https://github.com/YOUR_USERNAME/ankhbayar-portfolio.git
git push -u origin main
```

### Step 3: Enable GitHub Pages
1. Go to https://github.com/YOUR_USERNAME/ankhbayar-portfolio
2. Click **Settings** → **Pages**
3. Select **Source**: Deploy from a branch
4. Select branch: **main**
5. Select folder: **/ (root)**
6. Click **Save**

### Step 4: Wait for Build
- GitHub will show status: "Building..." → "Your site is live at..."
- Takes ~1-2 minutes
- Visit your site URL (shown in Pages settings)

### Using Custom Domain
1. Create `CNAME` file in root with your domain:
   ```
   myportfolio.com
   ```

2. Update DNS records:
   - Go to your domain registrar (GoDaddy, Namecheap, etc.)
   - Add DNS record:
     - Type: A
     - Name: @
     - Value: 185.199.108.153
   
   OR (simpler):
     - Type: CNAME
     - Name: www
     - Value: YOUR_USERNAME.github.io

3. Add domain to GitHub Pages:
   - GitHub Settings → Pages
   - Custom domain: myportfolio.com
   - Check "Enforce HTTPS"

---

## ✅ Pre-Launch Checklist

- [ ] All personal information updated (name, email, dates)
- [ ] Project descriptions match your actual work
- [ ] No typos in content
- [ ] Links working (test locally first)
- [ ] Images optimized & placed
- [ ] Mobile view tested (Chrome DevTools)
- [ ] Colors match your brand
- [ ] All social links updated
- [ ] Email works in contact buttons
- [ ] GitHub repository setup & public
- [ ] Custom domain configured (if using)
- [ ] GitHub Pages enabled
- [ ] HTTPS enforced

---

## 🧪 Testing Before Deploy

### Local Testing
```bash
# Start server
bundle exec jekyll serve

# Test in browser
# - Desktop: Full window
# - Mobile: Chrome DevTools (Ctrl+Shift+I → Toggle device)
```

### Quick Mobile Test Checklist
- [ ] Navigation pill appears at top on mobile
- [ ] Hero card stacks vertically
- [ ] Featured grid becomes single column
- [ ] Text readable on small screen
- [ ] Buttons full-width on mobile
- [ ] No horizontal scroll
- [ ] Images responsive

---

## 🔐 Privacy & SEO

### Add Meta Tags (Optional, in `_layouts/default.html`)
```html
<meta name="robots" content="index, follow">
<meta name="language" content="English">
<meta name="revisit-after" content="7 days">
<meta name="author" content="Your Name">
```

### Create `robots.txt` (in root)
```
User-agent: *
Allow: /
Sitemap: https://yourdomain.com/sitemap.xml
```

### Google Analytics (Optional)
Add to `_layouts/default.html` before `</body>`:
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_ID');
</script>
```

---

## 🛠️ Common Tasks

### Add a Blog Post
1. Create `_posts/2024-02-20-my-title.md`
2. Add frontmatter:
   ```yaml
   ---
   layout: default
   title: My Blog Post Title
   date: 2024-02-20
   ---
   ```
3. Write content in Markdown
4. Automatically appears on home page

### Update Navigation Links
Edit `_layouts/default.html` lines 23-38 (`<nav>` section)

### Change Font
Edit `_layouts/default.html` line 7:
```html
<link href="https://fonts.googleapis.com/css2?family=YOUR_FONT:wght@300;400;600;700&display=swap" rel="stylesheet">
```

### Add Social Links
Add to hero section in `index.md`:
```html
<div style="display: flex; gap: 1rem;">
    <a href="https://twitter.com/yourhandle" class="cta-button secondary">
        <i class="fab fa-twitter"></i>
    </a>
    <a href="https://linkedin.com/in/yourprofile" class="cta-button secondary">
        <i class="fab fa-linkedin"></i>
    </a>
</div>
```

---

## 📊 Performance Optimization

### Minify CSS
SCSS auto-minifies in production build:
```bash
JEKYLL_ENV=production bundle exec jekyll build
```

### Optimize Images
- Use WebP format when possible
- Compress with TinyPNG (80% size reduction)
- Use `loading="lazy"` for images below fold

### Check Performance
- Lighthouse (Chrome DevTools)
- GTmetrix: https://gtmetrix.com
- Google PageSpeed: https://pagespeed.web.dev

---

## 🆘 Troubleshooting

| Problem | Solution |
|---------|----------|
| Build fails locally | Run `bundle install` again |
| Styles not updating | Delete `_site/` folder, restart Jekyll |
| GitHub Pages shows error | Check `_config.yml` for YAML errors |
| Mobile nav broken | Clear browser cache |
| Images not showing | Check relative paths with `relative_url` filter |
| Email links don't work | Ensure `mailto:` prefix in href |

---

## 📚 Resources

- **Jekyll Docs**: https://jekyllrb.com/docs/
- **SCSS Guide**: https://sass-lang.com/guide
- **CSS Grid**: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout
- **GitHub Pages**: https://pages.github.com/
- **FontAwesome Icons**: https://fontawesome.com/icons

---

## 💬 Quick Reference: File Purposes

| File | Purpose |
|------|---------|
| `_config.yml` | Jekyll configuration & site settings |
| `_layouts/default.html` | Main HTML template for all pages |
| `assets/css/style.scss` | All styling rules & variables |
| `index.md` | Home page content |
| `archive.md` | Projects/repositories page |
| `cv.md` | Resume/CV page |
| `Gemfile` | Ruby dependencies list |
| `.gitignore` | Files to exclude from git |

---

**Ready to deploy? Good luck! 🚀**

*For support, check Jekyll docs or GitHub Pages docs*
