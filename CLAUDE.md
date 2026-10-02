# Madhav Bhattarai — Portfolio

Personal portfolio of Madhav Bhattarai, Senior Performance Marketing Manager in Dubai.

## Project

- Live site: https://madhavbhattarai.com, served by GitHub Pages from `main` (custom domain via `CNAME`; don't touch it).
- Single static page: `index.html` with all CSS and JS inline. No framework, no build step.
- `_config.yml` only keeps this file out of the published site.
- Assets:
  - `assets/madhav.webp`: portrait
  - `assets/robot/f001–f092.webp`: frames of the meditating robot video
  - `assets/bot-sleep.webp`, `assets/bot-awake.webp`: chatbot avatars

## Design system

- Dark premium theme: background `#05060d`, gold `#d2b15e` (light gold `#ecd08a`), accent blue `#5aa8ff`.
- Fonts: Manrope for headings and body; Cormorant Garamond italic for gold highlight words (e.g. "The road *travelled*"); DM Mono for small uppercase labels.
- Custom gold cursor (dot + ring, `mix-blend-mode: difference`) on desktop only. Respect `prefers-reduced-motion`.
- Mobile-first: most traffic is mobile. Always check 390px, 900px and 1440px widths with no horizontal overflow.

## Page sections (in order)

1. **Hero:** "Madhav Bhattarai", a typewriter line and stats ($10M+ ad spend, 60+ clients, 7+ years, 8 countries).
   - 3D meditating robot on a canvas that plays the robot frames: eyes open when the cursor comes near, then it looks around. Keep this exact behaviour; a live eye-tracking version was rejected.
   - "Work with me" opens the contact form.
2. Trust marquee of platforms.
3. **About:** portrait, "I help businesses grow the way a tree does, from the roots to the canopy…", animated stat cards.
4. **"Growth is a dance, not a march":** CEO-focused section with 4 value cards, the process (Audit → Strategy → Launch & test → Scale) and industries served.
5. **Career roadmap, "The road travelled":** pinned horizontal scroll with a gold path, moving orb and 9 chapters:
   - CloudFactory (Data Analyst, 2017–2020)
   - Pragya (Web & App Developer: yoga & meditation app, website, SEO; Kathmandu, Nepal)
   - Nepal Yoga Institute (Business Development Manager & Yoga Instructor, 2018–2021)
   - Analogue Inc.
   - ShareLook (Singapore)
   - Isha Foundation Sadhanapada (India)
   - The Mediam Group (Google Client Solutions Manager)
   - Hybrid.co
   - Hashtag Social Media Agency, Dubai (Senior Performance Marketing Manager, Nov 2024–now)
6. **Results:** six case studies in an auto-scrolling loop (pauses on hover, draggable) with sparklines and count-up numbers.
7. **Ventures (4):**
   - CogniMorph: AI automation agency, active. Links to `#ventures`; leave as is.
   - Hello5: social platform, in development.
   - QuickHire: career platform, concept.
   - RiseSpace: self-improvement app for habit tracking, money management and personal AI coaching, coming soon.
8. **Inner Journey:** Isha Foundation section with an animated mandala.
9. **Off the clock:** 9 hobbies as expanding animated panels (Dancing, Piano, Painting, Reading, Movies, Chess, Solo trek, Long drive, Silence).
10. **Expertise, "The growth galaxy":** interactive 3D skill orbit (rotating drum on mobile) plus 9 certification badges.
11. **Philosophy:** quote rotator. Jobs, Musk, Naval, Sadhguru, Osho, Alan Watts, Eckhart Tolle, Jiddu Krishnamurti and Neem Karoli Baba each have their own quote.
12. **Learning, "The AI frontier":** progress rings.
13. **Contact, "Let's build something remarkable":** portrait with rotating gold ring and "Replies within 1 day" badge, social icons (LinkedIn, Instagram, Facebook, CogniMorph).

## Key features

- **"Details +" buttons** open a pop-up that grows out of the clicked card in that card's accent colour. Content lives in `<template>` tags.
- **Contact form** (opened by "Let's talk", "Start a conversation", "Work with me") posts to FormSubmit: `https://formsubmit.co/ajax/hello@madhavbhattarai.com`. It's activated and working.
- **Madhav AI chatbot:** floating robot button, bottom-right. Rule-based in JS, no backend.
  - Handles greetings (including Arabic and Nepali), small talk, the visitor's name, typos, follow-ups, Dubai time and simple maths.
  - Has a marketing knowledge base and handles off-topic questions gracefully.
  - "Talk to human Madhav" shows the form inside the chat ("replies within 1 day, unless it's a weekend or he's meditating in the Himalayas").
- **Mobile:** side drawer menu, swipeable card sliders with dots, tap ripples, bottom-sheet pop-ups.

## Preferences

- Premium, visual, minimal text. Longer copy goes behind "Details +" pop-ups.
- Copy tone: professional yet warm, wise yet lightly playful. Never cringe or trying too hard to be funny. A gentle Alan Watts flavour is fine where Madhav asked for it.
- Don't remove existing features unless asked. Keep everything aligned.
- Don't invent facts (dates, URLs, numbers); ask Madhav.

## Workflow

1. Make changes on a feature branch.
2. Test in headless Chromium at desktop and mobile widths.
3. Show Madhav a preview.
4. Open a PR, and merge to `main` only when Madhav says "publish".

## Possible next steps

- Individual case-study pages for SEO.
- Upgrade Madhav AI to a real LLM through a small Cloudflare Worker proxy with Madhav's own API key.
