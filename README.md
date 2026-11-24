# Bioline Laboratory — Demo Website

A premium single-page demo website for **Bioline Laboratory**, a NABL-accredited automated clinical laboratory. Built as a single `index.html` file with a dark glassmorphism design system.

## Run

No build step. Open `index.html` in a browser, or serve locally:

```bash
npx serve .
```

## Project Structure

```
demo_bioline/
├── index.html      # Entire app: markup, CSS, JS (single file)
├── assets/         # Media (hero video + images)
│   └── Designing_lab_like_bioline_c57b28e7.mp4
└── README.md
```

## Pages (SPA navigation via `navigateTo()`)

| Page | Highlights |
|---|---|
| Home | Video hero, glass booking bar, stats, "Why Bioline" scroll-stack cards, popular packages |
| Health Packages | Amazon-style filter sidebar + package grid |
| Services | 500+ tests across specialties |
| About Us | Story, stats, team |
| Careers | Open positions list |
| Contact | Info + message form |
| Login / Register | Tabbed auth forms |

## Design System

- **Fonts:** Plus Jakarta Sans (primary), Inter (fallback)
- **Icons:** Font Awesome 6.5.1
- **Palette:**
  - Deep green `#06402B` (background)
  - Primary green `#0A5C40`
  - Light green `#1a8856`
  - Orange accent `#FF6B2C`
- **Style:** Glassmorphism — `backdrop-filter: blur(24px) saturate(180%)`, translucent white borders, soft shadows, animated gradient blobs + noise texture background
- **Mobile performance:** Trust cards use native page scrolling on small screens; below-the-fold images load lazily, and the hero video is deferred to desktop devices that allow motion
- **Footer watermark:** Full-width "BIOLINE" SVG wordmark after the footer, low-opacity white fade (12% → 2%), bottom 1/4 of letters clipped at the screen edge (`textLength` guarantees edge-to-edge cover on all screen sizes)

## Image Asset Plan

Generate each image with the prompt below and save it in `assets/` with the exact filename. All images share the brand palette so they blend into the glass cards.

### 1. `hero-lab.png` — Hero right panel (`.hero-scene`) · 1200×900 (4:3)

```
Premium 3D render of three glass blood sample vials with orange caps on a glossy dark surface, one vial filled with deep orange liquid, sleek glass microscope behind, soft green and orange rim lighting, dark emerald green background (#06402B), translucent glassmorphism panels floating behind, cinematic soft shadows, depth of field, centered composition, ultra detailed octane render, no text, no watermark
```

### 2. `why-home-collection.png` — Why Bioline card 01 · 1024×1024

```
Premium 3D render of a professional home sample collection kit: open glossy medical case with orange-capped blood vials in a rack, sterile gloves, small glowing holographic house symbol floating above, dark emerald green background (#06402B), green and orange accent lighting (#1a8856, #FF6B2C), glassmorphism style, soft cinematic shadows, centered composition, ultra detailed, no text, no watermark
```

### 3. `why-digital-reports.png` — Why Bioline card 02 · 1024×1024

```
Premium 3D render of a floating glass smartphone showing a glowing medical report with abstract chart lines and a green checkmark seal, orange notification badge, translucent glass panels around it, dark emerald green background (#06402B), green and orange accent lighting (#1a8856, #FF6B2C), glassmorphism style, soft cinematic shadows, centered composition, ultra detailed, no readable text, no watermark
```

### 4. `why-nabl-labs.png` — Why Bioline card 03 · 1024×1024

```
Premium 3D render of a translucent glass award badge with a bold green checkmark seal and orange ribbon, subtle golden glow, floating above a glossy dark pedestal, dark emerald green background (#06402B), green and orange accent lighting (#1a8856, #FF6B2C), glassmorphism style, soft cinematic shadows, centered composition, ultra detailed, no text, no watermark
```

### 5. `why-pathologists.png` — Why Bioline card 04 · 1024×1024

```
Premium 3D render of a sleek modern glass microscope with a glowing holographic cell analysis floating above the slide, orange and green data rings, dark emerald green background (#06402B), green and orange accent lighting (#1a8856, #FF6B2C), glassmorphism style, soft cinematic shadows, depth of field, centered composition, ultra detailed, no text, no watermark
```

