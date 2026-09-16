# Design Spec — BUDT748 Three-Page Website

Everything needed to reproduce this site from scratch. Hand this file to Claude (or any developer)
and the result should match the live site at https://kpdade.github.io/budt748-website/

---

## 1. What it is

A three-page static website for the BUDT748 Fall 2026 client-side technologies assignment:
**Homepage**, **About**, **Contact**. Plain HTML and CSS with Bootstrap 5 from the CDN. No build
step, no framework, no JavaScript beyond one small form handler.

The header must display the site owner's name: **Kushaal Pelluru Lakshminarasimhan**.

## 2. File structure

```
index.html        Homepage
about.html        About page
contact.html      Contact page
css/
  styles.css      Shared styles (tokens, nav, hero, buttons, cards, footer) + homepage
  styles2.css     About page only
  styles3.css     Contact page only
images/           Exported assets (currently unused)
README.md
```

Every page loads, in this order: Bootstrap CSS (CDN) → Google Fonts (Montserrat) → `css/styles.css`
→ its own page stylesheet if it has one. Stylesheet links carry a `?v=2` version stamp so browsers
don't serve stale CSS after a redesign. Bootstrap's JS bundle loads at the end of `<body>`.

```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<link rel="stylesheet" href="css/styles.css?v=2">
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
```

## 3. Design language

Restrained and corporate: navy and slate on white, one blue accent, generous whitespace. No
gradients on text, no glow effects, no bright colors. Everything reads as a consulting or
enterprise site rather than a student portfolio.

### Color tokens (defined on `:root` in `styles.css`)

| Token | Value | Used for |
|---|---|---|
| `--navy` | `#13355c` | Buttons, logo mark, active nav, left rules |
| `--navy-deep` | `#0d2440` | Headline text, button hover |
| `--accent` | `#2f6fb0` | Eyebrows, card labels, accent half of headings, links |
| `--accent-soft` | `#eef4fa` | Badge and avatar fills, ghost-button hover |
| `--ink` | `#101a2b` | Primary text |
| `--ink-soft` | `#55647a` | Body copy, muted text |
| `--line` | `#e3e8ef` | Card borders, dividers |
| `--line-strong` | `#cfd8e4` | Input borders, ghost button border |
| `--bg` | `#ffffff` | Page background |
| `--bg-alt` | `#f6f8fb` | Top band, footer, outline cards |

Shape and motion: `--radius-lg: 16px`, `--radius-md: 10px`,
`--shadow-sm: 0 1px 2px rgba(16,26,43,.06)`, `--shadow-md: 0 12px 28px rgba(16,26,43,.10)`,
`--ease: .2s ease`.

Body background is white with `linear-gradient(180deg, var(--bg-alt) 0%, var(--bg) 420px)`,
no-repeat — a soft band behind the header area only.

### Typography

Montserrat throughout (400/500/600/700/800), line-height 1.65, antialiased.
Sizes use `clamp()` so they scale without extra breakpoints:

- Hero title — `clamp(32px, 5.8vw, 60px)`, weight 700, line-height 1.12, letter-spacing -0.8px, `--navy-deep`
- Page title (About/Contact) — `clamp(28px, 4.4vw, 46px)`, weight 700
- Section title — `clamp(22px, 2.8vw, 30px)`, weight 700
- Hero subtitle — `clamp(16px, 1.9vw, 21px)`, `--ink-soft`, max-width 720px
- Page lead — `clamp(15.5px, 1.5vw, 18px)`, `--ink-soft`, max-width 840px
- Eyebrow — 12px, weight 700, letter-spacing 2.2px, uppercase, `--accent`
- Card label — 11.5px, weight 700, letter-spacing 1.8px, uppercase, `--accent`

Headings are two-tone: the second half is wrapped in `<span class="title-accent">` and colored
`--accent`. Example: `LET'S CREATE A <span class="title-accent">WEBSITE DESIGN</span>`.

## 4. Components

### Navigation bar (identical on all three pages)

Bootstrap `navbar navbar-expand-lg navbar-light site-nav sticky-top`. Sticky, white at 88% with a
12px backdrop blur and a 1px bottom border. The brand is a flex row: a 38x38 navy rounded square
reading `KP`, then the full name at 17px bold. Links sit right (`ms-auto`) at 15px `--ink-soft`,
26px apart, and grow a 2px navy underline from width 0 to 100% on hover and on `.active`. Collapses
to a hamburger below 992px; the collapsed menu stacks links with 8px vertical padding.

### Buttons

- `.btn-cta` — navy fill, white text, min-width 180px, radius 10px, 13px/32px padding, weight 600.
  Hover: darkens to `--navy-deep`, lifts 1px, shadow deepens.
- `.btn-ghost` — white fill, `--line-strong` border, ink text. Hover: navy border, `--accent-soft` fill.
- Inside `.cta-panel` the CTA inverts to white fill with navy text.

### Cards

