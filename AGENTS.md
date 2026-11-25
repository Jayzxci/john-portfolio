# Portfolio: John Benitez, video editor and AI UGC creator

## Stack
Astro + Tailwind + TypeScript. Static output only. No backend, no database.

## Design (inspired by bryllim.com; match screenshots in /reference)
- Desktop: two columns. Left panel is sticky: name, one-line role, nav, "Email me" button, theme toggle. Main column max 680px.
- Mobile: single column, panel becomes the header, sticky "Hire me" bar at the bottom.
- Light bg #f7f7f2, dark bg #151513. One link-blue accent. One typeface (Geist) with a system fallback.
- Hairline dividers, radius 6px max, generous spacing, left-aligned text.
- Never: gradients, glow, glassmorphism, card shadows, emoji icons, stock illustrations, all-caps labels, numbered sections (except the process list), "→" on buttons.
- Motion: none by default. Only theme toggle and video hover/in-view play.
- Light and dark mode via prefers-color-scheme plus a manual toggle.

## Sections (in order)
Intro and showreel, Featured (3 AI ads), Work (filter: AI ads, AI drama, Reels, Shorts), About, Services (quote on request, no prices), Process, Experience, Certifications, FAQ, Start a project (brief form that opens a mailto draft), Contact.

## Videos
- Data lives in src/data/work.ts (title, category, url, optional clip, poster, youtubeId).
- Cards use a poster and preload="none". Previews are muted, looped, playsinline, and play only in view. Max 2 playing at once.
- Full videos open in a modal with a youtube-nocookie facade (thumbnail first, player loads on click). Fall back to the Drive url if no youtubeId.

## Email
- Every video has "Email about this": mailto with subject "Video inquiry: <title>" and a short body (platform, length, deadline, budget).
- Email: johnemmealesbenitez@gmail.com. Also a "Copy email" button.

## Content rules
- Use only facts from the resume. Never invent testimonials, prices, or results.
- Label AI-generated work as AI. Sentence case. Plain, specific copy.

## Quality
Mobile-first, visible keyboard focus, reduced motion respected, Lighthouse mobile 90+, OG tags and Person JSON-LD.

## Commands
npm run dev | npm run build | npm run preview
