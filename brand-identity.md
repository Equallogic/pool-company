# Brand Identity Guide — St. Augustine Pool Co.

---

## Brand Positioning Statement

St. Augustine Pool Co. is the pool service company your neighbor already trusts — locally owned, consistently reliable, and refreshingly straightforward. We show up, we do the work, and your pool is ready for the weekend.

---

## Color Palette

Inspired by late-afternoon pool water, Florida sand, and the warm glow of a backyard evening. Avoids the generic light-blue-and-white of every other pool company. Warm, grounded, trustworthy — not corporate, not pastel.

| Name | Hex | Role | Usage Notes |
|---|---|---|---|
| **Deep Lagoon** | `#0D7377` | Primary brand color | Nav background, primary buttons, section headings, icon fills. The anchor — communicates trust, depth, and water without being light or generic. |
| **Gulf Sand** | `#F0E6CC` | Warm secondary background | Alternating section backgrounds, card fills, testimonial blocks. Gives every section a warm Florida-afternoon feel. |
| **Sunburst** | `#D4860B` | CTA / accent | "Get a Quote" buttons, star ratings, price callouts, hover highlights. Amber, not yellow — warm energy without being cheap. Use white text on top (passes WCAG AA). |
| **Palmetto** | `#4A9B7A` | Trust accent | Checkmarks, "Licensed & Insured" badges, "How It Works" step numbers, success states. Sage-green: health, nature, Florida. |
| **Driftwood** | `#2E2520` | Body text / dark | All body copy, headings on light backgrounds. Warm near-black — never cold pure `#000`. |
| **Sandshell** | `#FAF7F0` | Page background / light | Hero background, footer, nav when light variant used. Warm off-white — not stark white, not gray. |

### Contrast Notes (WCAG AA)
- Driftwood `#2E2520` on Sandshell `#FAF7F0`: ~17:1 ✓
- White `#FFFFFF` on Deep Lagoon `#0D7377`: ~7.1:1 ✓
- White `#FFFFFF` on Sunburst `#D4860B`: ~4.6:1 ✓ (use for button text only, not small body)
- White `#FFFFFF` on Palmetto `#4A9B7A`: ~4.5:1 ✓
- Driftwood `#2E2520` on Gulf Sand `#F0E6CC`: ~12:1 ✓

### Tailwind Theme Extension (for `<script>` config block)
```js
theme: {
  extend: {
    colors: {
      lagoon:    { DEFAULT: '#0D7377', dark: '#0A5C60' },
      sand:      { DEFAULT: '#F0E6CC', light: '#FAF7F0' },
      sunburst:  { DEFAULT: '#D4860B', light: '#F5A623' },
      palmetto:  { DEFAULT: '#4A9B7A', light: '#6DB89A' },
      driftwood: { DEFAULT: '#2E2520', light: '#5C4D46' },
    },
    fontFamily: {
      display: ['Nunito', 'sans-serif'],
      body:    ['Inter', 'sans-serif'],
    },
  }
}
```

---

## Typography

### Pairing: Nunito (display) + Inter (body)

**Why Nunito for headings?**
Nunito's rounded terminals give headings a warm, approachable quality — less cold than geometric sans (Montserrat, Raleway), less childish than Fredoka or Varela Round. It reads as professional but not stiff. Works exceptionally well at large display sizes. Use weights 700–800 for impact.

**Why Inter for body?**
Inter is the gold standard for UI legibility at small sizes and on mobile screens. It's neutral enough to let the content speak, reads well at 14–16px on retina and non-retina displays alike. Pairs naturally with Nunito's geometry without clashing.

### Google Fonts Import
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800;900&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
```

### Type Scale

| Level | Font | Size (mobile → desktop) | Weight | Line Height |
|---|---|---|---|---|
| Hero display | Nunito | 2.5rem → 3.75rem | 800 (ExtraBold) | 1.15 |
| H1 (section title) | Nunito | 1.875rem → 2.5rem | 700 (Bold) | 1.2 |
| H2 (card heading) | Nunito | 1.25rem → 1.5rem | 700 (Bold) | 1.3 |
| H3 (small label) | Nunito | 1rem → 1.125rem | 600 (SemiBold) | 1.4 |
| Body | Inter | 1rem (16px) | 400 | 1.65 |
| Body medium | Inter | 1rem (16px) | 500 | 1.65 |
| Small / meta | Inter | 0.875rem (14px) | 400 | 1.5 |
| CTA button | Nunito | 1rem → 1.0625rem | 700 | 1 |

> **Rule:** Never use Inter below 14px. Never use Nunito for long body paragraphs. Match.

---

## Visual Style

**In one line:** Clean, sunny, family-photo-album warm — with enough design polish to signal that these people are professional without feeling like a franchise.

### Aesthetic Principles

**Warmth over coldness.** Every surface has a hint of warmth — Sandshell instead of `#FFFFFF`, Gulf Sand instead of `#f5f5f5`, Driftwood instead of `#111`. No cold grays, no stark white sections.

