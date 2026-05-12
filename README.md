# Sadman Mazumder — Personal Portfolio

Personal portfolio website of Sadman Mazumder — Software Developer, AI/ML Engineer, and Game Developer. An artist at heart, the site is crafted with an aesthetic and interactive canvas effects reflective of who I am and my experience.

**Live site:** deployed on [Vercel](https://vercel.com)

---

## Pages

| File | Description |
|------|-------------|
| `index.html` | Main portfolio — Hero, About, Projects, Art teaser, Contact |
| `art.html` | Full art gallery — 31 artworks across 3 masonry sections |
| `index-dark.html` | Alternate dark variant |

---

## Features

### Hero Section
- **Portrait** — Photo with side-fade mask, teal glow aura, and water lily petal overlay
- **Checkerboard role-speller** — Canvas grid (left half) with 5×7 pixel-font letters that blink and pulse to spell **Software Developer**, **AI Engineer**, and **Game Developer** in glowing yellow
- **ASCII peel effect** — Mouse-tracking canvas that reveals ASCII density characters and sine wave lines within a copper-ringed radius around the cursor
- **Graph art SVG** — Parabolic curves, bezier sine waves, and axis tick marks in faint teal/copper
- **Three.js wireframe fragments** — Floating icosahedron/octahedron/box/tetrahedron wireframes that drift and respond to mouse parallax
- **HUD overlay** — Live coordinate readout in Courier New, copper color
- **Concentric radar rings** — Slow-spinning SVG rings with copper tick marks
- **Blueprint grid** — Faint technical-drawing grid across the full hero

### Site-wide
- Scroll progress bar (copper gradient)
- Custom cursor ring with RAF lerp
- Scroll-triggered reveal animations (IntersectionObserver)
- 3D card tilt on project cards (mouse hover)
- Mobile-responsive nav with toggle
- Contact form via `modal/contact.php`
- Vercel Analytics

---

## Stack

| Layer | Technology |
|-------|-----------|
| Markup | HTML5 (vanilla, no framework) |
| Styles | CSS3 — custom properties, `gallery-theme.css` |
| Interactivity | Vanilla JS — Canvas 2D API, SVG, RAF loops |
| 3D | [Three.js 0.163.0](https://threejs.org/) (CDN) |
| Fonts | Playfair Display + Inter (Google Fonts) |
| Deployment | [Vercel](https://vercel.com) |
| Analytics | `@vercel/analytics` |

---

## Project Structure

```
├── index.html              # Main portfolio page
├── art.html                # Art gallery page
├── index-dark.html         # Dark variant
├── vercel.json             # Vercel config (cleanUrls, no trailingSlash)
├── package.json
│
├── css/
│   ├── gallery-theme.css   # Primary theme 
│   ├── main.css
│   ├── style.css
│   ├── plugins.css
│   ├── colors.css
│   ├── dark.css
│   ├── nier-theme.css
│   └── font/               # Web fonts
│
├── js/
│   ├── init.js
│   ├── plugins.js
│   ├── jquery.js
│   ├── modernizr.custom.js
│   └── ie8.js
│
├── img/
│   ├── hero/               # Hero images (portrait, lily assets)
│   ├── about/              # About section photo
│   ├── portfolio/          # Project screenshots
│   ├── art/                # Art gallery images
│   ├── cv/                 # Resume PDF
│   ├── logo/
│   ├── thumbs/
│   └── svg/social/         # Social icons
│
└── modal/
    └── contact.php         # Contact form handler
```

---

## Design Tokens (CSS Custom Properties)

Defined in `gallery-theme.css`:

```css
--gallery-copper:        #b86a2e   /* Accent — copper */
--gallery-copper-light:  #d4894a   /* Hover / highlight copper */
--gallery-deep-teal:     #1a3a4a   /* Primary dark background */
--gallery-deeper-teal:   #0d2232   /* Darker sections (Projects) */
--gallery-darkest:       #07111a   /* Deepest bg (Contact, Footer) */
--gallery-warm-sand:     #e8e0d4   /* Light accent (Art teaser) */
```

---

## Local Development

No build step required — the site is plain HTML/CSS/JS.

```bash
# Serve locally (any static server works)
npx serve .
# or
python -m http.server 8080
```

> The contact form (`modal/contact.php`) requires a PHP-capable server to function.

---

## Deployment

Deployed automatically via Vercel on push to the main branch. Config in `vercel.json`:

```json
{
  "version": 2,
  "cleanUrls": true,
  "trailingSlash": false
}
```

---

## License

Personal portfolio — all content, artwork, and original code © Sadman Mazumder 2026. Not licensed for reuse or redistribution.
