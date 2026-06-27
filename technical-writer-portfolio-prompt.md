# 🧠 Master Prompt: Technical Writer Portfolio Website

Use this prompt with Claude (claude.ai) to build your complete portfolio. Paste it as-is, then follow the customization checklist at the bottom.

---

## THE PROMPT

---

Build me a **complete, single-file HTML portfolio website** for a Technical Writer with 4 years of experience. The output must be a single `.html` file with all CSS and JavaScript embedded inline — no external frameworks, no CDN dependencies except Google Fonts.

---

### 🎨 DESIGN SYSTEM

**Visual Identity:**
- **Color Palette:**
  - Background: `#0A0F1E` (deep navy-black)
  - Surface: `#111827` (card/section backgrounds)
  - Primary Accent: `#38BDF8` (sky blue — for headings, links, highlights)
  - Secondary Accent: `#818CF8` (soft indigo — for tags, borders, subtle glow)
  - Text Primary: `#F1F5F9` (near-white)
  - Text Muted: `#94A3B8` (slate gray)
  - Gradient: linear from `#38BDF8` → `#818CF8`
- **Typography:**
  - Display/Headings: `'Syne'` (Google Fonts) — bold, geometric
  - Body: `'Inter'` (Google Fonts) — clean, readable
  - Monospace labels/tags: `'JetBrains Mono'` (Google Fonts)
- **Design Language:** Dark futuristic editorial — minimal, high-contrast, technical precision aesthetic befitting a documentation professional
- **Signature Element:** An animated **dot-grid / particle canvas** background in the hero section, slowly drifting — symbolizing structured information systems

---

### ✨ ANIMATIONS & INTERACTIONS

Implement ALL of the following:

1. **Page Load:** Staggered fade-in + slide-up for hero text elements (name → title → tagline → CTA buttons), with 150ms delays between each
2. **Scroll Reveal:** Every section animates in on scroll using `IntersectionObserver` — elements slide up from `translateY(40px)` to `0` with `opacity: 0 → 1`, `transition: 0.6s ease`
3. **Navbar:** Transparent on hero, becomes `rgba(10,15,30,0.95)` with `backdrop-filter: blur(12px)` + subtle bottom border on scroll. Hamburger menu on mobile.
4. **Hero Canvas:** Animated particle/dot-grid background (canvas element) — 80 slow-drifting dots with faint connecting lines when close, in accent colors
5. **Skill Bars:** Animated width fill on scroll entry (from 0% to target %)
6. **Project Cards:** Subtle lift on hover (`translateY(-6px)`) + glow box-shadow in primary accent
7. **Active Nav Highlight:** Highlight the current section in the navbar using scroll spy
8. **Typing Effect:** Typewriter animation cycling through 3 roles below the name (e.g., "Technical Writer", "Documentation Specialist", "API Docs Author")
9. **Smooth Scroll:** All anchor links use smooth scroll behavior
10. **Back to Top Button:** Appears after 400px scroll, fades in/out
11. **Contact links:** Hover glow + icon bounce on hover
12. **Mobile Menu:** Slide-down animated mobile nav with close on link click

---

### 🗂️ SECTIONS (in order)

#### 1. NAVBAR
- Logo: "[Your Name]" in accent color, left-aligned
- Links: Home · About · Skills · Projects · Experience · Doc Samples · Contact
- Right side: "Download Resume" button (styled as outlined pill button)
- Sticky on scroll with blur effect
- Hamburger icon on mobile (animated to X on open)

---

#### 2. HERO SECTION
- Animated particle canvas background
- Badge pill: `✦ Available for Opportunities`
- Large display heading: "Hi, I'm **[Your Name]**"
- Typewriter subtitle cycling: `"Technical Writer"` | `"Documentation Specialist"` | `"API & Developer Docs Author"`
- One-line tagline: "Turning complex systems into clear, structured, human-readable documentation."
- Three CTA buttons: `[View My Work]` (primary filled) · `[Doc Samples]` (ghost) · `[Download Resume]` (ghost with icon)
- Stats row below: `4+ Years Experience` · `[X] Projects Documented` · `[X] Doc Types` · `Multi-Domain`
- Floating profile image on right (circular, with gradient glow ring), hidden on mobile
- Scroll indicator arrow at bottom

