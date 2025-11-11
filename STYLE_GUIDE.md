# 🎨 Project Aegis - Visual Style Guide

## Brand Identity

### Company Name
**Aegion** - Developer of advanced AI

### Product Name
**Project Aegis** - Self-learning AI with absolute privacy

### Tagline
*"Absolute Privacy. Advanced AI."*

### Motto
*"Engineered for excellence. Designed for privacy."*

---

## 🎨 Color System

### Primary Palette

#### Gold (#d4af37)
- **Usage**: Primary buttons, main headings, feature icons
- **Personality**: Premium, professional, trustworthy
- **Hex**: `#d4af37`
- **RGB**: `rgb(212, 175, 55)`
- **Light Variant**: `#e8c547`

#### Cyan (#00d9ff)
- **Usage**: Secondary accents, hover states, glows
- **Personality**: Modern, tech-forward, fresh
- **Hex**: `#00d9ff`
- **RGB**: `rgb(0, 217, 255)`
- **Light Variant**: `#4ff0ff`

### Background Palette

#### Dark Navy (#0a0e27)
- **Usage**: Main background
- **Purpose**: Professional, reduces eye strain
- **Hex**: `#0a0e27`
- **RGB**: `rgb(10, 14, 39)`

#### Dark Secondary (#1a1f3a)
- **Usage**: Cards, secondary backgrounds
- **Hex**: `#1a1f3a`

#### Dark Tertiary (#252d45)
- **Usage**: Deepest backgrounds, overlays
- **Hex**: `#252d45`

### Text Palette

#### Primary Text (#e8e8e8)
- **Usage**: Body text, main content
- **Hex**: `#e8e8e8`
- **Best on**: Dark backgrounds

#### Secondary Text (#b0b0b0)
- **Usage**: Descriptions, less important info
- **Hex**: `#b0b0b0`
- **Best on**: Dark backgrounds

---

## 🔤 Typography

### Font Family
**Primary**: "Segoe UI", "Fira Sans", sans-serif

### Font Sizes

| Element | Size | Weight | Usage |
|---------|------|--------|-------|
| H1 (Hero) | 4rem | 700 | Page titles |
| H2 (Section) | 2.2rem | 600 | Section headers |
| H3 (Card) | 1.4rem | 600 | Feature titles |
| H4 (Subtitle) | 1.1rem | 500 | Subsections |
| Body | 1.1rem | 400 | Main text |
| Small | 0.9rem | 400 | Secondary text |

---

## ✨ Visual Effects

### Shadows

#### Subtle Shadow
```css
box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
```

#### Gold Shadow
```css
box-shadow: 0 4px 15px rgba(212, 175, 55, 0.3);
```

#### Cyan Shadow
```css
box-shadow: 0 10px 25px rgba(0, 217, 255, 0.15);
```

#### Deep Shadow
```css
box-shadow: 0 20px 40px rgba(0, 217, 255, 0.2), 
            0 0 20px rgba(212, 175, 55, 0.1);
```

### Gradients

#### Gold to Cyan
```css
background: linear-gradient(135deg, var(--gold) 0%, var(--cyan) 100%);
```

#### Dark Background
```css
background: linear-gradient(135deg, var(--dark-bg) 0%, #0f1433 100%);
```

#### Gold Overlay
```css
background: linear-gradient(135deg, rgba(212, 175, 55, 0.05) 0%, 
                                    rgba(212, 175, 55, 0.02) 100%);
```

#### Cyan Overlay
```css
background: linear-gradient(135deg, rgba(0, 217, 255, 0.05) 0%, 
                                    rgba(0, 217, 255, 0.02) 100%);
```

### Glassmorphism

#### Blurred Background
```css
background: rgba(10, 14, 39, 0.95);
backdrop-filter: blur(10px);
border: 1px solid rgba(0, 217, 255, 0.2);
```

---

## 🎯 Component Styles

### Button - Primary
- **Background**: Gold gradient
- **Color**: Dark text
- **Padding**: 0.9rem 2.5rem
- **Border**: None
- **Border-radius**: 8px
- **Hover**: Scale up, enhanced shadow
- **Transition**: 0.3s cubic-bezier

### Button - Secondary
- **Background**: Transparent cyan
- **Color**: Cyan text
- **Border**: 2px solid cyan
- **Padding**: 0.9rem 2.5rem
- **Border-radius**: 8px
- **Hover**: Brightness increase
- **Transition**: 0.3s smooth

### Feature Card
- **Background**: Dark secondary gradient
- **Border**: 1px solid gold (0.3 opacity)
- **Border-radius**: 12px
- **Padding**: 2.5rem
- **Hover**: Lift + cyan border + glow shadow
- **Transition**: 0.4s cubic-bezier

### Navigation Link
- **Color**: Light gray
- **Padding**: 0.75rem 1.5rem
- **Border-radius**: 8px
- **Background**: Gold (0.1 opacity)
- **Hover**: Cyan color + border + translate up
- **Underline**: Animated gradient line
- **Transition**: 0.3s ease

---

## 🎬 Animations

### Fade In Down
```css
@keyframes fadeInDown {
    from { opacity: 0; transform: translateY(-30px); }
    to { opacity: 1; transform: translateY(0); }
}
Duration: 0.8s
Easing: ease
```

