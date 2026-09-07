# Handoff: SAS Landing Page

## Overview
Single-page marketing landing for **Smart Automation System (SAS)** — a social media automation service for small businesses. The page guides visitors through a video → tariffs → brief-filling funnel.

## About the Design Files
The files in this bundle are **high-fidelity HTML prototypes** — production-ready visuals with final colors, typography, spacing, and all interactions implemented. A developer can either deploy the HTML/CSS/JS directly (it has no build step dependencies) or recreate it in a target framework (React, Vue, Next.js, etc.) using the values documented here as the source of truth.

## Fidelity
**High-fidelity.** Every color, font size, spacing, animation easing, and copy string in this document reflects the final design. Recreate pixel-perfectly.

---

## Sections / Screens

### 1. Sticky Nav
**Purpose:** Global navigation, always visible.
**Layout:** `position:sticky; top:0; z-index:50`. Inner container `width:min(1160px, calc(100% - 40px)); margin:auto`. Nav row `height:76px; display:flex; justify-content:space-between; align-items:center; gap:16px; flex-wrap:wrap`.
**Components:**
- Logo: `font-weight:900; letter-spacing:-0.07em; font-size:28px`. "SAS" + blue dot `color:#1F3A93`.
- Links row: `display:flex; gap:22px; flex-wrap:wrap`.
  - "Тарифы" / "Вопросы" pill links: `font-weight:700; font-size:14px; padding:8px 16px; border-radius:100px; border:1px solid transparent; transition:background .25s, border-color .25s`. Hover: `background:#e6ecff; border-color:#c7d3f7`.
  - "Оставить заявку" outline pill: same font, `border:1px solid #1F3A9333; color:#1F3A93`. Hover: `background:#e6ecff`. Hidden on screens ≤700px.
  - "Заполнить бриф →" gradient CTA: `padding:14px 21px; border-radius:100px; background:linear-gradient(135deg,#2b46b0,#1F3A93); color:#fff; font-weight:750; box-shadow:0 8px 20px #1f3a9340`.
**Background:** `background:#f4f6fdb3; backdrop-filter:blur(16px); border-bottom:1px solid #ffffffb3`.
**Responsive:** ≤700px hide "Оставить заявку", reduce paddings; ≤400px reduce font sizes further.

---

### 2. Hero
**Purpose:** First impression — headline, value prop, CTAs, hero video.
**Layout:** Grid `repeat(auto-fit, minmax(300px,1fr)); gap:clamp(28px,4vw,46px); padding:clamp(36px,6vw,72px) 0 50px`.
**Left column:**
- Eyebrow: `font-size:12px; letter-spacing:.12em; text-transform:uppercase; font-weight:800; color:#4c5a78`. Text: "Smart Automation System".
- H1: `font-size:clamp(40px,6vw,74px); line-height:1.08; letter-spacing:-.07em`. Highlight "публикуются сами": `background:#cfd6f2; padding:0 .08em`.
- Body: `font-size:19px; color:#5b6478; max-width:590px`.
- CTA row `display:flex; gap:12px; flex-wrap:wrap`:
  - "Заполнить бриф →": gradient pill (same as nav CTA), `box-shadow:0 10px 26px #1f3a9345`.
  - "Смотреть видео ↓": glass pill `background:#ffffff8c; backdrop-filter:blur(12px); border:1px solid #ffffffcc; color:#171a24`.
- Social proof row: overlapping avatars (AI/VK/TG circles, 31px, `background:#cfd6f2`) + text.
**Right column:** Dark video card `background:linear-gradient(160deg,#0b1130,#16215c,#1F3A93); border-radius:30px; min-height:420px; overflow:hidden; box-shadow:0 25px 55px #0f204d40`. Contains autoplay muted looping `<video>` with poster `assets/bg-workflow.png`.

---

### 3. 5-Minute Video Section
**Purpose:** Key qualification — visitor watches before deciding on a tariff.
**Background:** `linear-gradient(165deg,#0b1130,#182463,#1F3A93)`. Section `padding:86px 0`.
**Layout:** Centered `max-width:640px` text header + `max-width:820px` video card.
**Video card:** `padding:14px; border-radius:28px; background:#ffffff14; backdrop-filter:blur(20px); border:1px solid #ffffff2e; box-shadow:0 30px 60px #0f204d55`. Inner 16:9 iframe (VK Video embed).
**Below video:** White CTA button `background:#fff; color:#1F3A93; font-weight:800; font-size:17px; padding:18px 34px; border-radius:100px; box-shadow:0 14px 34px #05081f66`. Hover: `transform:translateY(-4px) scale(1.03)`.

