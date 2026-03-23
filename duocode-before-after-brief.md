# Project: DuoCode Before/After Website Demo

Build a **single HTML file** (`index.html`) — no frameworks, no build tools, pure HTML/CSS/JavaScript only.

---

## Concept
A stunning before/after website demo for **DuoCode Technology**, a Malaysian web development agency. A toggle button in the top-right corner switches between two completely different visual states of the same website. This will be recorded as an Instagram Reels to showcase what DuoCode can do for SME clients.

---

## Brand Colors
- Navy Blue: `#1B3A5C`
- Teal/Cyan: `#00D4AA`
- Gold accent (After only): `#FFD700`

---

## Toggle Button (Always Visible)
- Fixed position, top-right corner
- Pill-shaped toggle switch
- Left label: `BEFORE` | Right label: `AFTER`
- OFF state = Before mode, ON state = After mode
- When toggled ON → trigger a dramatic full-screen **light sweep/flash transition** before revealing the After version
- Toggle button itself should always remain visible and on top (highest z-index)

---

## BEFORE Mode
**Goal: look like a cheap, outdated, boring website**

- Entire page in grayscale — background `#e0e0e0`, text `#555555`, borders `#bbbbbb`
- Font: Arial or Times New Roman
- Layout: flat, boxy, zero visual hierarchy
- Zero animations or transitions
- Sections (in order):
  - **Navbar**: plain gray bar, "DuoCode Technology" plain text logo, nav links: Home, Services, About, Contact
  - **Hero**: centered text block — headline "Welcome to DuoCode Technology", subtext "We build websites for your business.", a plain gray button "Contact Us"
  - **Services**: 3 plain gray cards in a row — "Web Design", "Web Development", "Digital Solutions" — each with a short boring one-liner description
  - **About**: two-column layout — left side a gray placeholder box (representing an image), right side a short paragraph about DuoCode
  - **Footer**: plain gray bar, copyright text

---

## AFTER Mode
**Goal: jaw-dropping, cinematic, animated — 青龙 (Azure Dragon) theme blended with DuoCode brand**

**Color palette**: Deep navy `#0a1628` background, teal `#00D4AA` primary, gold `#FFD700` accents, white text

**Typography**: Import from Google Fonts — use a bold display font for headings (e.g. Cinzel, Playfair Display, or Josefin Sans) and a clean modern font for body

### Full-screen Dragon Animation (Canvas)
- A canvas element sits behind all content (z-index: 0)
- An **Azure Dragon (青龙)** made of connected glowing teal/cyan particles flies across the entire screen in a sinuous, serpentine S-curve path
- Dragon body = 60–80 connected particle nodes, each glowing teal with a gold core
- It loops continuously, flying from left to right then looping back
- Particle trail fades behind the dragon head
- Additional ambient gold particles (50–80 small dots) float slowly upward across the entire canvas at all times

### Navbar
- Dark frosted glass background (`rgba(10, 22, 40, 0.85)`) with backdrop-filter blur
- "DuoCode Technology" logo text in teal-to-gold gradient
- Nav links with teal underline hover animation
- Thin gold border bottom on navbar

### Hero Section
- Full viewport height
- Large bold headline: "Transform Your Business Online" — teal-to-gold gradient text
- Subheadline: "DuoCode builds websites that don't just look good — they work hard for your business."
- Two CTA buttons: primary "Get Started" (teal fill, gold glow on hover), secondary "See Our Work" (outlined)
- Scroll-down animated arrow at bottom center

### Services Section
- Section title with gold underline decorator
- 3 cards with glassmorphism style (`rgba` background, backdrop blur, gold border)
- Cards: "Web Design", "Web Development", "Digital Solutions"
- Each card has a glowing teal icon (use Unicode or simple SVG), short description, hover effect that lifts the card with a gold glow shadow
- Cards animate in from below when section enters viewport (Intersection Observer)

### About Section
- Two-column layout
- Left: an animated decorative element — a glowing teal circle/ring with a Chinese-inspired geometric pattern or the DuoCode `</>` symbol inside, pulsing gently
- Right: paragraph about DuoCode — "We are a Malaysian digital agency helping SMEs grow their online presence with modern, high-performance websites."
- Subtle scroll-triggered fade-in

### Footer
- Dark background with teal top border
- "DuoCode Technology © 2025" centered
- Small tagline: "Empowering Malaysian SMEs, One Website at a Time."
- Social icons (FB, IG) as simple SVG circles with hover glow

### Toggle ON Transition (Before → After)
- A gold/white radial flash expands from the toggle button position across the full screen
- Duration: ~600ms
- After flash clears, After mode is fully revealed

### Toggle OFF Transition (After → Before)
- Simple fade to gray, ~400ms

---

## Technical Requirements
- Single `index.html` file, no external dependencies except Google Fonts CDN
- Canvas dragon animation must run at smooth 60fps
- Both modes share the same HTML structure — switching is done purely by toggling a CSS class (e.g. `body.after-mode`) and showing/hiding canvas
- All animations paused/removed in Before mode
- Mobile-responsive is a bonus but not required — optimise for desktop first (for screen recording)