### Fade In Up
```css
@keyframes fadeInUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
}
Duration: 0.8s
Easing: ease
```

### Slide In Right
```css
@keyframes slideInRight {
    from { opacity: 0; transform: translateX(50px); }
    to { opacity: 1; transform: translateX(0); }
}
Duration: 0.6s
Easing: ease
```

### Glow
```css
@keyframes glow {
    0%, 100% { text-shadow: 0 0 10px rgba(0, 217, 255, 0.5), 
                            0 0 20px rgba(212, 175, 55, 0.3); }
    50% { text-shadow: 0 0 20px rgba(0, 217, 255, 0.8), 
                       0 0 30px rgba(212, 175, 55, 0.5); }
}
Duration: 3s
Easing: ease-in-out
Repeat: infinite
```

---

## 📏 Spacing System

### Padding
- **Small**: 1rem
- **Medium**: 1.5rem
- **Large**: 2rem
- **XLarge**: 2.5rem
- **Card**: 2.5rem
- **Section**: 3rem
- **Hero**: 6rem

### Margin
- **Gap between cards**: 2rem
- **Section gap**: 4rem
- **Element gap**: 1rem
- **Feature gap**: 1.5rem

### Border Radius
- **Buttons**: 8px
- **Cards**: 12px
- **Sections**: 15px
- **Scrollbar**: 5px

---

## 🔍 Component States

### Button States
- **Default**: Gold gradient, subtle shadow
- **Hover**: Elevated, enhanced glow, slight scale
- **Active**: Brighter gold, stronger shadow
- **Disabled**: Reduced opacity, no hover

### Link States
- **Default**: Light gray, subtle background
- **Hover**: Cyan color, border highlight, translate up
- **Active**: Gold color, gold border
- **Visited**: Same as default (no change)

### Card States
- **Default**: Border visible, subtle glow
- **Hover**: Lifted up, cyan border, strong glow
- **Focus**: Cyan outline

---

## 🌐 Responsive Design

### Breakpoints

#### Desktop (1024px+)
- Full menu display
- Grid layouts optimal
- Large typography
- All effects enabled

#### Tablet (768px - 1024px)
- Adjusted padding
- Responsive grid
- Readable fonts
- Hover effects work

#### Mobile (<768px)
- Vertical navigation
- Single column layout
- Touch-friendly sizes
- Optimized animations

#### Small Mobile (<480px)
- Compact navigation
- Extra padding reduction
- Smaller fonts
- Simplified layout

---

## 🎨 Visual Hierarchy

### Level 1 - Most Important
- Gold text on dark background
- Large hero titles
- Primary buttons
- Feature icons

### Level 2 - Secondary
- Cyan accents
- Section headings
- Secondary buttons
- Card titles

### Level 3 - Tertiary
- Light gray text
- Body content
- Secondary descriptions

### Level 4 - Minimal
- Medium gray text
- Tertiary information
- Footnotes

---

## ✅ Accessibility

### Color Contrast
- Gold on Dark: **6.9:1** ✓ (AA compliant)
- Cyan on Dark: **8.2:1** ✓ (AA compliant)
- Text on Dark: **11.3:1** ✓ (AAA compliant)

### Touch Targets
- Minimum: 44px × 44px
- Button padding: 0.9rem (14px) minimum
- Link spacing: 1rem gap

### Focus States
- Visible focus indicators
- Clear hover states
- Keyboard navigation support

---

## 📱 Print Styles

### Print Layout
- Hide header and footer
- Black text on white background
- Remove background gradients
- Simple link styling
- Full width layout

---

## 🎯 Design Principles

1. **Dark & Professional** - Premium feel, easy on eyes
2. **Gold & Cyan** - Consistency throughout
3. **Smooth Motion** - Fluid 0.3-0.4s transitions
4. **Responsive** - Works on all devices
5. **Accessible** - High contrast, readable text
6. **Semantic** - Proper HTML structure
7. **Performant** - Optimized animations
8. **Modern** - Current CSS techniques

---

## 🎨 Icon System

All icons are emoji (Unicode):
- 🔐 Privacy/Security
- 🧠 AI/Learning
- ⚡ Power
- 🎯 Focus
- 🔄 Process
- 📊 Analytics
- 🔗 Connection
- 🎨 Design
- 📈 Growth
- 🚀 Launch
- 💡 Innovation
- 🌍 Global
- 🏆 Achievement
- 🤝 Partnership

---

## 💾 File Reference

### CSS Variables (in style1.css)
```css
--dark-bg: #0a0e27
--dark-secondary: #1a1f3a
--dark-tertiary: #252d45
--gold: #d4af37
--gold-light: #e8c547
--cyan: #00d9ff
--cyan-light: #4ff0ff
--text-primary: #e8e8e8
--text-secondary: #b0b0b0
--font-sans: 1.1rem "Segoe UI", "Fira Sans", sans-serif
--font-heading: "Segoe UI", "Fira Sans", sans-serif
```

---

## 🎉 Summary

This style guide ensures:
- ✅ Consistent visual identity
- ✅ Professional appearance
- ✅ Smooth user experience
- ✅ Accessible design
- ✅ Modern aesthetics
- ✅ Brand alignment

**All components follow these standards.**

---

*Project Aegis - Engineered for excellence. Designed for privacy.*