---

### 4. How It Works (Steps)
**Purpose:** Explain the 4-step process.
**Layout:** `padding:86px 0`. Grid `repeat(auto-fit,minmax(230px,1fr)); gap:12px`.
**Cards:** `border:1px solid #ffffffb3; border-radius:18px; padding:22px; background:#ffffff85; backdrop-filter:blur(16px); box-shadow:0 8px 24px #1f3a9312`. Step number: 30px circle `background:#e3eaf9`.

---

### 5. "Для малого бизнеса" Features
**Purpose:** 3 key differentiators.
**Background:** Dark overlay over `assets/bg-workflow.png` + `linear-gradient(170deg,#0b1130e6,#141d4dd9,#10182cf0); backdrop-filter:blur(2px)`. Section `padding:86px 0`.
**Cards:** `background:#ffffff14; border:1px solid #ffffff2e; border-radius:16px; padding:24px`. No hover animation. Line-icon SVGs in `#8fb4ff`, 44×44px.

---

### 6. Tariffs
**Purpose:** Pricing grid, each card links to brief.
**Layout:** `padding:86px 0`. Grid `repeat(auto-fit,minmax(230px,1fr)); gap:12px; align-items:stretch`.
**Cards (non-featured):** `background:#ffffff85; backdrop-filter:blur(16px); border:1px solid #ffffffb3; border-radius:18px; padding:22px; box-shadow:0 8px 24px #1f3a9312`. Hover: `background:linear-gradient(160deg,#cfd6f2cc,#7b8dc9b3); transform:translateY(-16px) scale(1.03); box-shadow:0 20px 44px #1f3a9330`. Transition: `transform .6s cubic-bezier(.22,1.6,.36,1), box-shadow .6s cubic-bezier(.22,1.6,.36,1), background .3s`. `will-change:transform`.
**Featured card (БИЗНЕС):** Same but always `background:linear-gradient(160deg,#cfd6f2cc,#7b8dc9b3); transform:translateY(-10px); box-shadow:0 16px 36px #1f3a9330`. Badge: `background:#171a24; color:#fff; font-size:10px; padding:5px 12px; border-radius:100px`.
**Price font:** `font-size:33px; font-weight:850; letter-spacing:-.06em`.
**All cards link to brief** (same Google Forms URL).

---

### 7. FAQ Accordion
**Purpose:** Answer pre-sale objections.
**Layout:** `padding:86px 0`. Max-width 820px grid of items, `gap:12px`.
**Items:** `background:#ffffff85; backdrop-filter:blur(16px); border:1px solid #ffffffb3; border-radius:16px; padding:20px 24px; cursor:pointer`. No hover effect.
**Animation:** On click, content div transitions `grid-template-rows: 0fr → 1fr` with `transition:.45s cubic-bezier(.22,.8,.36,1)`. Inner div gets `min-height:0` to collapse.
**6 questions** (see HTML source for copy).

---

### 8. "Первый шаг" CTA Block
**Purpose:** Final push to fill brief.
**Background:** `linear-gradient(160deg,#16215c,#1F3A93,#2b46b0)`. Padding: `clamp(28px,5vw,65px)`. Border-radius: 26px.
**Inner glass card:** `background:#ffffff14; backdrop-filter:blur(20px); border:1px solid #ffffff2e; border-radius:20px`.
**H2:** `font-size:clamp(32px,4.7vw,58px); line-height:1.06; letter-spacing:-.07em`.
**CTA button:** White pill, `color:#1F3A93`.
**Tariff chips:** `background:#ffffff26; border:1px solid #ffffff33; border-radius:100px; padding:8px 14px; font-size:13px`.

---

### 9. Contact Form Block ("Пока не готовы к брифу?")
**Purpose:** Capture leads not ready for full brief.
**Background:** `linear-gradient(170deg,#0b1130,#141d4d,#10182c)`. Border-radius: 24px. id=`contact-form`.
**Layout:** Grid `repeat(auto-fit,minmax(260px,1fr)); gap:36px; align-items:center`. Left: `assets/contact-phone.png` (transparent PNG, max-width:480px, margin:-40px 0). Right: title + form.
**Form grid:** `repeat(auto-fit,minmax(180px,1fr)); gap:10px`. Fields: `background:#ffffffe0; border:1px solid #ffffffcc; border-radius:10px; padding:12px`. Focus: `border-color:#1F3A93`.
**Custom dropdown:** Custom-built (not native `<select>`). Button triggers open/close state. Options list: `background:#141d4d; border-radius:12px; border:1px solid #ffffff2e`. Animate open via `max-height:0→300px; opacity:0→1; visibility:hidden→visible; transform:translateY(-6px)→0`. When closed: `pointer-events:none` to prevent click-through blocking submit button.
**Submit button:** `background:linear-gradient(135deg,#2b46b0,#1F3A93); color:#fff; border-radius:10px; padding:13px 15px`.