### 6. `why-automation.png` — Why Bioline card 05 · 1024×1024

```
Premium 3D render of a futuristic robotic arm handling orange-capped test tubes on a glossy conveyor line, glowing green scanner light, translucent glass safety panels, dark emerald green background (#06402B), green and orange accent lighting (#1a8856, #FF6B2C), glassmorphism style, soft cinematic shadows, centered composition, ultra detailed, no text, no watermark
```

### 7. `why-pricing.png` — Why Bioline card 06 · 1024×1024

```
Premium 3D render of a glossy glass price tag with orange ribbon and a glowing percent symbol, floating glass coins with soft orange glow, dark emerald green background (#06402B), green and orange accent lighting (#1a8856, #FF6B2C), glassmorphism style, soft cinematic shadows, centered composition, ultra detailed, no text, no letters, no watermark
```

### 8. `team-anil.png` — Dr. Anil Sharma, Chief Pathologist · 512×512

```
Photorealistic professional headshot of a distinguished Indian male doctor in his 50s, short gray-streaked hair, glasses, white lab coat over green scrubs, warm confident smile, dark emerald green studio background (#06402B), soft orange rim light, cinematic lighting, centered face composition, premium healthcare photography, square format, no text
```

### 9. `team-priya.png` — Dr. Priya Reddy, Head of Biochemistry · 512×512

```
Photorealistic professional headshot of a confident Indian female doctor in her 40s, dark hair tied back, white lab coat over green scrubs, stethoscope, warm smile, dark emerald green studio background (#06402B), soft orange rim light, cinematic lighting, centered face composition, premium healthcare photography, square format, no text
```

### 10. `team-vikram.png` — Dr. Vikram Kapoor, Microbiology Head · 512×512

```
Photorealistic professional headshot of an Indian male doctor in his 40s, neat beard, white lab coat over green scrubs, friendly assured expression, dark emerald green studio background (#06402B), soft orange rim light, cinematic lighting, centered face composition, premium healthcare photography, square format, no text
```

### 11. `team-sneha.png` — Dr. Sneha Nair, Molecular Diagnostics · 512×512

```
Photorealistic professional headshot of a young Indian female doctor in her 30s, shoulder-length dark hair, white lab coat over green scrubs, bright genuine smile, dark emerald green studio background (#06402B), soft orange rim light, cinematic lighting, centered face composition, premium healthcare photography, square format, no text
```

## Notes

- Demo data only (phone numbers, prices, reviews are placeholders).
- WhatsApp booking links use `openWhatsApp()` — replace placeholder numbers before production.
- Images are wired into the UI: hero panel (`.hero-scene`), six stack-card visuals (`.stack-card-right`), and four circular team avatars (`.team-avatar`).

## Health Packages Page (Understanding + Transparent PNG Image Prompt)

### Page Understanding

- **Top Bar:** "NABL ACCREDITED · SINCE 2008" and "AUTOMATED CLINICAL LABORATORY · 150+ BRANCHES"
- **Header:** glass-morphism nav — Logo "Bioline Laboratory" (flask icon + text), nav links (Home, Health Packages, Services, About Us, Careers, Contact), actions (Login icon, Cart, Book Now CTA with calendar icon, Hamburger menu)
- **Hero:** eyebrow "Health Packages" (box-open icon), title "Comprehensive Health Packages" (green-orange gradient), subtitle "Search and filter from our wide range of curated health checkup packages.", "Filters & Categories" toggle button
- **Layout (`#amz-layout`):** filter sidebar (glass card, full height) + results area:
  - Category checkboxes: Full Body (2), Diabetes (2), Heart Care (1), Thyroid (1), Vitamin (1), Liver (1), Kidney (1), Women's Health (1), Senior Citizen (1), Family / Pre-Marital (1)
  - Price range radios: All Prices / Under ₹500 / ₹500 – ₹1,000 / ₹1,000 – ₹2,000 / Above ₹2,000
  - Age group radios: All Ages / General (All Ages) / Adult (18+) / Senior (50+)
  - Sort by radios: Popularity / Price: Low to High / Price: High to Low / Discount
  - Results bar: "Showing 8 of 8 results" + "Free home collection on all bookings"
