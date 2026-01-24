# Welcome to Cancun

A fully responsive, accessible, and SEO-optimized travel website showcasing Cancun, Mexico, and popular tourist destinations in the Riviera Maya region.

## 🌟 Project Overview

This website was created as part of the SheCodes Responsive Add-on course to develop modern web development skills with a focus on accessibility, performance, and mobile-first responsive design. The project demonstrates production-ready code using vanilla HTML and CSS.

**Live Site:** https://meek-granita-bd67b6.netlify.app/

## 📚 Learning Objectives

- ✅ Master mobile-first responsive design principles
- ✅ Create accessible, semantic HTML5 structure
- ✅ Implement CSS Grid and Flexbox for modern layouts
- ✅ Optimize for multiple screen sizes and devices
- ✅ Achieve high Lighthouse performance scores
- ✅Implement SEO best practices with structured data
- ✅ Follow web accessibility (WCAG) guidelines

## 🛠 Technologies Used

- **HTML5** - Semantic markup with ARIA attributes
- **CSS3** - Modern CSS with Grid, Flexbox, and Custom Properties (CSS Variables)
- **Google Fonts** - Poppins font family with optimized loading
- **Google Maps Embed API** - Interactive location maps
- **YouTube Embed API** - Video content integration
- **PWA Features** - Web app manifest for installability
- **Structured Data** - JSON-LD schema markup for SEO

## ✨ Key Features

**Accessibility (WCAG 2.1 AA Compliant)**

- Skip-to-content link for keyboard navigation
- Proper ARIA labels and semantic HTML
- Full keyboard navigation support
- Screen reader optimized content
- High contrast focus indicators

**Performance Optimization**

- DNS prefetch and preconnect for external resources
- Lazy loading for images and iframes
- Fetchpriority hints for critical resources
- Image dimensions specified to prevent layout shift
- Async decoding for non-blocking rendering

**Responsive Design**

- **Mobile-First:** Base styles for 320px+ devices
- **Tablet:** Enhanced layouts from 768px
- **Desktop:** Full-featured experience from 1024px
- **Large Screens:** Optimized for 1200px+ and 1600px+
- Fluid typography and spacing using CSS custom properties

**SEO Features**

- Complete meta tag implementation (Open Graph, Twitter Cards)
- Canonical URLs
- Structured data (Schema.org JSON-LD)
- Semantic HTML for better indexing
- Descriptive alt text for all images

## 📊 Lighthouse Scores

**Desktop Device**

- **Performance:** 100/100 ✅
- **Accessibility:** 100/100 ✅
- **Best Practices:** 77/100 ⚠️
- **SEO:** 100/100 ✅

**Mobile Device**

- **Performance:** 93/100 ✅
- **Accessibility:** 100/100 ✅
- **Best Practices:** 73/100 ⚠️
- **SEO:** 100/100 ✅

### 📌 Note on Best Practices Score

The Best Practices score is impacted by third-party cookies from embedded Google Maps and YouTube iframes. These are necessary for interactive functionality:<br>
**Google Maps:** Interactive features (zoom, pan, street view, directions)<br>
**YouTube:** Video playback controls and recommendations

**Alternative solutions considered:**

- ❌ Static map images (removes essential interactivity)
- ⚠️ Lazy-loading on user interaction (adds UX friction)
- ⚠️Custom mapping solution (beyond project scope and budget)<br>

**Decision:** Prioritized user experience and functionality over achieving a perfect Lighthouse score — a real-world trade-off common in production environments.

## 🎨 Design Approach

### Mobile-First Development

The website follows a **progressive enhancement** strategy:

**1. Base Layer (Mobile)** - Core functionality for smallest screens (320px+)
**2. Enhancement Layers** - Additional features unlock at larger breakpoints
**3. Performance First** - Critical CSS inline, non-essential styles deferred
**4. Accessibility Always** - Works without CSS/JavaScript

