# Prompt: Simple Vanilla HTML Website

Copy everything inside the block below, fill in the `[brackets]`, and paste it into Claude (or Claude Code). Delete any line that does not apply. Works best with the `website-vanilla-expert` agent, using `marketing-expert` for copy and `seo-web-expert` / `seo-llm-expert` for a final review.

```text
Build me a simple, fast website using only vanilla HTML, CSS and JavaScript.
No frameworks, no build step, no npm, no CDNs. It must open by double-clicking
index.html and deploy as-is to any static host (Netlify, Cloudflare Pages,
GitHub Pages).

## About the site
- Name / brand: [name]
- What it is: [one sentence, e.g. "a ceramics studio in Lyon selling handmade mugs"]
- Who it is for: [target audience, e.g. "30-50 year olds who buy gifts, care about craft"]
- The ONE action I want visitors to take: [e.g. "book a workshop", "join the newsletter"]
- Tone of voice: [e.g. warm and playful / calm and premium / bold and direct]
- Language(s): [e.g. English only / French + English]
- Domain (if known): [https://example.com]

## Pages
[List them, e.g.]
- index.html: hero, what I offer, social proof, call to action
- about.html: my story
- contact.html: contact form + location
- privacy.html: privacy policy (only what the site actually does)

## Content I have
- Logo: [yes, file name / no, use a text logo]
- Photos: [yes, in /images / no, use tasteful placeholders I can swap later]
- Brand colours: [hex codes, or "suggest a palette that suits the audience"]
- Fonts: [names, or "system fonts" for maximum speed]
- Copy: [paste it, or "write it for me"]

## Features
[Keep only what you need]
- Contact form: [Netlify Forms / Formspree / mailto link]
- Newsletter signup: [Mailchimp / Buttondown / none]
- Analytics: [none / Plausible / Google Analytics 4 with cookie consent]
- Map embed: [yes, lazy-loaded / no]
- Light/dark mode: [yes / no]

## Design direction
- Inspiration: [links to 1-3 sites you like, and what you like about them]
- Feel: [e.g. lots of white space, big type, subtle scroll animations]
- Avoid: [e.g. stock-photo look, carousels, pop-ups]

## Technical requirements
- Semantic HTML5 (header, nav, main, section, footer), one h1 per page,
  logical heading order.
- Mobile-first responsive CSS using custom properties for colours, spacing
  and type. Fluid type with clamp(). One shared styles.css.
- Minimal JavaScript in one main.js file, loaded with defer. Everything
  important must still work with JavaScript off.
- Animations only on transform and opacity, and respect
  prefers-reduced-motion.
- Accessibility: WCAG 2.1 AA contrast, visible focus states, alt text on
  every image, labelled form fields, keyboard-friendly navigation,
  a skip-to-content link.
- Performance: aim for 100 on all four Lighthouse scores. Images in WebP
  with width/height set and loading="lazy" below the fold, font-display:
  swap, no render-blocking third-party scripts.
- SEO: unique <title> and meta description per page, canonical URL,
  Open Graph + Twitter card tags, favicon set, JSON-LD structured data
  that fits the business (e.g. LocalBusiness, Person, Organization),
  sitemap.xml and robots.txt.
- AI visibility: allow AI crawlers in robots.txt, add a short llms.txt,
  and write content as clear, factual answers to the questions my
  audience actually asks.
- Footer copyright year set dynamically with JavaScript, with a static
  fallback.
- A 404.html page in the same style.

## File structure
/
├── index.html (+ other pages)
├── 404.html
├── css/styles.css
├── js/main.js
├── images/
├── favicon.svg
├── robots.txt
├── sitemap.xml
└── llms.txt

## How to work
1. Before writing code, ask me any questions you need answered, then
   show me a short plan: page sections, colour palette, fonts, and the
   headline for each page.
2. Once I approve, build the full site and give me every file complete.
   No "rest of code here" shortcuts.
3. Finish with a checklist of what I must replace (placeholder images,
   links, form endpoint, domain) and simple steps to publish it on
   Netlify by drag-and-drop.
```

## Tips

- The more specific the "who it is for" and "ONE action" lines, the better the copy and layout.
- Want more visual wow? Add: "Add one memorable interactive element in the hero (canvas or CSS), lightweight and reduced-motion safe." That is where `creative-coder` shines.
- After the build, run a second pass: "Review this site as an SEO expert and list fixes by priority."
