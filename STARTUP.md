# Faculty Website — Session Startup Guide

## What This Is
A personal faculty homepage for Brooks Depro, Associate Professor of Economics at Elon University.
Replaces a Google Sites page. Hosted as static HTML on GitHub Pages.

**Local preview server:** `http://localhost:3002`
Launch config: `C:\Users\bdepro\.claude\launch.json` — server name `faculty-site`, port 3002, serves `repos/faculty/`.

---

## File Structure

```
repos/faculty/
├── index.html          — Homepage (hero, about, research, recent pubs, course cards)
├── teaching.html       — Full teaching page (course cards + philosophy + selected pubs)
├── publications.html   — All 17 publications grouped by year with type labels
├── banner.jpg          — Marine Corps honor guard photo (hero left panel)
├── 09_06_2023_Brooks Depro.jpg  — Headshot (circular, overlaps hero/identity strip)
├── STARTUP.md          — This file
└── google-site/        — Original Google Sites export (files only, not design)
```

---

## Design System

**Palette** — drawn from Marine dress blues in the banner photo:
| Variable | Value | Use |
|---|---|---|
| `--navy` | `#1a2744` | Primary color |
| `--navy-dk` | `#111b30` | Nav bar, hero panel background |
| `--gold` | `#c9a535` | Accent, borders, year tags |
| `--gold-link` | `#8a6e1a` | Link color |
| `--cream` | `#f9f8f5` | Page background |

**Fonts:** Source Serif 4 (headings) + Inter (body) — *faculty site only*
**Note:** Course sites all use Roboto. Faculty site intentionally uses a different, more personal type system.

**Hero layout:** Split — left half is `banner.jpg` (Marines photo, full visibility), right 42% is navy panel with name, title, and keyword chips.

**Identity strip:** White bar below hero. Circular headshot (`110px`) overlaps upward into the hero by `52px`. Contact info + external profile links (LinkedIn, Google Scholar, Elon Directory).

**Two-column body:** Main content (left, `1fr`) + sidebar (right, `270px`). Collapses to single column on mobile ≤700px.

---

## Content

### About / Bio
Uses the exact text from Brooks's Google Sites bio with links preserved:
- RTI International link
- B.S.B.A. Business Economics & Consulting program link
- PPE minor link
- Three in-text publication links
- Dean's Award mention

### Research Interests
Summary paragraph + 8 keyword chips: Environmental Justice, Residential Mobility, Pollution Policy, Labor Markets, Economics Education, Active Learning, Case-Based Pedagogy, Academic Mindset.

### Teaching (homepage shows 4 cards, full page at teaching.html)
| Code | Title | Link |
|---|---|---|
| ECO 1000 | Principles of Economics | bdepro.github.io/courses/eco1000-cengage/ |
| MBA 6250 | Essential Economics for Strategic Management | bdepro.github.io/courses/mba6250/ |
| ECO 4400 | Applied Economics & Consulting | bdepro.github.io/courses/eco4400/ |
| COR 1100 | The Global Experience | bdepro.github.io/courses/cor1100/ |

### Publications
All 17 publications in **Chicago Author-Date** format with HTML links.
Homepage shows 5 most recent with "View all 17 →" link to `publications.html`.
Full list in `publications.html` grouped by year (2026 → 2006) with type labels (Journal Article / Report / Book Chapter).

---

## External Profile Links
All links use real URLs:
- LinkedIn: `https://www.linkedin.com/in/brooksdepro/`
- Google Scholar: `https://scholar.google.com/citations?hl=en&user=ppmDzDgAAAAJ`
- Elon Directory: `https://www.elon.edu/u/directory/profile/bdepro/`

---

## Sidebar (all three pages)
- **Contact:** email, phone (336) 278-6883, Koury Business Center 122 / 2075 Campus Box / Elon NC 27244
- **Profiles:** LinkedIn, Google Scholar, Elon Faculty Profile
- **Recognition & Service:** Dean's Award, BSBA advisor, COA advocate, PPE board, USMC veteran

---

## Pending / Known Issues
- The preview screenshot tool has been unreliable this session — use browser at localhost:3002 directly
- About section text may be centering on some viewports — investigate layout bug

---

## Related Course Sites
All in `repos/courses/` — each has its own `config.js` as single source of truth for titles/dates.
| Course | Font | Title in config.js |
|---|---|---|
| ECO 1000 | Roboto | "Principles of Economics" |
| MBA 6250 | Roboto (updated this session) | "Essential Economics for Strategic Management" |
| ECO 4400 | Roboto | "Applied Economics & Consulting" |
| COR 1100 | Roboto via shared/brand.css | "The Global Experience" |

---

## GitHub Pages Plan (not yet done)
- Create repo named `bdepro.github.io` (or a subdirectory repo)
- Push `repos/faculty/` contents to root
- Enable GitHub Pages in repo Settings → Pages → main branch / root
- Update DNS if using a custom domain