- **Package Cards (8, glass-morphism):**
  - Full Body Checkup Advanced — 92 Tests Included — ₹2,499 (was ₹5,500, 54% OFF)
  - Women's Wellness — POPULAR badge — 67 Tests Included — ₹1,799 (was ₹4,200, 57% OFF)
  - Senior Citizen Health — 78 Tests Included — ₹2,999 (was ₹6,800, 56% OFF)
  - Heart Care Profile — 35 Tests Included — ₹1,299 (was ₹3,000, 56% OFF)
  - Diabetes Care Plus — 28 Tests Included — ₹899 (was ₹2,100, 57% OFF)
  - Liver Function Test — 11 Tests Included — ₹499 (was ₹1,200, 58% OFF)
  - Kidney Function Test — 14 Tests Included — ₹599 (was ₹1,500, 60% OFF)
  - Pre-Marital Checkup — 45 Tests Included — ₹1,999 (was ₹4,800, 58% OFF)
  - Each card has: View Details / Book Now / WhatsApp buttons
- **Process (4 steps):** Select Package / Book Slot / Sample Collection / Get Reports
- **Background:** deep green (#06402B) with green/orange radial blobs + noise texture. **Health Packages page unique design pattern** (`.page-flow-geo`): transparent full-height layer — dotted lattice + fine grid lattice + drifting lines, low opacity (~6%).

### Transparent PNG Generation Prompt

Generate a transparent PNG mockup of the Health Packages page (suggested filename: `assets/health-packages-page.png`):

```
A clean, high-end web design mockup of the Bioline Laboratory Health Packages page, generated as a TRANSPARENT PNG image (full transparent background). Include: a glass-morphism header at the top — a top bar row reading "NABL ACCREDITED · SINCE 2008" and "AUTOMATED CLINICAL LABORATORY · 150+ BRANCHES", then a glass nav bar with the logo "Bioline Laboratory" (flask icon + text) and nav links Home / Health Packages / Services / About Us / Careers / Contact, plus Login, Cart icons and a Book Now button (calendar icon + "Book Now"). Below it, the hero section with an upward label "Health Packages", a large heading "Comprehensive Health Packages" in a green-to-orange gradient, subtitle "Search and filter from our wide range of curated health checkup packages.", and a "Filters & Categories" toggle button. To the right, a glass sidebar panel with a "Filters" heading and sections: Category checkboxes (Full Body, Diabetes, Heart Care, Thyroid, Vitamin, Liver, Kidney, Women's Health, Senior Citizen, Family / Pre-Marital), Price Range radio buttons (All Prices, Under ₹500, ₹500 - ₹1,000, ₹1,000 - ₹2,000, Above ₹2,000), Age Group radio buttons (All Ages, General, Adult, Senior), and Sort By radio buttons (Popularity, Price: Low to High, Price: High to Low, Discount). Next to the sidebar, a grid of 8 glass-morphism package cards with names, test counts, and prices: Full Body Checkup Advanced — 92 Tests Included — ₹2,499 (₹5,500, 54% OFF), Women's Wellness — POPULAR — 67 Tests Included — ₹1,799 (₹4,200, 57% OFF), Senior Citizen Health — 78 Tests Included — ₹2,999 (₹6,800, 56% OFF), Heart Care Profile — 35 Tests Included — ₹1,299 (₹3,000, 56% OFF), Diabetes Care Plus — 28 Tests Included — ₹899 (₹2,100, 57% OFF), Liver Function Test — 11 Tests Included — ₹499 (₹1,200, 58% OFF), Kidney Function Test — 14 Tests Included — ₹599 (₹1,500, 60% OFF), Pre-Marital Checkup — 45 Tests Included — ₹1,999 (₹4,800, 58% OFF), each with View Details / Book Now / WhatsApp buttons. Below, a 4-step process section: Select Package, Book Slot, Sample Collection, Get Reports. Include a faint unique design pattern background on the page: dotted lattice + fine grid lattice lines in low opacity (green #06402B and orange #FF6B2C, ~6% opacity). Style: medical diagnostics, glassmorphism cards, translucent white panels, dark emerald green palette with orange accents, soft shadows, ultra detailed, high fidelity, transparent background, no text watermark. Size: 1920x1080, PNG format.
```
