# AR Saadhana — portfolio link hub

Date: 2026-10-24
Status: approved; education order added, dark emerald visual refresh shipped

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

- Static HTML and CSS only; inline SVG icons; no JavaScript; self-hosted
  Gloock and Manrope fonts; no third-party runtime requests.
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

- Single centered glass card, max width ~28rem, on a deep warm charcoal
  background with emerald and bronze radial glows and a fine grain overlay.
- Warm ivory text; emerald carries action, focus, and atmosphere. The name is
  set in self-hosted Gloock, the UI in self-hosted Manrope.
- Monogram "AS" in a glowing emerald ring with a hover lift, where a headshot
  would go.
- Education block between the name and the links: "IIT Madras" then "CUTN",
  each with its full institution name beneath.
- Five full-width glass link rows in the order the user listed: GitHub,
  LinkedIn, Instagram, Twitter/X, email. Each row has an inline SVG icon,
  label and handle, a 1px border, hover elevation with an emerald tint, and a
  visible keyboard focus ring.
- Email row uses `mailto:`; other rows open in a new tab with `rel="noopener"`.
- Small muted footer: "© AR Saadhana".
- Mobile-first, tap targets at least 44px, contrast at or above WCAG AA,
  `prefers-reduced-motion` respected.
- Basic `<title>`, meta description, and an SVG favicon of the monogram.

The dark theme replaced the original warm-paper palette at the user's request
(bolder, glass, emerald glow, richer typography).

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

- Open locally at 360px, 390px, 1440x900, and 1440x1200; check layout, tap
  targets, and that the card fits without clipping.
- Confirm every link target and the `mailto:` address.
- Tab through the page; confirm the focus ring is visible and never clipped.
- Hover the monogram and each link; confirm the lift, tint, and arrow motion.
- Check text and icon contrast against the dark surfaces.
- Verify the deployed page at https://gojo1709satoru.github.io/.

## Left to the builder

- Exact palette, spacing, and icon stroke weight tuned during the build.
- Headshot swap and optional tagline when the user has them.
