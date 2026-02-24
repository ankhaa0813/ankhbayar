# 🚀 QUICK START CARD

## ⚡ 3-Step Launch

### Step 1: Install & Run (1 minute)
```bash
cd c:\Users\AnkhbayarDelgerchulu\Documents\Admin\portfolia\ankhbayar
bundle install
bundle exec jekyll serve --livereload
```
→ Visit `http://localhost:4000`

### Step 2: Update Your Info (5 minutes)
- Edit `index.md` → Update hero card
- Edit `cv.md` → Update experience
- Edit `_layouts/default.html` → Update email

### Step 3: Deploy to GitHub (10 minutes)
```bash
git add .
git commit -m "Initial portfolio"
git push origin main
```
→ Enable GitHub Pages in repo settings

---

## 📁 File Structure

```
ankhbayar/
├── _layouts/default.html        # Navigation & template
├── assets/css/style.scss        # All styling (glassmorphism)
├── index.md                     # Home page
├── archive.md                   # Projects grid
├── cv.md                        # Resume page
├── _config.yml                  # Jekyll settings
├── Gemfile                      # Dependencies
└── 📖 DEPLOYMENT.md            # Full guide
```

---

## 🎨 Key Features

✨ **Glassmorphism 2.0**
- Soft gradient background (blue → peach → pink)
- Frosted glass cards with blur(25px)
- Rounded corners (32px) like Pixel UI

📱 **Mobile-First Design**
- Hero stacks vertically
- Featured grid → 1 column
- Nav pill adapts (icons ↔ labels)

🎯 **3 Main Pages**
1. **Home** - Hero + 2 featured projects
2. **Archive** - 6 GitHub repos
3. **CV** - Timeline, skills, education

---

## 🛠️ Common Updates

### Change Colors
**File**: `assets/css/style.scss` (Lines 10-30)
```scss
--accent-blue: #0ea5e9;    // Primary color
--accent-pink: #ec4899;    // Accent color
--grad-blue: #e0f2fe;      // Background
```

### Update Content
| Page | File | What to Change |
|------|------|---|
| Home | `index.md` | Hero card, projects |
| Projects | `archive.md` | 6 repo cards |
| Resume | `cv.md` | Experience, skills |

### Add Project Images
1. Create `assets/images/` folder
2. Add `.png` or `.jpg` files
3. Update card HTML to use images

---

## 📊 Components

| Component | File | Lines |
|-----------|------|-------|
| Glass Card | style.scss | 83-106 |
| CTA Button | style.scss | 155-190 |
| Timeline | style.scss | 338-404 |
| Skill Pill | style.scss | 417-435 |
| Nav Pill | style.scss | 293-335 |

---

## ✅ Pre-Deploy Checklist

- [ ] `bundle install` runs without errors
- [ ] `bundle exec jekyll serve` shows no errors
- [ ] Home page displays correctly
- [ ] Mobile view responsive (DevTools)
- [ ] All links work
- [ ] Email addresses updated
- [ ] GitHub repo created (if deploying)
- [ ] GitHub Pages enabled

---

## 🔗 Important Links

| Resource | URL |
|----------|-----|
| Jekyll Docs | https://jekyllrb.com |
| GitHub Pages | https://pages.github.com |
| FontAwesome | https://fontawesome.com/icons |
| SCSS Guide | https://sass-lang.com/guide |

---

## 💬 Need Help?

📖 **Full Guides Included**:
- `DEPLOYMENT.md` - GitHub Pages setup
- `IMPLEMENTATION.md` - Complete customization
- `DESIGN_SYSTEM.md` - Visual reference
- `BUILD_SUMMARY.md` - What's included

---

## 🎯 Most Important Files

1. **style.scss** - All design (800+ lines)
2. **default.html** - Page template
3. **index.md** - Home content
4. **cv.md** - Your resume
5. **_config.yml** - Site settings

---

## 🚀 GitHub Pages URL

After enabling GitHub Pages:
```
https://YOUR_USERNAME.github.io
```

Custom domain:
```
Update DNS + create CNAME file
(See DEPLOYMENT.md for details)
```

---

## ⚙️ Build Commands

```bash
# Development (auto-reload)
bundle exec jekyll serve --livereload

# Production build
JEKYLL_ENV=production bundle exec jekyll build

# Clean & rebuild
rm -rf _site && bundle exec jekyll build
```

---

## 🎨 Colors Quick Reference

```
Primary Blue:     #0ea5e9  ←  Buttons, links
Accent Pink:      #ec4899  ←  Secondary actions
Text Dark:        #1d1d1f  ←  Main text
Text Muted:       #6b7280  ←  Descriptions
```

---

## 📱 Responsive Sizes

```
Mobile:   ≤ 768px   (Single column)
Tablet:   769-1023px (2 columns)
Desktop:  ≥ 1024px  (2+ columns)
```

---

## 🔐 Git Quick Reference

```bash
# First time setup
git init
git add .
git commit -m "Initial portfolio"
git remote add origin https://github.com/YOU/repo.git
git push -u origin main

# Updates
git add .
git commit -m "Update description"
git push
```

---

## 🎓 Tech Stack

- **Generator**: Jekyll 4.x
- **Language**: SCSS (CSS)
- **Typography**: Inter (Google Fonts)
- **Icons**: FontAwesome 6.4
- **Hosting**: GitHub Pages
- **Version Control**: Git

---

## ⏱️ Estimated Times

| Task | Time |
|------|------|
| Install & run locally | 5 min |
| Update personal info | 10 min |
| Customize colors | 5 min |
| Add project images | 10 min |
| Test mobile | 5 min |
| Push to GitHub | 5 min |
| **Total** | **~40 min** |

---

## 🎉 You're All Set!

Your glassmorphism portfolio is ready to:
- ✅ Run locally
- ✅ Deploy instantly
- ✅ Scale to production
- ✅ Customize easily

**Next step**: `bundle exec jekyll serve --livereload`

---

*For detailed guides, see: DEPLOYMENT.md | IMPLEMENTATION.md | DESIGN_SYSTEM.md*

**Built February 2026 | Version 1.0**