---

#### 3. ABOUT SECTION
- Section label: `— 01 / ABOUT`
- Two-column layout: left = text, right = a decorative card with a quote
- Paragraph about yourself (2–3 sentences about background, specialization, approach)
- Highlight 3 values in small icon cards: e.g., `📐 Precision` · `🔗 Collaboration` · `📚 Clarity`
- Quote block: *"I don't just write docs — I build systems for understanding."*

---

#### 4. SKILLS SECTION
- Section label: `— 02 / SKILLS`
- Two columns:
  - **Left: Skill bars** (with animated fill on scroll)
    - Technical Writing: 90%
    - API Documentation: 85%
    - DITA / XML Authoring: 80%
    - User Guides & SOPs: 88%
    - Information Architecture: 82%
    - Content Strategy: 78%
  - **Right: Tool Tags grid** (pill badges, in secondary accent color)
    - Tools: MadCap Flare · Confluence · Jira · GitHub · Markdown · Swagger / OpenAPI · Figma · Notion · Oxygen XML · Microsoft Word · Google Docs · Snagit
- Below: 3 strength cards in a row: `Technical Writing` · `UX Writing` · `Developer Docs`

---

#### 5. PROJECTS SECTION
- Section label: `— 03 / PROJECTS`
- Subtitle: "Selected documentation projects demonstrating structured authoring, developer communication, and workflow clarity."
- Grid of **4 project cards**, each with:
  - Category badge (e.g., `API Docs`, `User Guide`, `SOP`, `Developer Portal`)
  - Project title
  - 2-line description
  - Tech/tool tags
  - Two buttons: `[Live Demo →]` (links to live URL or `#`) + `[View Docs]`
  - Hover: lift + glow
- Placeholder projects (user to replace):
  1. **API Reference Guide** — REST API docs for a SaaS platform. Tags: `Swagger` `Markdown` `REST`
  2. **Developer Onboarding Portal** — End-to-end onboarding docs with code samples. Tags: `Confluence` `GitHub` `Markdown`
  3. **Enterprise SOP Library** — 50+ standard operating procedures for manufacturing. Tags: `DITA` `XML` `MadCap`
  4. **User Manual — Mobile App** — Full user guide for a mobile productivity app. Tags: `Figma` `Snagit` `Word`

---

#### 6. WORK EXPERIENCE SECTION
- Section label: `— 04 / EXPERIENCE`
- Vertical timeline layout (line on left, cards on right)
- Each card has:
  - Role title (large, accent color)
  - Company name + duration (muted)
  - Bullet list of 3–4 key contributions
  - Tool/skill tags at bottom
- Placeholder entries (user to replace):
  1. **Senior Technical Writer** — [Company Name] | Jan 2023 – Present
  2. **Technical Writer** — [Company Name] | Jun 2021 – Dec 2022
  3. **Junior Technical Writer / Intern** — [Company Name] | Jan 2021 – May 2021

---

#### 7. DOC SAMPLES SECTION
- Section label: `— 05 / DOC SAMPLES`
- Subtitle: "Live documentation samples demonstrating structured authoring, procedural writing, and developer-focused communication."
- Grid of **4 sample cards**, each with:
  - Category label badge: `Service Doc` / `API Docs` / `User Guide` / `SOP`
  - Title
  - 2-line description
  - 3 tag pills
  - `[View Documentation →]` button linking to external URL (placeholder `#`)
- Card styling: border with secondary accent, hover glow

---

