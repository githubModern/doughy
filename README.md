<!-- © Atia Hegazy — atiaeno.com -->

<div align="center">

# 🍩 Doughy — Premium Donut Shop

**A handcrafted, pixel-perfect e-commerce storefront for a boutique donut brand.**

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Responsive](https://img.shields.io/badge/Responsive-4CAF50?style=for-the-badge&logo=google-chrome&logoColor=white)](#responsive-design)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

[Live Demo](#) · [Screenshots](#-screenshots) · [Features](#-features) · [Architecture](#-architecture) · [Getting Started](#-getting-started)

</div>

---

## 📸 Screenshots

### Homepage
![Homepage](screenshots/home.png)

### Shop — Product Catalog
![Shop](screenshots/shop.png)

### Product Detail
![Product Detail](screenshots/product.png)

### Authentication
![Login](screenshots/login.png)

### FAQ — Interactive Accordion
![FAQ](screenshots/faq.png)

### Delivery Info — Timeline & Zones
![Delivery](screenshots/delivery.png)

### Refund Policy — Step-by-Step Process
![Refund](screenshots/refund.png)

### Mobile Responsive
![Mobile](screenshots/mobile-home.png)

---

## ✨ Features

### 🛍️ E-Commerce Core
- **Product catalog** with category filtering, search, price range slider, and sorting
- **Product detail page** with image gallery, size/quantity selectors, nutritional info tabs, and customer reviews
- **Shopping cart** with real-time quantity updates, promo code support, and order summary
- **Checkout flow** with delivery options, payment method selection, and order confirmation with confetti animation

### 🔐 Authentication System
- **Login page** with email/password, social login (Google/Apple), remember me, and toast notifications
- **Registration page** with password strength meter, real-time validation, and terms acceptance
- **Forgot password flow** — 3-step process: email → confirmation → new password with toggle visibility

### 📄 Information Pages
- **FAQ** — Interactive accordion with categorized sections and smooth toggle animations
- **Delivery Info** — Visual timeline, delivery zone table with fees, packaging details
- **Cookie Policy** — Cookie type breakdown, detailed cookie table, management instructions
- **Privacy Policy** — Data collection overview, rights summary, info cards for key guarantees
- **Terms of Service** — Numbered sections with clear headings and cross-linked policies
- **Refund Policy** — Visual step-by-step process, eligibility tables, refund option cards

### 🍪 Cookie Consent Bar
- GDPR-friendly fixed bottom bar with accept/settings actions
- Persists consent via `localStorage`
- 1.5s delayed entrance animation
- Present across **all 15 pages**

### 📱 Responsive Design
- Mobile-first approach with breakpoints at `900px` and `600px`
- Slide-in mobile navigation drawer with overlay
- Responsive grid layouts that gracefully collapse on smaller screens
- Touch-friendly tap targets and interactive elements

---

## 🏗️ Architecture

### Project Structure

```
doughy/
├── index.html              # Homepage — hero, featured products, testimonials
├── shop.html               # Product catalog with filters & sorting
├── product.html            # Single product detail page
├── cart.html               # Shopping cart with quantity controls
├── checkout.html           # Checkout flow with payment options
├── account.html            # User account dashboard with tabs
├── login.html              # Login with social auth options
├── register.html           # Registration with password strength
├── forgot-password.html    # 3-step password reset flow
├── faq.html                # FAQ with interactive accordion
├── delivery.html           # Delivery zones, timeline, packaging
├── cookies.html            # Cookie policy with detail table
├── privacy.html            # Privacy policy with rights cards
├── terms.html              # Terms of service
├── refund.html             # Refund policy with step process
├── style.css               # Single consolidated stylesheet (~5500 lines)
├── screenshots/            # Project screenshots for documentation
│   ├── home.png
│   ├── shop.png
│   ├── product.png
│   ├── login.png
│   ├── faq.png
│   ├── delivery.png
│   ├── refund.png
│   └── mobile-home.png
└── README.md               # This file
```

### Design System

| Token | Value |
|-------|-------|
| **Primary Font** | Fredoka (headings) |
| **Body Font** | Nunito (body text) |
| **Pink** | `#FF6B9D` |
| **Yellow** | `#FFD93D` |
| **Blue** | `#6C5CE7` |
| **Green** | `#00B894` |
| **Orange** | `#FF9F43` |
| **Dark** | `#2D1B69` |
| **Border Radius** | 16–24px (playful, rounded) |
| **Border Style** | 3px solid dark (bold, graphic) |

### CSS Architecture

The project uses a **single consolidated stylesheet** (`style.css`) organized into clear sections:

1. **CSS Custom Properties** — Design tokens as variables
2. **Base & Reset** — Normalize and foundation styles
3. **Navigation** — Desktop nav, mobile drawer, hamburger
4. **Components** — Buttons, badges, tags, cards, forms
5. **Page-Specific** — Homepage, shop, product, cart, checkout, account
6. **Auth Pages** — Login, register, forgot password
7. **Info Pages** — FAQ, delivery, cookies, privacy, terms, refund
8. **Cookie Bar** — Consent banner
9. **Animations** — Keyframes for wiggle, bounce, float, confetti
10. **Responsive** — Media queries for tablet and mobile

### Key Technical Decisions

| Decision | Rationale |
|----------|-----------|
| **Zero dependencies** | Pure HTML/CSS/JS — no frameworks, no build tools, instant load |
| **Single CSS file** | Reduced HTTP requests, easier cache invalidation, single source of truth |
| **No inline styles** | All styles extracted to `style.css` for maintainability and CSP compliance |
| **CSS Custom Properties** | Consistent theming, easy to modify brand colors in one place |
| **Semantic HTML** | Proper use of `<nav>`, `<main>`, `<footer>`, `<section>` for accessibility |
| **Progressive Enhancement** | Core content works without JS; JS enhances interactivity |
| **localStorage** | Cookie consent persistence without server dependency |

---

## 🚀 Getting Started

### Prerequisites

Any static file server. No build step required.

### Quick Start

```bash
# Clone the repository
git clone https://github.com/githubModern/doughy.git

# Open directly in browser
open doughy/index.html

# Or serve with any static server
cd doughy
npx serve .
# or
python -m http.server 8000
```

### Local Development (XAMPP)

```bash
# Clone into your htdocs directory
cd C:\xampp\htdocs
git clone https://github.com/githubModern/doughy.git dle

# Navigate to http://localhost/dle/index.html
```

---

## 🎨 Design Philosophy

Doughy's design follows a **bold, playful, neo-brutalist** aesthetic that stands out from generic e-commerce templates:

- **Thick borders** (3px solid) create a graphic, sticker-like feel
- **Saturated candy colors** reinforce the donut/bakery brand identity
- **Generous whitespace** and large padding give content room to breathe
- **Emoji as icons** — zero icon library dependency, universally supported, on-brand personality
- **Micro-interactions** — hover lifts, wiggle animations, toast notifications, confetti bursts
- **Card-based layouts** — every content block is a tactile, bordered card

---

## 📄 Pages Overview

| Page | Description | Key Features |
|------|-------------|--------------|
| `index.html` | Homepage | Hero banner, featured products grid, testimonials, newsletter |
| `shop.html` | Product catalog | Category chips, search, price slider, sort, 12 product cards |
| `product.html` | Product detail | Gallery, variants, quantity, tabs (description/nutrition/reviews) |
| `cart.html` | Shopping cart | Line items, quantity +/−, promo codes, order summary |
| `checkout.html` | Checkout | Delivery options, payment methods, confetti on submit |
| `account.html` | Dashboard | Tabs: orders, profile, addresses, loyalty, settings |
| `login.html` | Login | Email/password, social auth, remember me, toast redirect |
| `register.html` | Register | Full form, password strength meter, terms checkbox |
| `forgot-password.html` | Password reset | 3-step flow with email → confirm → new password |
| `faq.html` | FAQ | 8 questions in accordion with smooth toggle |
| `delivery.html` | Delivery info | 4-step timeline, zone table, hours, packaging |
| `cookies.html` | Cookie policy | Cookie types, detail table, management guide |
| `privacy.html` | Privacy policy | Data collection, sharing, rights cards |
| `terms.html` | Terms of service | 10 numbered sections, cross-linked policies |
| `refund.html` | Refund policy | 4-step process cards, eligibility, timeline table |

---

## 🌐 Browser Support

| Browser | Support |
|---------|---------|
| Chrome 90+ | ✅ Full |
| Firefox 88+ | ✅ Full |
| Safari 14+ | ✅ Full |
| Edge 90+ | ✅ Full |
| Mobile Safari | ✅ Full |
| Chrome Android | ✅ Full |

---

## 📊 Performance

- **0 dependencies** — no npm, no node_modules, no build step
- **2 HTTP requests** for styles (1 Google Fonts + 1 CSS file)
- **No JavaScript frameworks** — vanilla JS for interactivity only
- **< 200KB total page weight** (excluding screenshots)
- **Instant FCP** — no render-blocking JS

---

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

## 👩‍💻 Author

**Atia Hegazy**

- Website: [atiaeno.com](https://atiaeno.com)
- GitHub: [@githubModern](https://github.com/githubModern)

---

<div align="center">
  <p>Made with 🍩 and love</p>
  <p><strong>© Atia Hegazy — atiaeno.com</strong></p>
</div>