**Generous breathing room.** Sections breathe. Cards have comfortable padding. Copy doesn't crowd its container. Whitespace communicates confidence — a cheap site packs everything in. This one doesn't.

**Rounded everything.** `border-radius` of `0.75rem` (12px) for cards, `0.5rem` (8px) for buttons, `1.5rem` for the hero illustration container. Rounded corners communicate approachability — the same reason Nunito works here.

**Soft elevation.** Cards lift slightly on hover with a warm shadow (`box-shadow: 0 4px 24px rgba(46, 37, 32, 0.08)`). No harsh black drop shadows. No flat no-shadow look either — find the middle ground.

**SVG illustration over photography.** No stock photos of pools. The hero uses a hand-drawn-feel SVG pool/water illustration (animated). Service icons use consistent Lucide-style SVGs at 24–28px, `1.5px` stroke, `currentColor`. Consistent stroke width across all icons.

**One accent at a time.** Don't layer Deep Lagoon backgrounds with Sunburst text and Palmetto badges all at once. Each section has one primary color temperature. The palette should feel coordinated, not loud.

---

## Voice & Tone

**How the brand talks:**

We speak in first-person plural. "We show up every Tuesday." "We handle the chemicals." "We'll let you know if something needs attention."

**Plain words only.** Not "oxidation-reduction management" — just "chemical balancing." Not "aquatic surface remediation" — just "green pool cleanup." If a homeowner on a Tuesday morning wouldn't say it, we don't say it.

**Local specifics earn trust.** "Nocatee," "Ponte Vedra Beach," "St. Johns County," "World Golf Village." Generic copy could have been written by anyone in the country. Local copy proves we're actually here.

**No fake urgency.** No "limited spots!", no "act now!", no "prices going up soon." These patterns are noise. What builds a phone call is: showing up, being clear, and letting the work speak.

**Dry, quiet confidence.** We've cleaned thousands of pools. We don't need to shout about it. A tone that's friendly but not performatively cheerful — like a contractor who's good at their job and knows it.

**Sample copy patterns:**
- ✓ "We show up every week. Same tech, same day."
- ✓ "Your pool should be the easy part of your week."
- ✓ "We'll catch a failing pump before it becomes a $1,200 problem."
- ✗ "Amazing pool service at unbeatable prices!"
- ✗ "Our team of highly trained aquatic professionals…"
- ✗ "Don't miss out — limited availability!"

---

## Logo / Name Treatment

No brand mark exists yet. Use a typeset wordmark approach.

### Primary Wordmark
```
St. Augustine Pool Co.
```
- Font: **Nunito ExtraBold (800)**
- Color: **Deep Lagoon** `#0D7377` on light backgrounds, or **Sandshell** `#FAF7F0` on dark/colored backgrounds
- Tracking: `letter-spacing: -0.01em` at large sizes, normal at small
- No all-caps. Mixed case only.

### SVG Icon Mark
A minimal wave-and-circle mark: three horizontal sine-wave lines inside a circle, rendered in Deep Lagoon. Sits to the left of the wordmark text in the nav. Should work at 32×32px in the nav and 64×64px standalone.

```svg
<!-- Suggested icon mark structure -->
<svg width="32" height="32" viewBox="0 0 32 32" fill="none">
  <circle cx="16" cy="16" r="15" stroke="#0D7377" stroke-width="1.5"/>
  <!-- Three wave lines -->
  <path d="M7 13 Q10 11 13 13 Q16 15 19 13 Q22 11 25 13" stroke="#0D7377" stroke-width="1.5" stroke-linecap="round" fill="none"/>
  <path d="M7 16 Q10 14 13 16 Q16 18 19 16 Q22 14 25 16" stroke="#0D7377" stroke-width="1.5" stroke-linecap="round" fill="none"/>
  <path d="M7 19 Q10 17 13 19 Q16 21 19 19 Q22 17 25 19" stroke="#0D7377" stroke-width="1.5" stroke-linecap="round" fill="none"/>
</svg>
```

### Context Rules
| Context | Treatment |
|---|---|
| Nav (sticky, light bg) | Icon + "St. Augustine Pool Co." in Nunito 800, Deep Lagoon |
| Nav (sticky, dark bg) | Icon + wordmark in Sandshell |
| Footer | Icon + full wordmark + tagline small text |
| Favicon | Icon mark only (circle with waves), 32×32 |
| Mobile nav (collapsed) | Icon mark only |

### Tagline (optional use in hero trust line)
> "Locally owned. Showing up every week."

---

## Anti-Patterns to Avoid

- Generic "pool blue" (`#00BFFF`, `#87CEEB`) — this palette is deliberately richer
- Corporate navy (`#1e3a5f`, `#0a2540`) — signals franchise, not local
- Stark white backgrounds — always use Sandshell or Gulf Sand
- Emoji as icons — Lucide SVGs only
- All-caps headings — Nunito in mixed case only
- Fake testimonials with stock photo avatars — use initials or first name only
- "Limited time offer" or "Book now before spots fill up" language
