# The Batcave — Hrithik Patil's Interactive Portfolio

An illustrated, interactive portfolio built as a single self-contained web page.
No framework, no build step, no external image or audio assets — every visual
is hand-built SVG/CSS, and the ambient score is generated live in-browser with
the Web Audio API (three detuned oscillators, not an audio file).

## What's in this project

```
batcave-portfolio/
├── index.html      ← the entire site: HTML, CSS and JavaScript in one file
├── package.json    ← optional convenience script for local preview
└── README.md       ← this file
```

There is no separate CSS file, JS bundle, image folder, or audio folder,
because the project doesn't use any — everything is inline in `index.html`.
That's intentional: it keeps the whole site portable as one file with zero
dependencies.

## Running it locally

You don't need Node, npm, or a build step. Either:

**Option A — just open it**
Double-click `index.html`, or drag it into a browser tab.

**Option B — serve it (recommended for the clipboard/share features,**
**which some browsers restrict on the `file://` protocol)**
```bash
npx serve .
```
Then open the local URL it prints (usually `http://localhost:3000`).

`package.json` only wires up that one convenience script — there's nothing
to `npm install`.

## Features

- 8 illustrated rooms (About, Projects, Education, Experience,
  Certifications, Skills, Resume, Contact) built as one continuous
  illustrated structure, not cards
- Clickable environmental hotspots with an exploration tracker and a
  downloadable "fully explored" badge
- A hidden Batcomputer-style terminal (icon in the top bar) with its own
  command set
- A secret arrow-key input sequence hidden on the page
- An **Identity Configurator** — a customizable, original guardian-style
  avatar (cowl style, suit material, cape style, emblem, lens style, belt,
  accessory) with a live SVG preview, opened from the top bar and saved to
  `localStorage` so it persists across visits
- Parallax tilt, ambient dust/flyby animation, a live Mumbai clock, a
  generative ambient score toggle, and full `prefers-reduced-motion` support
- A separate, distinctly-written downloadable resume file (not a copy of
  the PDF resume — its own document)

## Notes on the avatar feature

The Identity Configurator renders an original, abstract character — a
stylized cowl-and-cape silhouette built from geometric shapes — not a
depiction of any existing copyrighted character. All emblem variants
(chevron, diamond, arrow) are original abstract marks designed for this
project.

## Browser storage used

Everything persisted (avatar config, exploration progress, visited rooms,
a session ID, achievement flags, the "have you visited before" flag) is
stored in `localStorage`, scoped to whichever browser opens the page. None
of it is sent anywhere — there is no backend.

## Deploy checklist
- **Site URL:** meta tags, canonical, sitemap and robots assume `https://hrithikk21.github.io/batcave-portfolio/`.
  If your repo/site lives elsewhere, find-and-replace that URL in `index.html`, `sitemap.xml` and `robots.txt`.
- **Link preview image:** `og-image.png` (1200x630). Test with LinkedIn Post Inspector / opengraph.xyz after deploying;
  platforms cache previews, so re-scrape after changes.
- **Analytics:** free GoatCounter. Sign up, then set `GOATCOUNTER_CODE` at the top of the script in `index.html`.
  Until then nothing loads. Tracks page views, room opens, resume download/view, terminal use, project link clicks.
- **Music:** add `music/theme.mp3` or `theme.ogg`. **Resume:** replace `resume/Hrithik_Patil_Resume.pdf`.