---

## Interactions & Behavior

| Interaction | Behavior |
|---|---|
| Nav anchor links | `scroll-behavior:smooth` on `html` |
| Tariff card hover | Spring lift `translateY(-16px) scale(1.03)` + shadow, easing `cubic-bezier(.22,1.6,.36,1) .6s` |
| Feature icon hover | `scale(1.22) rotate(-4deg)`, `cubic-bezier(.34,1.56,.64,1) .35s` |
| Nav link hover | `background:#e6ecff; border-color:#c7d3f7` |
| FAQ item click | Toggle open/close, `grid-template-rows` transition `.45s cubic-bezier(.22,.8,.36,1)` |
| Dropdown open | Max-height expand + opacity fade + slight translateY |
| Hero video | Autoplay, muted, loop, playsInline. `play()` called from componentDidMount. Poster: `assets/bg-workflow.png` |
| Form submit | Prevent default, show confirmation note in `formNote` field |

---

## State Variables

| Variable | Type | Default | Purpose |
|---|---|---|---|
| `selectedPlan` | string | `'Нужна помощь с выбором'` | Selected tariff |
| `planOpen` | boolean | `false` | Dropdown open state |
| `openFaq` | number\|null | `null` | Open FAQ index |
| `formNote` | string | consent text | Submission feedback |

---

## Design Tokens

### Colors
| Token | Value | Usage |
|---|---|---|
| Brand blue | `#1F3A93` | Primary CTAs, accents |
| Blue dark | `#2b46b0` | Gradient start |
| Navy 1 | `#0b1130` | Dark section bg |
| Navy 2 | `#141d4d` | Dark card bg |
| Navy 3 | `#10182c` | Dark section end |
| Navy 4 | `#16215c` | CTA section bg |
| Text primary | `#171a24` | Body text |
| Text muted | `#5b6478` | Subtext |
| Text light | `#c0cbe0` | Dark bg subtext |
| Text lighter | `#dbe2f7` | Dark bg body |
| Surface light | `#f4f6fd` | Page bg |
| Glass light | `#ffffff85` | Light frosted cards |
| Glass dark | `#ffffff14` | Dark frosted cards |
| Highlight | `#cfd6f2` | H1 word highlight |
| Icon blue | `#8fb4ff` | SVG icon stroke |

### Typography
- Font: **Inter** (weights 400/600/700/800/900) from Google Fonts
- H1: `clamp(40px,6vw,74px)`, weight 900, `letter-spacing:-.07em`, `line-height:1.08`
- H2: `clamp(30px,4vw,50px)`, weight 800, `letter-spacing:-.06em`
- Body: 16–19px, `line-height:1.5`
- Small/eyebrow: 12px, `letter-spacing:.12em`, `text-transform:uppercase`, weight 800

### Spacing
- Section padding: `86px 0` (desktop)
- Container: `width:min(1160px, calc(100% - 40px)); margin:auto`

### Border Radii
- Cards large: 18–26px
- Cards small: 16px
- Buttons/pills: 100px
- Video card: 28px

### Shadows
- Card light: `0 8px 24px #1f3a9312`
- Card featured: `0 16px 36px #1f3a9330`
- Dark block: `0 16px 40px #05081f40`

---

## Assets

| File | Usage |
|---|---|
| `assets/hero.mp4` | Hero section background video (autoplay, muted, loop) |
| `assets/bg-workflow.png` | Dark features section background + video poster |
| `assets/contact-phone.png` | Transparent PNG phone illustration in contact block |

---

## Brief URL
All CTA buttons link to:
`https://docs.google.com/forms/d/e/1FAIpQLSfsLU10BCvi8zrXi5_aAPyzKfMKOG3e1FG6udNLLWYkIs1rWQ/viewform`

---

## Files
- `SAS Landing.dc.html` — complete prototype (open directly in browser, no build step)
- `assets/` — all referenced media files
