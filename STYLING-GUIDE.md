# Styling Customization Guide

Your website comes with a modern, polished design that includes:

## 🎨 Design Features

### Color Scheme
- Modern gradient accents
- Automatic dark mode support (based on system preferences)
- Customizable color palette via CSS variables

### Typography
- Professional font stack
- Optimized for readability
- Responsive font sizes
- Custom heading styles with gradient underlines

### Components
- Smooth hover animations
- Elevated card designs with 3D effects
- Gradient borders on post cards
- Animated navigation links
- Professional footer with social links

### Advanced Features
- Smooth page transitions
- Skeleton loading states
- Reading progress indicator
- Back-to-top button
- Print-friendly styles
- Full accessibility support

## 🎯 Quick Customization

### Change Primary Colors

Edit `themes/personal/static/css/style.css`:

```css
:root {
    --primary-color: #3b82f6;      /* Main brand color - Change this! */
    --primary-dark: #2563eb;       /* Darker shade */
    --primary-light: #60a5fa;      /* Lighter shade */
    --accent-color: #8b5cf6;       /* Secondary accent color */
}
```

**Popular color schemes:**

**Professional Blue (default)**
```css
--primary-color: #3b82f6;
--accent-color: #8b5cf6;
```

**Tech Green**
```css
--primary-color: #10b981;
--accent-color: #06b6d4;
```

**Creative Purple**
```css
--primary-color: #8b5cf6;
--accent-color: #ec4899;
```

**Bold Red**
```css
--primary-color: #ef4444;
--accent-color: #f59e0b;
```

**Ocean Teal**
```css
--primary-color: #14b8a6;
--accent-color: #0ea5e9;
```

### Customize Typography

Change the font family:

```css
body {
    font-family: 'Your Font', -apple-system, BlinkMacSystemFont, sans-serif;
}
```

**Using Google Fonts:**

1. Add to `themes/personal/layouts/_default/baseof.html` in `<head>`:
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
```

2. Update CSS:
```css
body {
    font-family: 'Inter', sans-serif;
}
```

**Recommended fonts:**
- **Modern**: Inter, Poppins, DM Sans
- **Classic**: Merriweather, Lora, Crimson Text
- **Tech**: Fira Code, JetBrains Mono, Space Mono
- **Minimal**: Work Sans, Nunito, Karla

### Adjust Spacing

```css
:root {
    --max-width: 900px;  /* Content width */
}

main {
    padding: 3rem 2rem;  /* Vertical and horizontal padding */
}
```

### Change Border Radius

```css
:root {
    --radius-sm: 6px;   /* Small elements */
    --radius-md: 8px;   /* Medium elements */
    --radius-lg: 12px;  /* Large elements */
}
```

For sharper design, use smaller values:
```css
--radius-sm: 3px;
--radius-md: 4px;
--radius-lg: 6px;
```

For rounder design:
```css
--radius-sm: 8px;
--radius-md: 12px;
--radius-lg: 16px;
```

### Disable Dark Mode

Remove or comment out the dark mode section in `style.css`:

```css
/* @media (prefers-color-scheme: dark) {
    ... entire dark mode block ...
} */
```

### Enable Force Dark Mode

Add this at the top of `style.css`:

```css
:root {
    color-scheme: dark;
}
```

## 🎭 Advanced Customization

### Add Custom Gradient Backgrounds

```css
.hero {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
}
```

### Add Particle Background

1. Add to `baseof.html` before `</body>`:
```html
<script src="https://cdn.jsdelivr.net/particles.js/2.0.0/particles.min.js"></script>
<div id="particles-js"></div>
```

2. Add CSS:
```css
#particles-js {
    position: fixed;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    z-index: -1;
}
```

### Custom Post Card Styles

Make cards more prominent:

```css
.post-card {
    background: white;
    box-shadow: 0 10px 30px rgba(0,0,0,0.1);
}

.post-card:hover {
    box-shadow: 0 20px 40px rgba(0,0,0,0.15);
    transform: translateY(-8px);
}
```

### Add Image Effects

```css
.content img {
    filter: grayscale(20%);
    transition: filter 0.3s;
}

.content img:hover {
    filter: grayscale(0%);
}
```

## 📱 Mobile Customization

Adjust mobile breakpoints in `style.css`:

```css
@media (max-width: 768px) {
    /* Tablet styles */
}

@media (max-width: 480px) {
    /* Mobile styles */
}
```

## 🎪 Animation Customization

### Disable Animations

Add to `style.css`:

```css
*, *::before, *::after {
    animation-duration: 0s !important;
    transition-duration: 0s !important;
}
```

### Add Custom Animations

```css
@keyframes slideIn {
    from {
        opacity: 0;
        transform: translateX(-20px);
    }
    to {
        opacity: 1;
        transform: translateX(0);
    }
}

.post-card {
    animation: slideIn 0.5s ease;
}
```

## 🔧 Component Customization

### Navigation Style

**Centered navigation:**
```css
.nav-container {
    justify-content: center;
    flex-direction: column;
}
```

**Transparent header:**
```css
header {
    background-color: transparent;
    border-bottom: none;
}
```

### Footer Style

**Minimal footer:**
```css
footer {
    background: transparent;
    border-top: 1px solid var(--border-color);
    padding: 2rem 0;
}
```

**Social icons only:**
```css
.footer-container p {
    display: none;
}
```

## 🎨 Pre-made Themes

You can copy entire theme sections from `enhancements.css` and customize them!

## 📝 Best Practices

1. **Make changes incrementally** - Test each change before moving to the next
2. **Use browser DevTools** - Experiment with styles in real-time
3. **Keep backups** - Git commit before major style changes
4. **Test responsiveness** - Check mobile, tablet, and desktop views
5. **Validate colors** - Use contrast checkers for accessibility
6. **Test dark mode** - If you keep it enabled

## 🆘 Troubleshooting

**Styles not applying?**
- Clear browser cache (Ctrl+Shift+R / Cmd+Shift+R)
- Check file paths are correct
- Ensure CSS file is saved

**Colors look different?**
- Check if dark mode is interfering
- Verify color format (use hex #000000 or rgb())

**Layout broken on mobile?**
- Check media query breakpoints
- Test with browser responsive mode

## 🚀 Resources

- [Color Palette Generator](https://coolors.co)
- [Google Fonts](https://fonts.google.com)
- [CSS Gradient Generator](https://cssgradient.io)
- [Box Shadow Generator](https://shadows.brumm.af)

---

Remember: The best design is one that reflects your personal style while maintaining readability and usability!
