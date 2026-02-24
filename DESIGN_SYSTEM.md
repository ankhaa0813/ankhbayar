# 🎨 Glassmorphism Design System - Style Guide

## Color Palette

### Primary Gradient (Background)
```
Background: Radial Gradient
├─ Center (0%):    #e0f2fe (Light Blue - Sky)
├─ Middle (50%):   #fdf2f8 (Peach - Warm)
└─ Edge (100%):    #fce7f3 (Soft Pink - Rose)
```

### Accent Colors
| Color | Hex | Usage | Example |
|-------|-----|-------|---------|
| Sky Blue | `#0ea5e9` | Primary buttons, links, hover states | CTA buttons, nav highlights |
| Hot Pink | `#ec4899` | Secondary actions, accents | Featured buttons, highlights |
| Emerald | `#10b981` | Success, stats, badges | Star icons, positive indicators |

### Text Colors
| Name | Hex | Usage |
|------|-----|-------|
| Dark | `#1d1d1f` | Main body text, headings |
| Muted | `#6b7280` | Secondary text, descriptions |
| Light | `#f3f4f6` | Light backgrounds, inverted text |

---

## Typography System

### Font Family
```
Primary: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif
Weight Scale: 300 (light) → 400 (regular) → 500 (medium) → 600 (semibold) → 700 (bold)
Line Height: 1.3 (headings), 1.7 (body)
```

### Type Scale
```
Base: 1rem (16px)

Scale Hierarchy:
├─ xs:  0.75rem  (12px)  - Small labels, badges
├─ sm:  0.875rem (14px)  - Descriptions, meta
├─ base: 1rem    (16px)  - Body text
├─ lg:  1.125rem (18px)  - Navigation, emphasis
├─ xl:  1.25rem  (20px)  - Section headers
├─ 2xl: 1.5rem   (24px)  - Major headings
├─ 3xl: 1.875rem (30px)  - Page titles
└─ 4xl: 2.25rem  (36px)  - Hero title
```

### Usage Guidelines
- **h1**: Page main title (36px, 700 weight)
- **h2**: Section title (30px, 700 weight)
- **h3**: Card titles (24px, 600 weight)
- **h4**: Subsection (20px, 600 weight)
- **p**: Body copy (16px, 400 weight, 1.7 line-height)
- **Small**: Meta info (14px, 400 weight)

---

## Spacing Scale

```
xs:  0.5rem  (8px)
sm:  1rem    (16px)
md:  1.5rem  (24px)
lg:  2rem    (32px)
xl:  2.5rem  (40px)
2xl: 3rem    (48px)
```

### Usage
- **Padding**: Cards, containers
- **Margin**: Section separation
- **Gap**: Flex/grid item spacing

---

## Border Radius System

| Size | Desktop | Mobile | Usage |
|------|---------|--------|-------|
| sm | 12px | 12px | Small elements, pills |
| md | 20px | 20px | Medium buttons, badges |
| lg | 32px | 24px | Main glass cards |
| full | 999px | 999px | Pill shapes, nav |

---

## Component Library

### 1️⃣ Glass Card (Base Component)

**Properties**:
```scss
Background:     rgba(255, 255, 255, 0.15)
Backdrop Filter: blur(25px)
Border:         1px solid rgba(255, 255, 255, 0.3)
Border Radius:  32px (desktop), 24px (mobile)
Padding:        2.5rem (desktop), 1.5rem (mobile)
Box Shadow:     0 8px 32px rgba(0, 0, 0, 0.05)
```

**Hover State**:
```scss
Background:     rgba(255, 255, 255, 0.25)
Transform:      translateY(-4px)
Box Shadow:     0 12px 48px rgba(0, 0, 0, 0.08)
Transition:     all 0.3s ease
```

**Code**:
```scss
.glass-card {
    background: rgba(255, 255, 255, 0.15);
    backdrop-filter: blur(25px);
    -webkit-backdrop-filter: blur(25px);
    border: 1px solid rgba(255, 255, 255, 0.3);
    border-radius: 32px;
    padding: 2.5rem;
    transition: all 0.3s ease;
    
    &:hover {
        background: rgba(255, 255, 255, 0.25);
        transform: translateY(-4px);
        box-shadow: 0 12px 48px rgba(0, 0, 0, 0.08);
    }
}
```

---

### 2️⃣ CTA Button

