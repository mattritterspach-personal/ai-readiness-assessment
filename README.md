# AI Readiness Assessment

An interactive, self-scoring AI readiness assessment tool for business leaders — built as a lead generation and consulting qualification tool for [Agosto Capital](https://agostocapital.io).

**Live tool:** [mattritterspach.com/ai-assessment](https://mattritterspach.com/ai-assessment) *(embed URL — see below)*

---

## What It Does

Visitors answer 12 questions across three dimensions:

1. **Data Infrastructure** — Data quality, accessibility, and integration
2. **Team Capabilities** — AI/ML talent, digital fluency, and tooling
3. **Organizational Culture** — Leadership buy-in, experimentation mindset, and change readiness

The tool calculates a 0–100 score, assigns a tier (Foundations Needed / Building Momentum / Ready to Scale / AI Leader), generates personalized recommendations, and emails a report to both the respondent and the consulting inbox.

---

## Tiers

| Score | Tier | Description |
|-------|------|-------------|
| 0–25 | Foundations Needed | Focus on data infrastructure before AI investment |
| 26–50 | Building Momentum | Ready for targeted pilots in 1–2 areas |
| 51–75 | Ready to Scale | Positioned to move into production AI within 3–6 months |
| 76–100 | AI Leader | Positioned to use AI as a genuine competitive differentiator |

---

## Technical Details

- **Single-file HTML** — no build step, no dependencies except EmailJS
- **EmailJS** for client-side email delivery (no server required)
- Dark theme with gold accents (#c9a84c) matching the Matt Ritterspach brand
- Animated SVG score ring + dimension breakdown bars
- Mobile-responsive

### EmailJS Setup

Replace the three placeholders in `index.html` before deploying:

```js
const EMAILJS_PUBLIC_KEY  = 'YOUR_PUBLIC_KEY';   // from emailjs.com > Account
const EMAILJS_SERVICE_ID  = 'YOUR_SERVICE_ID';   // from Email Services tab
const EMAILJS_TEMPLATE_ID = 'YOUR_TEMPLATE_ID';  // from Email Templates tab
```

Template variables expected:
`to_name`, `to_email`, `company`, `score`, `tier`, `title`, `data_score`, `team_score`, `org_score`, `rec_1`, `rec_2`, `rec_3`, `consulting_email`

---

## Embedding on Squarespace

1. Add a **Code Block** or **Embed Block** to your page
2. Use an `<iframe>` pointing to the GitHub Pages URL:

```html
<iframe
  src="https://mattritterspach-personal.github.io/ai-readiness-assessment/"
  width="100%"
  height="900"
  frameborder="0"
  style="border:none; border-radius:8px;"
></iframe>
```

Or host `index.html` directly on your domain and link to it.

---

## License

MIT
