# AI projects portfolio

A one-page static site listing Sam Beckwith III's AI projects, served by GitHub Pages at https://redeemed2011.github.io/ from the `main` branch. The URL never changes. An update is a commit and push to `main`, and GitHub Pages republishes it in a minute or two. There is no custom domain.

## Conventions

### File layout

- `index.html`: the whole page, with inline CSS. No build step, no framework, no JavaScript.
- `images/`: every image on the page, plus `og-image.png` (1200×630, the link preview).
- `README.md`: this file.

### Section order

1. Header: name, role, a one-line hero, a short supporting line, LinkedIn and GitHub buttons, a strip of up to 3 real numbers, and section links.
2. Project cards, strongest first: shop assistant, multi-agent system, pi-toolbag (CTX and failover), job search, puppy search.
3. Models I use and how.
4. Stack, as grouped chips. Never skill bars or percentages.
5. Footer: open-source contributions, the screenshot note, links, and the "Updated" month.

### Card structure

Every project card uses these fields, in this order, skipping any it doesn't have:

1. Title (`h2`) and a meta line (year and type).
2. Headline result (`.lede`): one outcome-first sentence.
3. Screenshot or photo, if the card has one.
4. A one-line architecture (`.arch`).
5. "Key decisions": 3 to 5 bullets.
6. "Numbers": real numbers only. If there are none, leave the heading out.
7. Stack chips (`.chips`), 3 to 7 per card.
8. Limits (`.limits`): one honest line.

Keep the copy plain and concrete, and lead with impact. No hype words, no "passionate" bio. Say Sam designed and built the work. Don't list work that is still in development. No tables anywhere. The page is mobile-first and must not scroll sideways at 390px.

### Image rules

- Screenshots are made-up sample data, never real records. Rebuild the page with invented entries, replace every private field with placeholder blocks before rendering, then blur those spots so nothing can be recovered.
- Fields that must be replaced or blurred: pay and prices, company and employer names, recruiter and people names, shelter, rescue, breeder and seller names, addresses and locations, phone numbers, emails, and contact details.
- A real listing's photo is never used. An example listing photo must be a licensed stock photo placed inside the sample screenshot, with its credit in that screenshot's caption. `dog-search-1.png` uses "Black Labrador Pup" by John Schanlaub (CC BY 3.0, https://commons.wikimedia.org/wiki/File:Black_Labrador_Pup.jpg), cropped to fill the photo spot.
- Size: render at a 430px-wide viewport at 2× scale, which gives 860px-wide PNGs. Crop to one readable section at a time, about 600 to 1,000px tall, with a clean edge and no cut-off lines of text.
- Stock photos come only from a source whose license allows reuse, such as Wikimedia Commons (CC0, public domain, CC BY, CC BY-SA), Unsplash, or Pexels. Never use a listing's or breeder's photo. A stand-alone stock photo should be about 800px wide, as a JPEG under 200 KB. Credit the author, license, and source link in the caption.
- Every image has alt text and a short caption.

### Privacy rules

- No pay figures, company names, recruiter names, family details, addresses, phone numbers, or email addresses.
- The only contact links are LinkedIn (https://www.linkedin.com/in/samb1/) and GitHub (https://github.com/redeemed2011).
- Every number must come from a real source: repo docs, tests, configs, Sam's resume, or Sam himself. Never estimate or round up a metric. If a card has no real number, it shows none.
- No secrets, keys, tokens, or internal hostnames, in the page or in the repo.

### Preview locally

Open `index.html` in a browser, or serve the folder:

```
python -m http.server 8000
```

Then open http://localhost:8000/. Check it at a phone width (390px) and a desktop width (1280px). With Chrome or Playwright, take full-page screenshots at both widths, and confirm nothing private is readable before asking for approval.

### Publishing

Git Sync does every commit and push to `main`. No other bot or person pushes this repo. Every change is previewed and approved before it is pushed.
