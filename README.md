# Talent & Workforce · Stakeholder Redteaming Dashboard

A self-contained, single-file policy dashboard built for a **Talent & Workforce Subcommittee**. It helps staff anticipate which stakeholder groups have concerns about each of six policy recommendations, ranked by grievance intensity, with tailored engagement strategies.

## What it does

- **6 policy recommendation tabs** — Community upskilling, PK–13 education, Credentialling, Pipeline to workforce, UE & reemployment, Private sector partnership
- **Stakeholder cards** sorted by grievance intensity (highest → lowest), filterable by stance (Against / Neutral / Pro)
- **Slide-in detail panel** on card click — shows what each stakeholder cares about, their core grievance, and how to engage them
- **Stakeholder overview tab** — a full grid of every stakeholder across all recommendations, with non-negotiables derived from their stated priorities

## Built by

**Duke University — Stakeholders & Science Policy course**

- Jon Crucitti
- Angie Feng
- Victoria Lanier
- Celine Yang

## Single source of truth

All content lives in the `stakeholders` object near the top of the `<script>` block in `index.html`. To add, edit, or remove a stakeholder, update that object only — the entire UI renders from it.

Each stakeholder entry has the shape:

```js
{
  name:      'Stakeholder name',
  stance:    'against' | 'neutral' | 'pro',
  intensity: 0–100,          // grievance intensity score
  oneliner:  'One-sentence summary shown on the card.',
  cares:     'What they fundamentally care about.',
  grievance: 'Their specific concern with this recommendation.',
  engage:    'Concrete strategies for productive engagement.',
}
```

## Deployment

No build step, no CDN, no dependencies. Deploy by pushing `index.html` to any static host.

For GitHub Pages, see the step-by-step instructions below (or in the repo description).
