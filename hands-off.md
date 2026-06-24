# Hands-off Documentation: Havenbath Luxury Showroom Landing Page

This repository contains the Astro-based showroom landing page for **Havenbath by Msquare Groups**, Madurai's premier destination for luxury bathing solutions. The design is based on the Stitch prototype and implements a quiet, opulently minimalist five-star hotel spa aesthetic.

---

## 🛠️ Technology Stack

- **Framework**: [Astro v5.x](https://astro.build/) (Static Site Generation / Zero-JS by default where possible)
- **Styling**: [Tailwind CSS v4.x](https://tailwindcss.com/) (using the new Vite plugin `@tailwindcss/vite`)
- **Fonts**: 
  - *Playfair Display* (Serif headings, high-contrast, tight tracking)
  - *Montserrat* (Sans-serif body, labels, lighter weights for luxury catalog feel)
- **Icons**: Material Symbols Outlined
- **Hosting/Deployment**: [Vercel](https://vercel.com/) (Static deployment out-of-the-box)

---

## 🎨 Design System & Styling Tokens

The theme variables are configured inside `src/styles/global.css` using the Tailwind v4 `@theme` directive:

### Color Palette
- **Warm Ivory / Background** (`bg-surface`): `#F9F5EE` (softer and more premium than pure white)
- **Deep Charcoal / Text** (`text-on-surface`): `#1C1C1C` (editorial contrast)
- **Deep Champagne / Primary Accent** (`text-primary`): `#C9A84C`
- **Muted Gold / Dividers** (`.divider-gold`): `#E8D5A3`
- **Soft Warm White / Alternate Panels** (`bg-surface-container-low`): `#FDFAF4`

### Layout & Spacing
- **Gutter**: 32px
- **Desktop Margins**: 80px
- **Section Gaps**: 120px
- **Corner Radii**: Sharp corners (`rounded-none` / 0px) to project precision and structural elegance.

### Custom Classes
- `.glass-panel`: Frosted glass blur overlay for the location concierge card.
- `.divider-gold`: 1px thin separator lines.
- `.hero-vignette`: Radial gradient on the hero image to guarantee text readability.

---

## 📁 Project Structure

```
havebath/
├── public/
│   └── images/               # High-res local assets (Hero, Gallery, Icons)
├── src/
│   ├── layouts/
│   │   └── Layout.astro      # Global template (fonts, meta tags, SEO description)
│   ├── pages/
│   │   └── index.astro       # Landing page (Header, Hero, Heritage, Collection, Location, Footer)
│   └── styles/
│       └── global.css        # Tailwind @import, theme overrides, custom utilities
├── astro.config.mjs          # Astro configurator (Vite integration for Tailwind)
├── package.json              # Script runners and packages
└── hands-off.md              # Project handoff file (this file)
```

---

## 🚀 Local Development

Follow these steps to run the project locally:

1. **Install Dependencies**:
   ```bash
   npm install
   ```

2. **Start Dev Server**:
   ```bash
   npm run dev
   ```
   Open `http://localhost:4321` in your browser.

3. **Production Build**:
   ```bash
   npm run build
   ```
   This generates a static output inside the `dist/` directory.

---

## 🌐 Deployment to Vercel

Vercel automatically detects Astro projects and configures the build settings correctly without any special adapters:

- **Build Command**: `npm run build` or `astro build`
- **Output Directory**: `dist`
- **Install Command**: `npm install`

To deploy manually via CLI:
```bash
npx vercel
```
Or hook up the GitHub repository to your Vercel Dashboard for automated continuous deployment (recommended).
