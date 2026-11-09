# RASTER · Kaffee & Lab

> A premium, modern landing page designed for an artisanal specialty coffee roastery and tasting lab.

RASTER is a premium, modern landing page and digital experience designed for an artisanal specialty coffee roastery and tasting lab. Built with strict adherence to Josef Müller-Brockmann's Swiss International Typographic Style, the project combines a mathematical 12-column grid, sharp 0px architectural geometry, kinetic GSAP microinteractions, and direct-trade commerce channels.

---

## Technology Stack

This project is built using modern web performance standards, prioritizing zero-runtime overhead, buttery smooth scrolling, and strict typographic discipline.

- **Architecture**: Modular HTML Component Pipeline with custom Node.js Compiler (`build.js`)
- **Styling**: Tailwind CSS & Master 12-Column Swiss Grid Overlay
- **Typography**: Manrope (Google Fonts Variable 300–800)
- **Animations**: GSAP (GreenSock Animation Platform 3.12) & ScrollTrigger
- **Smooth Scrolling**: Studio Freight Lenis
- **Mapping**: Leaflet.js with custom monochrome CARTO Positron architectural tiles
- **Iconography**: Phosphor Icons Web (`@phosphor-icons/web`)

---

## Architecture & Project Structure

The codebase is organized into independent, isolated section templates that compile into static production outputs for maximum speed and maintainability.

```text
coffee_shop/
├── sections/                        # Modular section components
│   ├── navbar.html                  # 100% transparent floating masthead & kinetic CTA
│   ├── hero.html                    # Monumental editorial headline & 4-plate filmstrip
│   ├── about.html                   # Tlogomas roastery narrative & editorial portrait
│   ├── beans.html                   # Specialty single-origin beans catalog & modal preview
│   ├── menu.html                    # 4-track cafe drinks index with museum thumbnail frames
│   ├── gallery.html                 # Spatial photography filmstrip & roastery bar atmosphere
│   ├── visit.html                   # Flagship location with architectural Leaflet map
│   └── footer.html                  # Editorial directory, single-origin roasts & colophon
├── images/                          # Curated high-res editorial photography & packshots
├── build.js                         # Zero-dependency Node.js compiler script
├── index.html                       # Compiled flagship landing page
├── bean-detail.html                 # Standalone single-origin product page (Shopee & WA)
└── README.md                        # Project documentation
```

---

## Design System & Theming

RASTER adheres strictly to the tenets of the **Swiss International Typographic Style**:

- **Strict 0px Radius**: No rounded corners (`rounded-none` across cards, frames, and buttons).
- **Zero All-Caps / Uppercase**: Pure sentence case and natural casing for balanced readability.
- **Museum Hairline Framing**: 1.5px solid borders (`rgba(49, 87, 98, 0.2)`) and honest negative space without blurry drop shadows.
- **Architectural Shutter Motion**: Interactive elements utilize vertical shutter wipe transitions inspired by darkroom photography and mechanical apertures.

### Official Brand Palette

| Color Token | Hex Code | Visual Application |
|---|---|---|
| **Signature Orange** | `#E9631A` | Brand accents, geometric grid mark, primary CTA backgrounds |
| **Flash White** | `#EFEFEF` | Neutral canvas, typography on dark surfaces, background fill |
| **Dark Slate** | `#315762` | Structural grid lines, body copy, secondary navigation links |
| **Deep Charcoal** | `#162B31` | Headings, brand wordmark, kinetic shutter hover states |

---

## Getting Started

### Prerequisites

Ensure you have [Node.js](https://nodejs.org/) installed (version 16 or newer recommended).

### Compilation & Development

1. Clone or download the repository:
   ```bash
   git clone https://github.com/your-username/raster-coffee.git
   cd raster-coffee
   ```

2. Compile all modular section templates into `index.html` and `bean-detail.html`:
   ```bash
   node build.js
   ```

3. Preview the application locally using any static web server:
   ```bash
   # Using npx serve
   npx serve .

   # Or using Python's built-in HTTP server
   python -m http.server 3000
   ```
   Open `http://localhost:3000` in your browser.

---

## Code Standards

- **Component Isolation**: All layout updates must be made inside `/sections/*.html` and compiled via `node build.js`. Do not edit the compiled `index.html` directly.
- **Typography Discipline**: Maintain natural casing across all headings and labels. Never apply CSS `uppercase` or forced all-caps.
- **Geometry**: Preserve sharp `rounded-none` corners on all containers, images, and interactive buttons.
- **Map Aesthetics**: Preserve the monochrome CARTO Positron tile filter to keep spatial maps 100% on-brand with the roastery's visual identity.
