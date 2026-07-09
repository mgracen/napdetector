# NAPDetector

**Are your local business listings correct?**

Scan all of your listings across Google, Yelp, Apple Maps and Bing and fix the errors in your name, address, phone, website, hours of operation and more. Clean up your listings to get a major boost in rankings, traffic and sales.

Live app: https://mgracen.github.io/napdetector

---

## What it does

NAPDetector audits NAP (Name, Address, Phone) consistency across the four major local listing platforms for every location you own. It flags discrepancies, scores each location, generates JSON-LD schema markup, and exports a CSV fix list you can hand to your team.

**Platforms checked:**
- Google Business Profile
- Apple Maps
- Yelp
- Bing Places

**What you get per audit:**
- Platform-by-platform comparison of name, address, phone, website, hours, category
- Critical issues vs warnings
- NAP score per location (0-100)
- Review ratings snapshot across platforms
- JSON-LD schema output (full or essential)
- CSV export of all discrepancies

---

## Status

| Phase | Status |
|---|---|
| Frontend - hero, copy, UI | Done |
| API key prompt (localStorage) | Done |
| Simulated audit via Anthropic API | Done |
| GitHub Pages deployment | Done |
| DataForSEO integration (real listing data) | In progress |
| Railway backend | Planned |
| Real-time listing data | Planned |

---

## How to use

1. Open the app at the live URL above
2. Enter your Anthropic API key when prompted (stored in your browser only, never shared)
3. Add locations manually or import via CSV
4. Click Run Audit
5. Review results in the Audit, Issues, Schema, and Export tabs

**CSV import format:**
```
name, category, address, city, state, zip, phone, website, hours
```

---

## Tech stack

| Layer | Tool |
|---|---|
| Frontend | Single HTML file, vanilla JS |
| Hosting | GitHub Pages |
| Audit engine (current) | Anthropic API (claude-sonnet-4-6) |
| Listing data (planned) | DataForSEO |
| Backend (planned) | Railway |

---

## Roadmap

- [ ] DataForSEO integration for real listing data
- [ ] Railway backend to handle API calls server-side
- [ ] Persistent location storage (currently session only)
- [ ] PDF report output for client deliverables
- [ ] White-label mode for agency use

---

## Notes

- Audit results are currently **simulated** by Claude based on the business info you enter. Real listing data via DataForSEO is next.
- Your Anthropic API key is stored in localStorage and sent directly to Anthropic. It never touches any other server.
- Each audit call uses approximately 1,500 tokens. At standard Anthropic pricing this is well under $0.01 per location.
