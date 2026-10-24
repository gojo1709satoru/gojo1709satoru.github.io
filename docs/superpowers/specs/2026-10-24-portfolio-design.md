# AR Saadhana — portfolio link hub

Date: 2026-10-24
Status: approved; education order added at the user's request

## Intent

A single page that gathers AR Saadhana's public profiles in one place, so a
visitor can find and contact them in one click. It should feel deliberate and
professional even before a headshot exists.

## Goals

- Show the name, a monogram, education, and five links: GitHub, LinkedIn,
  Instagram, Twitter/X, email.
- Load fast, work on any phone, need no build step.
- Replace the monogram with a real headshot later without redesigning.

## Non-goals

- No project showcase, blog, or long bio in v1.
- No AmbitionBox link (private profile) and no second email address.
- No contact form, backend, analytics, or tracking.
- No dark/light theme toggle in v1.

## Constraints

- Static HTML and CSS only; inline SVG icons; no JavaScript; no external fonts
  or requests.
- Deployable to GitHub Pages as-is.
- Photo: initials monogram until a headshot is supplied.

## Approaches considered

1. **Plain static page — chosen.** One `index.html` plus `styles.css`. The
   smallest thing that fully does the job; zero tooling, trivial hosting.
2. **Astro or Next static site.** Adds a build step, dependencies, and project
   structure for what is five links and a name. Rejected as overkill.
3. **Linktree/Carrd page.** Fastest to publish, but limited control over
   branding and an external dependency. Rejected.

## The page (my calls)

- Single centered column, max width ~26rem, on a warm off-white background.
- Ink-colored text; one emerald accent. Name set in a serif, links in the
  system sans stack.
- Monogram "AS" in a thin emerald ring where a headshot would go.
- Education block between the name and the links: "IIT Madras" then "CUTN",
  each with its full institution name beneath.
- Five full-width link rows in the order the user listed: GitHub, LinkedIn,
  Instagram, Twitter/X, email. Each row has an inline SVG icon, label, 1px
  border, hover lift, and a visible keyboard focus ring.
- Email row uses `mailto:`; other rows open in a new tab with `rel="noopener"`.
- Small muted footer: "© AR Saadhana".
- Mobile-first, tap targets at least 44px, contrast at or above WCAG AA,
  `prefers-reduced-motion` respected.
- Basic `<title>`, meta description, and an SVG favicon of the monogram.

## Content

| Label     | Target                                        |
| --------- | --------------------------------------------- |
| GitHub    | https://github.com/gojo1709satoru              |
| LinkedIn  | https://www.linkedin.com/in/a-r-saadhana       |
| Instagram | https://instagram.com/cosmic_chaos17_          |
| Twitter/X | https://x.com/Gojo1709satoru                   |
| Email     | mailto:gojo1709satoru@gmail.com                |

Education, top to bottom:

1. IIT Madras — Indian Institute of Technology Madras
2. CUTN — Central University of Tamil Nadu

Name displayed: AR Saadhana. No tagline in v1.

## Verification

- Open locally at 360px and 1440px widths; check layout and tap targets.
- Confirm every link target and the `mailto:` address.
- Tab through the page; confirm focus is always visible.
- Check text contrast with a contrast checker.

## Left to the builder

- Exact palette, spacing, and icon stroke weight tuned during the build.
- Headshot swap and optional tagline when the user has them.
