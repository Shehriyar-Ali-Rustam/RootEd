# RootEd — landing page

Pre-launch landing page for **RootEd**, a Matric (Grades 9–10) learning platform for Pakistan that
pairs board-aligned lessons with vetted university-student tutors.

_Grow where you are planted._

## Status

Pre-launch. This page exists to do one job: find out whether students, parents and prospective
tutors actually want this, and collect their contact details while they are interested.

Nothing on the page claims traction. There are no user counts, no ratings, no launch date, and the
three tutor cards are clearly marked as examples until real vetted tutors replace them.

## What's here

A single static `index.html`. No build step, no dependencies, no framework.

```
index.html    the whole page — markup, styles and script inline
```

Run it locally by opening the file, or:

```bash
python3 -m http.server 8000     # then visit http://localhost:8000
```

## Deploying

Any static host works. Push to `main` and the host rebuilds.

| Host | Notes |
| --- | --- |
| **Cloudflare Pages** | Free tier permits commercial use, unlimited bandwidth. Recommended once payments start. |
| **Vercel** | Best DX. Hobby tier is non-commercial — move to Cloudflare or Vercel Pro before taking money. |
| **GitHub Pages** | Works, since the site is fully static. |

No build command. Output directory is the repo root.

## Design system

Defined as CSS custom properties at the top of `index.html`.

| Token | Value | Role |
| --- | --- | --- |
| `--root` | `#174d3a` | Primary brand green, CTAs |
| `--forest` | `#0e3125` | The single dark anchor panel, footer |
| `--sage` | `#a7bfa9` | Soft accents, text on forest |
| `--brass` | `#8f6216` | Sparingly — passes AA on white |
| `--ink` | `#152520` | Body text |
| `--mist` | `#f3f7f4` | Secondary surface (green-biased, deliberately not cream) |

Type: **Literata** for display (a face designed for reading, not a fashion serif), **Figtree** for UI,
**DM Mono** for chapter codes and labels.

The page commits to a light theme by design.

## Copy rules

These come from the business plan and are not stylistic preferences:

- No "Pakistan's first" or "#1" — competitors predate us
- No invented user counts, ratings or testimonials
- Never describe tutors as *certified teachers* — they are vetted university students
- No guaranteed marks or results
- No identifiable minor in imagery without guardian consent

## Known gaps

- [ ] The signup form validates and shows a success state, but does not persist anywhere yet
- [ ] Tutor cards hold example data pending the first three vetted tutors
- [ ] No `og:image` — needs a 1200×630 card for WhatsApp and social previews
- [ ] Urdu translation not started; layout is ready for it
- [ ] Launch board and subject still undecided (decisions D1/D2 in the business plan)
