# Kloodi Labs Website

Professional static website for Kloodi Labs software company.

## Structure

```
kloodi-labs-website/
├── index.html          # Etusivu (Homepage)
├── referenssit.html    # Referenssit (References)
├── yhteystiedot.html   # Yhteystiedot (Contact)
├── styles.css          # Complete design system
├── script.js           # Interactivity (menu, forms)
└── README.md           # Documentation
```

## Design System

### Colors
- **Primary (Claw Red)**: `#C61D23` — Used sparingly as accent only
- **Primary Dark**: `#8E1419` — Hover states
- **Neutral Black**: `#0F1720` — Primary text
- **Neutral Gray**: `#6B7280` — Secondary text, UI elements
- **Neutral Light**: `#E5E7EB` — Borders, cards
- **Background**: `#FAFAFA` — Page background

### Typography
- **Primary Font**: Inter (400, 500, 600, 700)
- **Brand Font**: Space Grotesk (headings only)
- **H1**: 40px / 700 weight
- **H2**: 32px / 600 weight
- **H3**: 24px / 600 weight
- **Body**: 16px / 400 weight
- **Line Height**: 1.4-1.6

### Spacing
8-point grid system: 4px, 8px, 16px, 24px, 32px, 48px, 64px

### Components
- **Buttons**: 8px border-radius, smooth transitions
- **Cards**: 12px border-radius, subtle borders
- **Inputs**: Focus state with red accent
- **Icons**: Lucide icons (CDN), 1.5-2px stroke

### Brand Guidelines
- Minimal, precise, technical aesthetic
- Red color used sparingly for impact
- Generous whitespace
- Functional animations only (120-180ms)
- WCAG AA contrast compliance

## Features

### Navigation
- Sticky header
- Mobile-responsive hamburger menu
- Active page highlighting

### Pages

**Etusivu (Homepage)**
- Hero section with value proposition
- 4 service cards (development, consulting, DevOps, AI)
- About section
- Call-to-action
- Footer with navigation

**Referenssit (References)**
- Grid of 6 project case studies
- Tech stack tags for each project
- Industry categorization
- Hover effects on cards

**Yhteystiedot (Contact)**
- Contact form with validation
- Company information sidebar
- Map placeholder
- Contact details (email, phone, address)

### Mobile Responsive
- Breakpoint: 768px
- Hamburger menu for mobile
- Single-column layouts on small screens
- Touch-friendly tap targets

## Technical Details

### Browser Support
- Modern browsers (Chrome, Firefox, Safari, Edge)
- ES6+ JavaScript
- CSS Grid and Flexbox

### Performance
- No framework overhead (vanilla HTML/CSS/JS)
- Google Fonts with preconnect
- Minimal external dependencies
- Inline SVG logo for fast loading

### SEO
- Semantic HTML5
- Meta descriptions
- Open Graph tags
- Finnish language content

## Deployment

### Local Development
1. Open `index.html` in a browser
2. Or use a local server:
   ```bash
   python3 -m http.server 8000
   # or
   npx serve .
   ```

### Production
- Upload all files to web server
- Ensure proper MIME types
- Configure CDN if needed
- Add SSL certificate

### Customization
1. **Colors**: Edit CSS variables in `styles.css` `:root` selector
2. **Content**: Modify HTML files directly
3. **Logo**: Replace SVG in navigation
4. **Contact Form**: Implement backend in `script.js` `handleSubmit()`

## Contact Form Integration

The contact form currently shows a browser alert. To integrate with a backend:

1. Add form action endpoint in `script.js`
2. Use fetch API or form service (Formspree, Netlify Forms, etc.)
3. Implement server-side validation
4. Add CAPTCHA if needed

Example with fetch:
```javascript
fetch('/api/contact', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify(data)
})
```

## License
All rights reserved © 2026 Kloodi Labs