### Responsive Breakpoints

```css
/* Mobile: Base styles (320px - 767px) */
/* All devices get these styles first */

/* Tablet: Enhanced layout */
@media (min-width: 768px) {
  /* 2-column grids, larger typography */
}

/* Intermediate: Gallery optimization */
@media (min-width: 900px) {
  /* 4-column photo grid */
}

/* Desktop: Full experience */
@media (min-width: 1024px) {
  /* 3-column cards, decorative elements */
}

/* Large Desktop: Maximum width constraint */
@media (min-width: 1200px) {
  /* Container max-width, increased spacing */
}

/* Extra Large: Premium spacing */
@media (min-width: 1600px) {
  /* Enhanced padding and margins */
}
```

### CSS Architecture

**Custom Properties (CSS Variables)**

- Centralized design tokens for colors, spacing, and typography
- Easy theme modifications and maintenance
- Improved consistency across breakpoints

**Grid-First Approach**

- CSS Grid for page-level layouts
- Flexbox for component-level alignment
- auto-fit and minmax() for flexible galleries

**Card Component System**

Cards use a 3-row grid to ensure consistent alignment:

```css
.card {
  display: grid;
  grid-template-rows: auto 1fr auto;
  /* 
    auto  = header (image + map) - natural height
    1fr   = body (content) - flexible, fills space
    auto  = footer (button) - natural height
  */
}
```

**Benefits**

- ✅ All card images align perfectly
- ✅ Variable content doesn't break layout
- ✅ Buttons always aligned at bottom
- ✅ Cards maintain equal heights in grid

## 📁 Project Structure

```
cancun-travel-website/
├── index.html                          # Main HTML file
├── README.md                           # Project documentation
├── src/
│   ├── styles.css                      # All CSS styles
│   └── manifest.json                   # PWA manifest
├── images/                             # Image assets
│   ├── cancun_background.jpg           # Hero background
│   ├── tropical-paradise.jpg           # Why Cancun section
│   ├── xcaret-park.jpg                 # Card image
│   ├── chichen-itza.jpg                # Card image
│   ├── rio-secreto.jpg                 # Card image
│   ├── cancun-food.jpg                 # Gallery photo
│   ├── cancun-celebrations.jpg         # Gallery photo
│   ├── cancun-street-scene.jpg         # Gallery photo
│   ├── sea-turtle-aumal.jpg            # Gallery photo
│   ├── cenote-ik-kil.jpg               # Gallery photo
│   ├── musa_underwater_museum.jpg      # Gallery photo
│   ├── Cancun-sea-hotels.jpg           # Gallery photo
│   ├── cancun-colorful-pottery.jpg     # Gallery photo
│   ├── puerto-morelos-catamaran.jpg    # Gallery photo
│   ├── mesoamerican-barrier-reef.jpg   # Gallery photo
│   ├── cancun-dusk.jpg                 # Gallery photo
│   ├── cancun-beach-scene.jpg          # Gallery photo
│   └── Cancun_logo-transparent.jpg     # Footer background
├── favicon-32x32.png                   # Favicon 32x32
└── favicon-16x16.png                   # Favicon 16x16
```

## 🚀 How to View

**Option 1: Direct File Access**

1. Clone or download this repository
2. Open index.html directly in your web browser
3. Works offline (except for embedded maps and videos)

**Option 2: Live Server (Recommended for Development)**

1. Install VS Code
2. Install "Live Server" extension by Ritwick Dey
3. Right-click on index.html
4. Select "Open with Live Server"
5. Site opens at http://localhost:5500

**Option 3: View Live Deployment**

Visit: https://meek-granita-bd67b6.netlify.app/

## 💡 Key Learning Takeaways

### 1. Mobile-First is More Intuitive

Starting with mobile constraints forces you to prioritize content and functionality. Adding complexity for larger screens is easier than stripping it away.

### 2. CSS Grid Solves Real Problems