**Variants**:

**Primary (Blue)**:
```scss
Background:   #0ea5e9
Text Color:   white
Padding:      0.5rem 1rem
Border Radius: 20px
Box Shadow:   0 4px 15px rgba(14, 165, 233, 0.3)
Font Weight:  600
```

**Secondary (Glass)**:
```scss
Background:   rgba(255, 255, 255, 0.2)
Text Color:   #1d1d1f
Border:       1px solid rgba(255, 255, 255, 0.3)
```

**Accent Pink**:
```scss
Background:   #ec4899
Box Shadow:   0 4px 15px rgba(236, 72, 153, 0.3)
```

**Hover**: 
- Scale down 1-2px
- Enhanced shadow
- Darker shade

---

### 3️⃣ Navigation Pill

**Desktop Position**:
- Fixed bottom-right
- 32px from edges
- Shows icons only

**Mobile Position**:
- Fixed top-right (compact)
- 16px from edges
- Shows text labels

**Styling**:
```scss
Background:       rgba(255, 255, 255, 0.15)
Backdrop Filter:  blur(25px)
Border:           1px solid rgba(255, 255, 255, 0.3)
Padding:          0.5rem (inner spacing)
Border Radius:    999px (full pill)
Z-Index:          999
Box Shadow:       0 8px 32px rgba(0, 0, 0, 0.1)
```

---

### 4️⃣ Skill Pill Badge

**Properties**:
```scss
Background:      rgba(255, 255, 255, 0.15)
Text:            #1d1d1f
Padding:         0.5rem 1rem
Border Radius:   999px (full pill)
Border:          1px solid rgba(255, 255, 255, 0.3)
Font Size:       14px
Font Weight:     500
```

**Hover**:
```scss
Background:     rgba(255, 255, 255, 0.25)
Color:          #0ea5e9 (blue highlight)
Transform:      translateY(-2px)
Box Shadow:     0 6px 25px rgba(14, 165, 233, 0.15)
```

---

### 5️⃣ Timeline Component

**Connector Line**:
```scss
Position:      Absolute (vertical)
Width:         2px
Height:        Full (top to bottom)
Background:    Linear gradient blue → pink
Left Position: 50% (desktop), 0 (mobile)
```

**Timeline Dot**:
```scss
Width/Height:   16px
Background:     white
Border:         3px solid #0ea5e9
Border Radius:  50% (circle)
Z-Index:        2
Position:       Absolute
```

**Timeline Card**:
- Extends `.glass-card`
- Text-align: right (odd), left (even)
- Desktop: alternating left/right layout
- Mobile: stacked single column

---

### 6️⃣ Featured Project Card

**Structure**:
```
┌─────────────────────┐
│  Project Image      │  (240px height, gradient bg)
├─────────────────────┤
│  Project Title      │  (24px, 600 weight)
│  Metadata Badges    │  (skill tags, language)
│  Description        │  (14px, muted text)
│  [Action Button]    │  (CTA button)
└─────────────────────┘
```

**Responsive**:
- Desktop: 2-column grid
- Mobile: 1 column, full-width

---

### 7️⃣ Archive Card (Small)

**Properties**:
```scss
Padding:        1.5rem (more compact)
Icon Position:  Top-left
Layout:         Vertical stack
Content:        Name + Description + Stats
```

**Grid**:
- Desktop: 3 columns (auto-fit)
- Tablet: 2 columns
- Mobile: 1 column

---

## Responsive Breakpoints

```scss
// Mobile-first approach
Mobile:   ≤ 768px   (Single column)
Tablet:   769-1023px (Flexible 2-column)
Desktop:  ≥ 1024px  (Full 2+ column)
```

### Layout Changes
| Component | Mobile | Tablet | Desktop |
|-----------|--------|--------|---------|
| Hero | Column | Column | Row (side-by-side) |
| Featured Grid | 1 col | 1-2 col | 2 col |
| Archive Grid | 1 col | 2 col | 3 col |
| Timeline | Single | Single | Alternating |
| Nav Pill | Top-right | Bottom-right | Bottom-right |

---

## Animation & Transitions

### Transition Speeds
```scss
--transition-fast: 0.15s ease   (Quick feedback)
--transition-base: 0.3s ease    (Standard animations)
--transition-slow: 0.5s ease    (Entrance/exit)
```

