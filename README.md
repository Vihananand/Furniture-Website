# Augusta Luxury — Furniture Website

A modern, responsive **Next.js (App Router)** website for a luxury furniture brand (Augusta Luxury).  
It includes a curated home page, product collection browsing, individual product-category gallery pages, and a **Custom Order** form that opens WhatsApp with a pre-filled message.

**Live site:** [https://furniture-website-kappa-five.vercel.app](https://www.augustaluxury.in/about)

---

## Tech Stack

- **Next.js 15** (App Router)
- **React 19**
- **Tailwind CSS v4** (via `@tailwindcss/postcss`)
- **next/image** for optimized images
- Google fonts via **`next/font`** (Inter + Cormorant Upright)

---

## Pages & Features

### Core pages
- **Home** (`app/page.js`)
  - Hero section + featured product links
- **Products** (`app/products/page.js`)
  - Category filter (All / Benches & Ottomans / Classic Sofas / Beds & Daybeds / Chaise Lounges & Settees)
  - Image grid with preview behavior (client-side)
- **Product gallery pages** (`app/products/*/page.js`)
  - Dedicated gallery pages such as:
    - Chesterfield Lounger Sofa
    - Ottoman Bench Sofa
    - Carved Sofas
    - Dining and Lighting
  - Click-to-preview modal-style behavior (client-side state)
- **About** (`app/about/page.js`)
- **Custom Order** (`app/custom-order/page.js`)
  - Collects name/email/phone/budget/category/message
  - Opens **WhatsApp Web / WhatsApp App** with a formatted message

### Layout
- Global layout in `app/layout.js`
- Shared UI:
  - `app/components/Navbar.js`
  - `app/components/Footer.js`
- Global styles: `app/globals.css`

---

## Getting Started (Local Development)

### 1) Install dependencies
```bash
npm install
```

### 2) Run the dev server
```bash
npm run dev
```

Then open: http://localhost:3000

---

## Production Build

```bash
npm run build
npm run start
```

---

## Images

This project uses:
- Local images from the `public/` folder (example paths like `/images/...`)
- Remote images are allowed from:
  - `images.unsplash.com`
  - `upload.wikimedia.org`

(See `next.config.mjs`.)

---

## Project Structure (High-level)

```text
app/
  layout.js
  globals.css
  page.js
  about/page.js
  products/
    page.js
    chesterfield-lounger-sofa/page.js
    ottoman-bench-sofa/page.js
    carved-sofas/page.js
    dining-and-lighting/page.js
  custom-order/page.js
  components/
    Navbar.js
    Footer.js
    Images.js
public/
  (static assets like logo.svg, images, etc.)
```

---

## Deployment

This repo is ready to deploy on **Vercel** as a standard Next.js app.

Typical flow:
1. Push to GitHub
2. Import repository into Vercel
3. Build command: `next build`
4. Output: Next.js default

---

## Notes / Customization

- To update branding text and metadata, edit: `app/layout.js` (title/description)
- To modify navigation, edit: `app/components/Navbar.js`
- To change the WhatsApp phone number or message format, edit: `app/custom-order/page.js`

---

## License

No license specified yet. If you want, add a `LICENSE` file (MIT is common for portfolio projects).