The `grid-template-rows: auto 1fr auto` pattern elegantly solves the card alignment issue that previously required JavaScript hacks or complex flexbox.

### 3. CSS Customer Properties Are Game Changers

Centralized design tokens made responsive design easier. Changing one variable updates across all breakpoints.

### 4. Semantic HTML Improves Everything

Proper structure `(<header>, <main>, <section>, <nav>, <footer>)` helped with:

- SEO rankings
- Screen reader navigation
- Code maintainability
- Browser reader modes

### 5. Performance ≠ Perfection

Real-world sites integrate third-party services. Perfect Lighthouse scores aren't always achievable (or necessary) when user experience depends on features like interactive maps.

### 6. Accessibility is Non-Negotiable

Features like skip links and ARIA labels cost minimal effort but make the site usable for everyone. It's not optional — it's professional responsibility.

## 🔧 Browser Compatibility

Tested and working on:

- ✅ Chrome 120+ (Desktop & Mobile)
- ✅ Firefox 121+ (Desktop & Mobile)
- ✅ Safari 17+ (Desktop & Mobile)
- ✅ Edge 120+ (Desktop)
- ✅ Samsung Internet 23+

### Known issues

- IE11: Not supported (uses CSS Grid and Custom Properties)
- Older iOS Safari (<12): May have layout issues

## 📈 Future Enhancements

### Phase 1: Interactivity

[ ] Add lightbox gallery for photo expansion<br>
[ ] Implement smooth scroll behavior<br>
[ ] Add cookie consent banner for GDPR/CCPA<br>
[ ] Create interactive "Plan Your Trip" form<br>

### Phase 2: Content Expansion

[ ] Add more destinations (Tulum, Playa del Carmen, Cozumel)<br>
[ ] Create dedicated pages for activities (diving, food tours)<br>
[ ] Add traveler reviews/testimonials section<br>
[ ] Integrate weather widget<br>

### Phase 3: Advanced Features

[ ] Implement dark mode toggle<br>
[ ] Add language switcher (English/Spanish)<br>
[ ] Create blog section for travel tips<br>
[ ] Add booking integration for tours/hotels<br>
[ ] Implement search functionality<br>

### Phase 4: Performance & PWA

[ ] Convert to full Progressive Web App<br>
[ ] Add service worker for offline functionality<br>
[ ] Implement WebP images with fallbacks<br>
[ ] Add critical CSS inlining<br>
[ ] Create app icons for all sizes<br>

## 👤 Author

**Caroline Hargreaves**
Aspiring Web Developer | SheCodes Student

- [GitHub Profile](https://github.com/carolinehargreaves41-sketch)

## 📜 License

This project is open source and available under the MIT License. Feel free to use it for educational purposes.

### Usage Terms

- ✅ Use for learning and education
- ✅ Fork and modify for your own projects
- ✅ Use as portfolio piece (with credit)
- ❌ Do not claim as your own work
- ❌ Do not use commercially without permission

## 🙏 Acknowledgments

- **SheCodes** - For the comprehensive Responsive Web Design course
- **Matt Delac** - Founder of SheCodes and excellent instructor
- **Google Fonts** - For the Poppins typeface
- **Google Maps Platform** - For the embed API and mapping services
- **Netlify** - For seamless deployment and hosting
- **Lighthouse** - For performance auditing and optimization guidance
- **MDN Web Docs** - For excellent HTML/CSS reference documentation

## 📚 Resources Used

- [CSS-Tricks Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [MDN Web Accessibility](https://developer.mozilla.org/en-US/docs/Web/Accessibility)
- [Web.dev Performance](https://web.dev/performance/)
- [Schema.org Documentation](https://schema.org/)
- [WCAG 2.1 Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)

---

**Project Status:** ✅ Completed - January 2026<br>
**Version:** 1.0.0<br>
**Last Updated:** 24 January 2026<br>

_Built with 💜 and lots of 🫖 in England, UK_