### Hover Effects
```scss
// Card Lift
Transform: translateY(-4px)
Box Shadow: Enhanced
Duration:  0.3s ease

// Button Feedback
Transform: translateY(-2px)
Duration:  0.15s ease

// Text Links
Color Change: #0ea5e9 → #ec4899
Text Decoration: Add underline
Duration:  0.15s ease
```

### Entrance Animations (Optional)
```scss
// Fade In
Opacity: 0 → 1
Duration: 0.5s ease

// Slide Up
Transform: translateY(20px) → translateY(0)
Opacity: 0 → 1
Duration: 0.5s ease-out
```

---

## Accessibility Guidelines

### Color Contrast
```
Text on Glass:   #1d1d1f on rgba(255,255,255,0.15)
                 ✓ WCAG AA Compliant (4.5:1)
```

### Focus States
```scss
.glass-nav-pill a:focus {
    outline: 2px solid #0ea5e9;
    outline-offset: 2px;
}
```

### ARIA Labels
```html
<a href="/" aria-label="Home">
    <i class="fas fa-home"></i>
</a>
```

### Semantic HTML
- Use `<h1>`, `<h2>`, etc. (not `<div>` styled as heading)
- Use `<button>` for actions
- Use `<nav>` for navigation
- Use `<section>` for content groups

---

## Dark Mode (Optional)

### Color Adjustments
```scss
// Light Mode (current)
--text-dark: #1d1d1f;
--bg-gradient: Light colors;

// Dark Mode
--text-dark: #f3f4f6;
--bg-gradient: Dark colors;
--glass-light: rgba(255, 255, 255, 0.05);
```

### Implementation
```scss
@media (prefers-color-scheme: dark) {
    :root {
        // Override variables
    }
}
```

---

## Image Usage Guidelines

### Featured Project Images
- **Dimensions**: 600×400px (3:2 ratio)
- **Format**: WebP (with PNG fallback)
- **File Size**: < 100KB (optimized)
- **Style**: Flat design, soft edges

### Avatar Images
- **Dimensions**: 200×200px (square)
- **Format**: PNG (transparent bg recommended)
- **Style**: Professional headshot or icon

### Screenshot Images
- **Dimensions**: 1200×800px minimum
- **Format**: PNG or WebP
- **Content**: Clear, well-lit screenshots

---

## Code Examples

### Creating a New Glass Card
```html
<div class="glass-card">
    <h3>Your Title</h3>
    <p>Your content here...</p>
</div>
```

### Adding a Skill Pill
```html
<span class="skill-pill">
    <i class="fas fa-code"></i> Python
</span>
```

### Creating a CTA Button
```html
<a href="#target" class="cta-button">
    <i class="fas fa-arrow-right"></i> Learn More
</a>
```

### Primary vs Secondary Button
```html
<!-- Primary (Blue) -->
<button class="cta-button">Primary Action</button>

<!-- Secondary (Glass) -->
<button class="cta-button secondary">Secondary Action</button>

<!-- Accent Pink -->
<button class="cta-button accent-pink">Special Action</button>
```

---

## Usage Checklist

- [ ] All text uses Inter font
- [ ] Heading hierarchy maintained (h1 > h2 > h3)
- [ ] Color contrast ≥ 4.5:1 for accessibility
- [ ] Spacing follows 8px/16px grid
- [ ] Cards have consistent border radius
- [ ] Hover states on all interactive elements
- [ ] Mobile responsive ≤768px
- [ ] Max width 900-1200px for content
- [ ] Buttons use semantic `<button>` or `<a>`
- [ ] Icons from FontAwesome 6.4+
- [ ] No hardcoded colors (use variables)

---

## Modification Quick Reference

### To Change Primary Color Theme:
```scss
// In assets/css/style.scss, line 25
--accent-blue: #YOUR_NEW_COLOR;  // Changes all blues
```

### To Add Rounded Edges:
```scss
// Line 42
--radius-lg: 40px;  // More rounded
```

### To Increase Blur Effect:
```scss
// Line 223 (glass-card)
backdrop-filter: blur(30px);  // More blur (or 15px less)
```

### To Speed Up Animations:
```scss
// Line 45
--transition-base: 0.15s ease;  // Faster (was 0.3s)
```

---

**This design system ensures consistency, accessibility, and modern aesthetics across your portfolio.**

*Version 1.0 | February 2026*
