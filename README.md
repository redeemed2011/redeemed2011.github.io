# AI projects portfolio

A one-page static site listing Sam Beckwith III's AI projects, served by GitHub Pages at https://redeemed2011.github.io/ from the `master` branch. The URL never changes. An update is a commit and push to `master`, and GitHub Pages republishes it in a minute or two. There is no custom domain.

## Conventions

### File layout

- `index.html`: the main page. CSS is inline in a `<style>` block, and two small inline scripts run the phone menu, the active nav link, and the section-header and diagram animations.
- `approach/index.html`: the "Start from the goal" article, linked as "My approach". It repeats the same inline CSS and menu script.
- `images/`: every screenshot on the page, plus `og-image.png`, the link preview. There are no `css/` or `js/` folders.
- `README.md`: this file.

### Build step

None. The repo is plain HTML and CSS served as is, with no framework, package manager, or generated files. Fonts load from Google Fonts. Do not add a dependency or a build tool.

### Design

The current design is round-8 v9: a dark terminal style with orange accents, dim orange `>` markers before card meta lines, bracketed section headers such as `[ Full-time work ]` with a rule after them, rounded mono stack chips, and a thin rule between cards. New sections and images should match it.

### Section order

1. Header: name, role, LinkedIn and GitHub buttons, "12+ years in SRE and platform engineering", the one-line hero, a short intro, and highlight tiles (Ticket to PR, Team-trusted, 3x, 6x).
2. My approach: a short pull quote that links to `approach/`.
3. Full-time work, newest first. No employer names, code, or screenshots.
4. Side projects.
5. Personal projects.
6. Open source.
7. Models.
8. Stack, as grouped chips. Never skill bars or percentages.
9. Footer: the screenshot note, LinkedIn and GitHub links, and the "Updated" month.

### Card structure

Every project card (`article.card`) uses these parts, in this order, skipping any it doesn't have:

1. Meta line (`.meta`): a dim orange `>`, the area name, and the year range, for example "> Kubernetes Reliability · 2024–present".
2. Title (`h3`).
3. Headline result (`.lead`): one outcome-first sentence.
4. Numbers (`.facts`): real numbers only. If there are none, leave it out.
5. Screenshots or a diagram, if the card has one.
6. "What it does" and "Why it matters": short bullet lists.
7. Stack chips (`.chips`), 3 to 7 per card.

Keep the copy plain and concrete, and lead with the outcome, then how it works. No hype words, no "passionate" bio. Side and personal projects say Sam designed and built them. Full-time cards may say Sam designed, led, and built the work: he owned it end to end and implemented it himself, with co-workers supporting (Sam, 2026-10-27). Never say "directed". Don't list work that is still in development. Use real numbers only. No tables anywhere. The page is phone-first: check it at 390px, and it must not scroll sideways.

### Image rules

- Screenshots are made-up sample data, never real records. Rebuild the page with invented entries, replace every private field with placeholder blocks before rendering, then blur those spots so nothing can be recovered.
- Fields that must be replaced or blurred: pay and prices, company and employer names, recruiter and people names, shelter, rescue, breeder and seller names, addresses and locations, phone numbers, emails, and contact details.
- A real listing's photo is never used. An example listing photo must be a licensed stock photo placed inside the sample screenshot, with its credit in that screenshot's caption. `dog-search-1.png` uses "Black Labrador Pup" by John Schanlaub (CC BY 3.0, https://commons.wikimedia.org/wiki/File:Black_Labrador_Pup.jpg), cropped to fill the photo spot.
- Size: render at a 430px-wide viewport at 2× scale, which gives 860px-wide PNGs. Crop to one readable section at a time, about 600 to 1,000px tall, with a clean edge and no cut-off lines of text.
- Where they live: every screenshot is a PNG in `images/`, named after its project with a number (for example `job-pipeline-2.png`). A replacement for a live image gets a suffix such as `-r6`. Today they are 860px wide and 710 to 2,052px tall, from 73 KB to 373 KB.
- Link preview: `images/og-image.png` is a 1200×630 PNG under 300 KB in the round-8 v9 style, with the name, role, hero line, and highlight tiles copied from the page. It is rendered from a throwaway HTML file with headless Chrome, and that helper is not committed. Both pages point `og:image` and `twitter:image` at `https://redeemed2011.github.io/images/og-image.png`. When the hero or tiles change, rebuild the image and update the meta tags to match.
- Stock photos come only from a source whose license allows reuse, such as Wikimedia Commons (CC0, public domain, CC BY, CC BY-SA), Unsplash, or Pexels. Never use a listing's or breeder's photo. A stand-alone stock photo should be about 800px wide, as a JPEG under 200 KB. Credit the author, license, and source link in the caption.
- Every image has alt text and a short caption.

### Privacy rules

- No pay figures, company names, recruiter names, family details, addresses, phone numbers, or email addresses.
- The only contact links are LinkedIn (https://www.linkedin.com/in/samb1/) and GitHub (https://github.com/redeemed2011).
- Every number must come from a real source: repo docs, tests, configs, Sam's resume, or Sam himself. Never estimate or round up a metric. If a card has no real number, it shows none.
- No secrets, keys, tokens, or internal hostnames, in the page or in the repo.
- Sam's rule (2026-10-27): "anything that would be added to the portfolio site should be blurred out or anonymized to stay within EULA."
- Third-party data (stock figures, company data, news headlines, job postings) must be blurred or replaced with made-up sample values before it goes on the site.

### Preview locally

Open `index.html` in a browser, or serve the folder:

```
python -m http.server 8000
```

Then open http://localhost:8000/. Check it at a phone width (390px) and a desktop width (1280px). With Chrome or Playwright, take full-page screenshots at both widths, and confirm nothing private is readable before asking for approval.

### Publishing

Git Sync does every commit and push to `master`. No other bot or person pushes this repo. Every change is previewed and approved before it is pushed.