- `.feature-card` — white, 1px `--line`, radius 16, `--shadow-sm`, 30px/26px padding. Hover lifts 3px.
  Contains a 40x40 `--accent-soft` badge with a navy number, a 20px title, body copy, and a small
  uppercase meta line separated by a top border.
- `.detail-card` (About) — same base plus a 3px navy bar down the left edge via `::before`.
- `.outline-item` (About) — `--bg-alt` fill that turns white on hover.
- `.contact-item` (Contact) — flex row: 42px circular `--accent-soft` avatar with navy initials, then
  name and email stacked. Shifts 2px right on hover.

### Form (Contact)

Bootstrap form controls inside `.form-panel` (white card, radius 16). Fields: Name and Email side by
side (`col-md-6`), then a Subject `<select>` and a Message `<textarea>` full width. Inputs are white
with `--line-strong` borders, radius 8; focus turns the border `--accent` with a 3px
`rgba(47,111,176,.14)` ring. Submit is `.btn-cta`. Since the site is static, JS calls
`preventDefault()` and reveals a success alert telling the visitor to use the listed emails instead.

### Footer

`--bg-alt` band with a top border. Two columns on the grid: name and "BUDT748, Fall 2026" on the
left, the three page links right-aligned from 768px up.

## 5. Page content

### Homepage (`index.html`)

1. Eyebrow `BUDT748 · Fall 2026 · Client-Side Technologies`
2. Hero `LET'S CREATE A WEBSITE DESIGN` (second half accented), centered
3. Subtitle: "Today let's create a sample website design with Claude and build out its corresponding
   HTML and CSS code."
4. Buttons: `Get Started` → about.html, `Contact the team` → contact.html
5. Section "From design to deployment" with three `col-md-4` cards: **Design** (Claude Design), **Build**
   (HTML · CSS · Bootstrap), **Deploy** (Git · GitHub Pages)
6. Navy `.cta-panel`: "Built with Bootstrap 5" and a `See the course` button

### About (`about.html`)

1. Eyebrow `About the course`
2. Title `BMGT407 — Information Systems Projects` (second half accented)
3. The course paragraph: capstone for IS majors, real-world solutions for business clients, full IS
   development process, functional prototypes, careers in technology and consulting
4. Three `col-md-4` detail cards: **Semester Details** / Spring 2027 / "Capstone term";
   **Professor** / Paul T Shapiro / "Course instructor"; **Teaching Assistants** / Bharath Sreekumar,
   Caifu Lin, Sumanth Devara (as a bordered list)
5. Section "What the capstone covers" — three outline items: Discovery, Design, Prototype

### Contact (`contact.html`)

1. Eyebrow `Get in touch`, title `Contact Us` (Us accented), lead "Reach out to the course team for
   support or inquiries."
2. Left column (`col-lg-5`): **Professor Contact** — Paul T Shapiro, pshapiro@umd.edu.
   **TA Contact** — Bharath Sreekumar bsreekum@umd.edu, Caifu Lin clin0817@terpmail.umd.edu,
   Sumanth Devara sdevara@umd.edu. Each as a `.contact-item` with initials.
3. Right column (`col-lg-7`): the form panel described above.

## 6. Bootstrap usage (graded)

- Responsive navbar with `navbar-toggler` and `collapse navbar-collapse`
- 12-column grid: `container`, `row`, `col-md-4`, `col-lg-5`, `col-lg-7`, `col-md-6`, `g-4`, `h-100`
- Buttons built on `.btn`
- Form controls: `form-control`, `form-select`, `form-label`, `alert alert-success`
- Utilities: `ms-auto`, `text-center`, `text-lg-end`, `mb-0`, `d-none`

## 7. Responsive and accessibility

- `@media (max-width: 991.98px)` — collapsed menu spacing, brand name drops to 15px
- `@media (max-width: 768px)` — hero padding tightens, hero buttons go full width, card padding shrinks
- `@media (min-width: 768px)` — footer links right-align
- `@media (prefers-reduced-motion: reduce)` — all transitions off
- `:focus-visible` — 2px `--accent` outline, 3px offset
- The logo mark is `aria-hidden="true"` since the name follows it as real text

## 8. Reproducing it with Claude

Paste this into Claude Code:

> Build a three-page static website (index.html, about.html, contact.html) using HTML, CSS and
> Bootstrap 5 from the CDN, following the spec in CLAUDE-DESIGN.md exactly: the color tokens,
> typography scale, component styles, and page content described there. Put shared styles in
> css/styles.css, About-only styles in css/styles2.css, and Contact-only styles in css/styles3.css.
> The header must show "Kushaal Pelluru Lakshminarasimhan" on every page. No build step and no
> JavaScript except the contact form's preventDefault handler.

To verify a rebuild: all three pages parse with no unclosed tags, the name appears in every navbar,
every `var(--token)` used in styles2/styles3 is defined in styles.css, and Bootstrap CSS and JS load
on each page.

## 9. Deployment

Static hosting, no build. Currently GitHub Pages from the `main` branch root of
https://github.com/kpdade/budt748-website — Settings → Pages → Branch: main → / (root).
