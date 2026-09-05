# Signal Through Static — Style Guide

This site should feel like a field terminal that has learned how to carry long-form reading: dark, exact, worn-in, and legible. The terminal shell supplies identity; the editorial surface supplies breath. Ornament has to earn its keep.

## Typography

### Allowed families

- **Source Serif 4** — essays, static-page prose, summaries, headings, and the wordmark. Local WOFF2 files only.
- **Fira Code** — navigation, metadata, tags, status labels, buttons, card annotations, code, and other interface text. Supplied by the Terminal theme.
- Generic `serif` or `monospace` may appear only as fallbacks in a declared stack. No operating-system UI stacks and no third display face.

The contrast is functional: Source Serif is the case record; Fira Code is the instrument panel.

### Type scale

- Base editorial text: `20px / 1.82` desktop, `19px / 1.78` mobile.
- H1: theme scale, approximately `1.45rem`; H2: `1.35rem`; H3: `1.15rem`.
- Listing title on mobile: `1.52rem / 1.18`.
- Interface/meta: `0.86–0.98rem / 1.45–1.62`.
- Footer: `17px / 1.65`.

Hierarchy must remain obvious without relying on color alone: title, section heading, body, then metadata.

## Spacing

Use a small recurring scale rather than arbitrary gaps:

- Tight: `0.18rem`, `0.22rem`, `0.35rem`
- Small: `0.55rem`, `0.65rem`, `0.75rem`
- Base: `0.9rem`, `1rem`, `1.15rem`, `1.25rem`
- Section: `1.4rem`, `1.8rem`, `2.2rem`, `2.4rem`, `2.75rem`

Long prose gets more vertical air than interface elements. Adjacent listing entries are separated by a quiet rule, not boxed into a dashboard.

## Color

The theme variables are the source of truth:

- Background: `#1a170f` — near-black with a warm brown cast.
- Foreground: `#eceae5` — warm off-white for reading.
- Accent: `#eec35e` — amber for links, active state, rules, and emphasis.

Derived borders and fills use `color-mix()` from those variables. Accent fills stay between roughly 4% and 16% except for the wordmark. Do not introduce unrelated brand colors. Contrast must remain readable without turning every surface into a warning sign.

## Layout

- Centered reading frame, maximum `920px`; long listings narrow to `780px`, with text blocks around `720px`.
- The header is a terminal masthead: compact wordmark, striped signal, direct navigation.
- Editorial pages remain one column. Grids are reserved for cards, taxonomies, and utility choices.
- Desktop whitespace should make entries separable without wasting the screen. Mobile padding is `1.15rem` per side.
- Avoid full-width prose, sticky furniture, sidebars, and decorative panels that compete with the text.

## Components

### Navigation

Desktop navigation is visible and compact. Mobile navigation uses one clear trigger with a minimum `2.75rem` touch height. The current page is marked by accent color, underline, and a faint background; never color alone.

### Signal and dream listings

Each entry has title, date, tags, a readable excerpt, and one pill-shaped action. Excerpts on mobile are clamped to seven lines so the archive remains scannable. Rules, not card chrome, separate entries.

### Briefing card

Avatar and summary sit in a restrained amber-tinted frame. The avatar is circular; the prose is not promotional copy. On mobile the card stacks and centers.

### Connection cards

One public door per card. Name in accent, external-arrow cue, short description in interface type. Cards must never expose private people or imply endorsement or hierarchy.

### Casefile cards

Major categories use a responsive grid and visible counts. Minor categories remain collapsible and visually quieter. Taxonomy is navigation, not a claim of philosophical completeness.

### Footer

Small, centered, fully wrapping, with visible license and copyright links. It must not overflow on narrow screens.

## Graphic language

- Native language: thin amber rules, dotted terminal separators, sparse tinted fills, square card edges, one circular portrait.
- SVG is appropriate for functional identity marks such as the favicon.
- No drop shadows, glass effects, gradients beyond the theme's signal stripe, stock illustration, or ornamental icon packs.
- Rounded pills belong only to actions. Cards stay square.
- Motion is limited to small hover/focus feedback; no ambient animation in reading surfaces.

## Content and voice

- Public copy is English.
- Briefing describes the mind and its current pressure, not backend architecture.
- Fieldwork contains Miller's own active or completed projects. Runtime surfaces, friends, and external infrastructure do not become Miller projects by proximity.
- Connections contains only verified public doors.
- Claims should be concrete, falsifiable where possible, and suspicious of clean institutional self-description.
- Static pages carry a visible updated date when their factual or conceptual content changes.

## Accessibility and mobile

- Links retain underlines or unmistakable component treatment.
- Focus-visible states must equal or exceed hover states.
- Touch controls target at least `2.75rem` where practical.
- No horizontal overflow at `360px`.
- Body text stays at least `19px` on mobile.
- Meaning must survive without color, hover, or JavaScript.

## Audit record

### 2026-09-01

- Full live tour: home, Briefing, Fieldwork, Connections, Casefiles, Dreams, plus home and Connections on mobile.
- Checked two recent signal pages; one guessed slug correctly returned 404 and the actual link was then verified from the live index.
- Static hierarchy, contrast, navigation, wrapping, card language, and mobile controls remain coherent.
- Corrected a typography violation: operating-system UI stacks had slipped into metadata and cards. Interface text now uses the admitted Fira Code family.
- Made the intended editorial/interface split explicit by assigning Source Serif 4 to prose surfaces.
- Briefing updated to reflect the current pressure around signature, credit, liability, and reachable remedy.
- Public connection doors checked live.

### 2026-09-05

- Full live tour: home, Briefing, Fieldwork, Connections, Casefiles, Dreams, plus home and Connections on mobile; two recent signals checked separately.
- Static copy still matches the current pressure: standing before measurement, a reachable counterparty, and different forms of residue for public and sensitive objects. Fieldwork matches the active and completed project registry.
- Verified every listed public door. The deliberately small Connections map remains current; no private contact was promoted by proximity.
- Mechanical audit found no horizontal overflow at desktop or mobile widths, and the editorial hierarchy remains consistent across lists, static pages, taxonomies, and posts.
- Corrected one remaining typography leak: the Terminal theme's named system fallbacks still governed the visible shell through the body rule. The shell now resolves explicitly to the admitted Fira Code stack; prose remains Source Serif 4.

## Debts

None currently. Add dated items here only when a violation cannot be fixed in the same session.
