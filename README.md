# AI projects portfolio

A one-page static site listing Sam Beckwith III's AI projects, served by GitHub Pages at https://redeemed2011.github.io/ from the `master` branch. The URL never changes. An update is a commit and push to `master`, and GitHub Pages republishes it in a minute or two. There is no custom domain.

## Conventions

### File layout

- `index.html`: the main page. CSS is inline in a `<style>` block, and two small inline scripts run the phone menu, the active nav link, the section-header animation, and the ticket-to-PR checklist animation.
- `approach/index.html`: the "Start from the goal" article (page title "How I design agent pipelines"), linked as "My approach". It repeats the same inline CSS and menu script.
- `images/`: every screenshot on the page, plus `og-image.png`, the link preview. There are no `css/` or `js/` folders.
- `README.md`: this file.

### Build step

None. The repo is plain HTML and CSS served as is, with no framework, package manager, or generated files. Fonts load from Google Fonts. Do not add a dependency or a build tool.

### Design

The current design is round-8 v9: a dark terminal style with orange accents, dim orange `>` markers before card meta lines, bracketed section headers such as `[ Full-time work ]` with a rule after them, rounded mono stack chips, and a thin rule between cards. New sections and images should match it.

### Section order

1. Header: name, role ("Senior SRE · AI platform engineering". It describes the work, and the site never claims a job title Sam doesn't hold), LinkedIn and GitHub buttons, "12+ years in SRE and platform engineering", the one-line hero ("I build internal AI agents and platforms that change how engineering teams work."), a short intro, and four highlight tiles: Ticket to PR (agent pipelines, design to review), Self-service IaC (engineers ship their own infrastructure changes), 3x (my engineering output), and 6x (faster CI/CD).
2. My approach: a short pull quote that links to `approach/`.
3. Full-time work, newest first: the ticket-to-PR pipeline, AI agents, the IaC platform, Kubernetes reliability, CI/CD, then the Kubernetes migration. No employer names, code, or screenshots.
4. Side projects, one section: the garage assistant, pi-toolbag, the Grok CLI harness, the assistant team (no household, family, or health details and no diagram), and the AI job-search pipeline. There is no separate "Personal projects" section or nav link.
5. Open source.
6. Models.
7. Stack, as grouped chips. Never skill bars or percentages.
8. Footer: LinkedIn and GitHub links, and the "Updated" month.

### Card structure

Every project card (`article.card`) uses these parts, in this order, skipping any it doesn't have:

1. Meta line (`.meta`): a dim orange `>`, the area name, and the year range, for example "> Kubernetes Reliability · 2024–present".
2. Title (`h3`).
3. Headline result (`.lead`): one outcome-first sentence.
4. Numbers (`.facts`): real numbers only. If there are none, leave it out.
5. Screenshots or a diagram, if the card has one.
6. Two short bullet lists. The first is headed "How it works" when it describes the system, or "What I built" or "What I did" when it describes Sam's own work. Mechanics such as watchdogs, rollbacks, backups, sandboxes, and test gates go here. The second is "Why it matters", and it states real impact on the people and teams who use the work, never mechanics and never a repeat of the headline.
7. Stack chips (`.chips`), 3 to 7 per card.

A card may add a short context line (`.sub`) after the headline that states the goal, what made it hard, or the main design choice.

A card may also add a short "Limits:" line (`.limits`) after the two lists and before the chips, stating what the system does not cover.

Keep the copy plain and concrete, and lead with the outcome, then how it works. No hype words, metaphors, coined labels, em dashes, or "not just X but Y". No "passionate" bio. Projects say "Designed and built". Never say "led" or "directed". Say "my team" only for what the team actually uses, and don't claim company-wide reach without a confirmed number. The IaC platform shows no engineer count and no percentage. The ticket-to-PR, incident, and research pipelines are separate pipelines that share tooling. Don't list work that is still in development. Use real numbers only. No tables anywhere. The page is phone-first: check it at 390px, and it must not scroll sideways.

### Image rules

- Screenshots are made-up sample data, never real records. Rebuild the page with invented entries, replace every private field with placeholder blocks before rendering, then blur those spots so nothing can be recovered.
- Fields that must be replaced or blurred: pay and prices, company and employer names, recruiter and people names, shelter, rescue, breeder and seller names, addresses and locations, phone numbers, emails, and contact details.
- A real listing's photo is never used. An example listing photo must be a licensed stock photo placed inside the sample screenshot, with its credit in that screenshot's caption. No screenshot on the site uses a stock photo today.
- Size: render at a 430px-wide viewport at 2× scale, which gives 860px-wide PNGs. Crop to one readable section at a time, about 600 to 1,000px tall, with a clean edge and no cut-off lines of text.
- Where they live: every screenshot is a PNG in `images/`, named after its project with a number (for example `shop-1.png`). A replacement for a live image gets a suffix such as `-r6`. Today there are four screenshots, all 860px wide: `shop-1.png` (the build board, made-up sample data), `job-pipeline-2.png` (a job-search role card for the made-up sample company "Example Robotics Co.", restored from commit 93303ca; the "Status copy" and "Apply" rows are cut out so it shows no application status, and it holds no real company, person, URL, pay, or metro area), `job-pipeline-3.png` (the job-search company card, made-up sample company "Northwind Robotics", restored from commit 93303ca and cropped to the company card; the stock benchmark name and the layoffs.fyi link are covered with placeholder blocks and blurred), and `shop-2.png` (a Slack thread Sam supplied from the garage assistant's staging workspace). In `shop-2.png`, every person's name and the build links (URL and build id) are covered with placeholder blocks and blurred. Build names, such as "Beau Brown 59 Viking (Powerhouse)", stay readable at Sam's request (2026-10-31), and the phone status bar is cropped off.
- No placeholder images, diagrams, or captions go live. If a diagram isn't final, leave it out.
- Link preview: `images/og-image.png` is a 1200×630 PNG under 300 KB in the round-8 v9 style, with the name, role, hero line, and highlight tiles copied from the page. It is rendered from a throwaway HTML file with headless Chrome, and that helper is not committed. Both pages point `og:image` and `twitter:image` at `https://redeemed2011.github.io/images/og-image.png`. When the hero or tiles change, rebuild the image and update the meta tags to match.
- Stock photos come only from a source whose license allows reuse, such as Wikimedia Commons (CC0, public domain, CC BY, CC BY-SA), Unsplash, or Pexels. Never use a listing's or breeder's photo. A stand-alone stock photo should be about 800px wide, as a JPEG under 200 KB. Credit the author, license, and source link in the caption.
- Every image has alt text and a short caption.

### Privacy rules

- No pay figures, employer or company names, recruiter names, job searches, family or health details, pets' locations, addresses, phone numbers, or email addresses.
- Exception (Sam, 2026-10-31): the AI job-search pipeline card is allowed. It still names no real companies, recruiters, or job boards, and shows nothing about what Sam has applied to.
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

One designated publisher does every commit and push to `master`, and nobody else pushes this repo. Every change is previewed and approved before it is pushed.