#### 8. CONTACT SECTION
- Section label: `— 06 / CONTACT`
- Centered heading: "Let's Work Together"
- Subtext: "Open to Technical Writing, Documentation, and Developer Advocacy roles."
- Four contact cards in a row (2x2 on mobile), each with icon + label + value + link:
  - 📱 **Phone** → `tel:+91XXXXXXXXXX`
  - 📧 **Email** → `mailto:youremail@example.com`
  - 💼 **LinkedIn** → `https://linkedin.com/in/yourprofile`
  - 📄 **Resume** → download link to your PDF resume (use `download` attribute)
- Cards have hover lift + accent glow
- Each card is fully clickable

---

#### 9. FOOTER
- Left: `© 2025 [Your Name]. All rights reserved.`
- Center: nav links (Home · About · Skills · Contact)
- Right: LinkedIn + Email icon links
- Top border: 1px gradient line (accent colors)

---

### 📱 FULL RESPONSIVENESS

Implement responsive breakpoints for:
- **Mobile** (< 640px): Single column, stacked sections, hamburger nav, hidden profile image in hero
- **Tablet** (640px – 1024px): 2-column grids, adjusted font sizes
- **Laptop/Desktop** (> 1024px): Full layout as described

All touch targets minimum 44px. Font sizes scale with `clamp()`. No horizontal scroll at any breakpoint.

---

### ⚙️ TECHNICAL REQUIREMENTS

- **Single `.html` file** — all CSS in `<style>`, all JS in `<script>` at bottom
- Google Fonts loaded via `<link>` in `<head>`: Syne, Inter, JetBrains Mono
- `prefers-reduced-motion` media query respected — disable animations for users who prefer it
- Smooth scroll: `html { scroll-behavior: smooth; }`
- All external links: `target="_blank" rel="noopener noreferrer"`
- Resume download: `<a href="resume.pdf" download>` (user replaces with real path)
- Semantic HTML5: `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`
- No JavaScript frameworks — vanilla JS only
- Particle canvas must degrade gracefully if canvas not supported

---

### 🔧 CUSTOMIZATION PLACEHOLDERS

Use these exact placeholder strings so they're easy to find-and-replace:
- `[Your Name]` — full name
- `[Your Title]` — e.g., Technical Writer
- `[Your Tagline]` — one-line personal brand statement
- `[Your Email]` → `youremail@example.com`
- `[Your Phone]` → `+91XXXXXXXXXX`
- `[Your LinkedIn URL]` → `https://linkedin.com/in/yourprofile`
- `[Your Resume PDF]` → path to resume PDF
- `[Project Live URL]` → live demo links
- `[Doc Sample URL]` → doc sample links

---

### 🚫 DO NOT

- Do not use Bootstrap, Tailwind, or any CSS framework
- Do not use React, Vue, or any JS framework
- Do not use placeholder Lorem Ipsum — write realistic technical writer copy
- Do not add unnecessary animations that feel gimmicky
- Do not break mobile layout with fixed-width elements

---

Output the complete, working HTML file. All sections must be present and functional. Animations must work on first load without any build step.

---

## 📋 AFTER BUILDING — YOUR CUSTOMIZATION CHECKLIST

Once Claude generates the file, open it in a browser and update these:

- [ ] Replace `[Your Name]` everywhere
- [ ] Add your real email, phone, LinkedIn URL
- [ ] Upload your resume PDF and update the download link
- [ ] Replace project titles/descriptions with your real projects
- [ ] Replace work experience entries with your real employers and dates
- [ ] Add real links to your Doc Samples (your live hosted docs)
- [ ] Replace skill percentages with your actual confidence levels
- [ ] Add/remove tools from the tools grid
- [ ] Replace stats in hero (years, projects, doc types)
- [ ] Add your profile photo (replace the placeholder circle)

## 🚀 DEPLOYMENT OPTIONS

- **Free:** Upload to [Vercel](https://vercel.com) (drag and drop your HTML file) or [Netlify Drop](https://app.netlify.com/drop)
- **GitHub Pages:** Push to a repo → Settings → Pages → Deploy from main branch
- **Custom domain:** Point your domain to Vercel/Netlify after deployment

---

*Prompt crafted for a 4-year Technical Writer portfolio. Inspired by madhyam-mesta.vercel.app*
