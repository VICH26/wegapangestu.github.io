# Portfolio — Design Spec

## Overview
Enhance existing static portfolio (Bootstrap 5, Font Awesome) for Wega Pangestu — IT Support Technician. Target: personal branding + recruiters.

## Sections

### 1. Projects Section (new)
- Dedicated `#projects` section between Penghargaan and Sertifikat
- Card grid with thumbnail, title, description, tech stack badges, link buttons (Demo/GitHub/YouTube)
- **Waste Management System (WMS)** — IoT dashboard + AWS chatbot, Juara 1 Cloud Computing
  - Move project detail from Penghargaan to Projects
  - Add screenshot thumbnail from `img/` (or YouTube thumbnail)
  - Tech: IoT, AWS, AI Chatbot, Dashboard
  - Links: YouTube documentation
  - Status badge: "Selesai"
- 2 placeholder project cards for future work
- Penghargaan section retains only the award/prestige aspect (Juara 1, medal display)

### 2. Contact Form Functional
- Use Formspree for form handling (free tier, 50 submissions/month)
- Add `action="https://formspree.io/f/..."` to form
- Add hidden `_subject` input
- Add honeypot spam protection
- Show success/error feedback via JS after submission

### 3. UI Modernization
- **AOS (Animate On Scroll)** — CDN, data-aos attributes on sections/cards
- **Dark mode toggle** — button in navbar (sun/moon icon), CSS variables for colors, localStorage persistence
- **Smooth scroll refinement** — existing active link tracking works fine
- **Navbar shrink** — add class `navbar-shrink` on scroll > 80px, reduce padding

## Technical Decisions
- No build step — pure static HTML/CSS/JS
- CDN for AOS library
- Formspree for contact — no backend needed
- CSS custom properties for dark mode theming
- Keep Bootstrap 5 + Font Awesome CDN (already used)

## File Changes
- `index.html` — new section, form action, dark mode toggle, AOS init, navbar shrink JS
- `css/style.css` — dark mode variables, project card styles, navbar shrink, AOS overrides, form feedback
