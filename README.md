# Ankhbayar Delgerchuluun | Portfolio

A modern, responsive personal portfolio website built with **Jekyll**, **SCSS**, and **Glassmorphism 2.0** design principles.

## 🎯 Features

- **Glassmorphism Design**: Soft, frosted glass UI elements with backdrop blur effects
- **Mobile-First Responsive**: Perfect on all devices (mobile, tablet, desktop)
- **Fast Static Generation**: Jekyll-powered for GitHub Pages deployment
- **Modern Aesthetics**: Google Pixel-inspired design with rounded corners
- **Smooth Animations**: CSS transitions and hover effects
- **Accessible**: Semantic HTML with ARIA labels and FontAwesome icons

## 📁 Project Structure

```
ankhbayar/
├── _layouts/
│   └── default.html          # Main layout template with floating nav pill
├── assets/
│   └── css/
│       └── style.scss        # Complete SCSS stylesheet with glassmorphism
├── _config.yml               # Jekyll configuration
├── index.md                  # Home page with hero & featured projects
├── archive.md                # GitHub repository archive
├── cv.md                     # CV with timeline & skills
└── README.md                 # This file
```

## 🚀 Quick Start

### 1. Install Jekyll & Dependencies
```bash
gem install bundler jekyll
bundle install
```

### 2. Run Locally
```bash
bundle exec jekyll serve
# Visit http://localhost:4000
```

### 3. Build for Production
```bash
bundle exec jekyll build
```

## 🎨 Design Philosophy

### Color Palette
- **Gradient Background**: Radial blend of peach, light blue, and soft pink
- **Accent Colors**: Sky blue (#0ea5e9), Hot pink (#ec4899), Emerald green (#10b981)
- **Glass Elements**: Semi-transparent white with backdrop blur (25px)

### Typography
- **Font**: Inter (via Google Fonts)
- **Weight Scale**: 300, 400, 500, 600, 700
- **Line Height**: 1.7 for readability

### Components

#### Glass Cards
- `backdrop-filter: blur(25px)`
- `background: rgba(255, 255, 255, 0.15)`
- `border-radius: 32px` (desktop), `24px` (mobile)
- `1px solid` subtle white border

#### Navigation Pill
- Floating on bottom-right (desktop)
- Compact on mobile with labels
- Glassmorphic styling with icons from FontAwesome

#### Featured Project Cards
- Image placeholder with gradient
- High-contrast action buttons
- Responsive grid layout

#### Timeline (CV Page)
- Vertical timeline with dot connectors
- Alternating left/right layout on desktop
- Stacked on mobile

## 📱 Responsive Breakpoints

- **Desktop**: 1024px+ (full 2-column layouts)
- **Tablet**: 769px - 1023px (flexible layouts)
- **Mobile**: ≤768px (single column, compact navigation)

## 🔧 Customization

### Update Personal Info
Edit the frontmatter in `index.md`, `cv.md`, `archive.md` and the contact email in `_layouts/default.html`

### Change Colors
Update CSS variables in `assets/css/style.scss` (lines 10-30):
```scss
--accent-blue: #0ea5e9;
--accent-pink: #ec4899;
--grad-blue: #e0f2fe;
```

### Modify Repository List
Edit the archive grid cards in `archive.md`

### Update Experience
Edit the timeline items in `cv.md`

## 🌐 Deployment

### GitHub Pages
1. Push to GitHub repository
2. Enable GitHub Pages in repository settings
3. Site deployed to `https://username.github.io`

### Custom Domain
1. Add `CNAME` file with your domain
2. Update DNS records to point to GitHub Pages

## 📦 Dependencies

- **Jekyll 4.x**
- **SCSS** (built-in with Jekyll)
- **Google Fonts** (Inter)
- **FontAwesome 6.4** (CDN)

## 🛠 Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- iOS 13+
- Android 7+
- Supports CSS Backdrop Filter and Grid

## 📄 License

Personal portfolio - feel free to use as inspiration for your own!

## ✉️ Contact

Email: a.delgerchuluun@stud.uni-goettingen.de

---

Built with ❤️ using Jekyll & SCSS
