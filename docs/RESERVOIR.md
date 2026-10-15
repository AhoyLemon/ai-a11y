# Reservoir

Everything the talk could draw on: the facts (with sources), the material for each section, the demo app's feature ideas, and the joke avenues. Slides pull from here, and what gets cut goes back here.

## Locked facts

Verified at the primary source on 2026-10-14. Quote these as written; don't round them up.

### FTC v. accessiBe (never cut)

- **The order.** Proposed order announced 2025-01-03 (5-0 vote); final order approved 2025-04-22 (3-0), issued 2025-04-21, in force for 20 years. accessiBe pays **$1 million**, and it can't claim its automated products "can make any website WCAG-compliant or can ensure continued compliance with WCAG over time" without evidence.
- **Complaint ¶7, the claim.** Installing accessWidget's "one line of code" "makes a website compliant with 30% of WCAG's requirements immediately and initiates an AI process that makes the website fully compliant with the remaining 70% of WCAG requirements within 48 hours."
- **Complaint ¶8.** The claims ran in "paid advertisements that Respondents knew were deceptively formatted to appear like impartial reviews and articles."
- **Complaint ¶9, the reality.** accessWidget "fails or has failed to make basic and essential website components like menus, headings, tables, images, recordings, and more, compliant with WCAG and accessible to persons with disabilities."
- **Complaint ¶37, their own 30-second ad.** "accessiBe is the first and only AI-automated web accessibility solution that allows every business to meet ADA and WCAG compliance in 48 hours for only $490 per year."
- **Samuel Levine (FTC).** "Overstating a product's AI or other capabilities without adequate evidence is deceptive, and the FTC will act to stop it."
- **Rule for jokes about it:** stay strictly on the public record.
- **Sources:** [January release](https://www.ftc.gov/news-events/news/press-releases/2025/01/ftc-order-requires-online-marketer-pay-1-million-deceptive-claims-its-ai-product-could-make-websites), [April release](https://www.ftc.gov/news-events/news/press-releases/2025/04/ftc-approves-final-order-requiring-accessibe-pay-1-million), [complaint PDF](https://www.ftc.gov/system/files/ftc_gov/pdf/complaint.222_3156_-_accessibe_final_consent_package_without_signatures.pdf).

### LLMs pass what they can't see (ASSETS '25)

- Kumar, Padath and Wang, "Benchmarking PDF Accessibility Evaluation: A Dataset and Framework for Assessing Automated and LLM-Based Approaches for Accessibility Testing", ASSETS '25, [arXiv 2509.18965](https://arxiv.org/abs/2509.18965).
- Models tested: GPT-4-Turbo, GPT-4o-Vision, Claude-3.5 Sonnet, Gemini-1.5-Pro, Llama-3.2-Vision.
- "Claude-3.5 fabricated alt text descriptions in 32% of 'Cannot Tell' cases."
- Claude-3.5 "tended to default to 'Passed' in uncertain cases", while Gemini-1.5 leaned toward 'Failed'. The authors call Claude's pattern "an underlying bias toward assuming compliance".
- **On-stage caveat:** 2024-era models, and PDFs rather than web pages. The failure mode is the point, not the model.

### Coverage, three ways (all true: "Yes. Also no.")

- **Deque, 2021:** automated testing (axe) found 57% of issues by volume across 13,000+ pages. A vendor study, measuring issue count. [Deque](https://www.deque.com/blog/automated-testing-study-identifies-57-percent-of-digital-accessibility-issues)
- **GOV.UK, 2017:** a page with 142 deliberate barriers. The best tool found 40%, the worst 13%, and 29% were missed by every tool. Home-team credit in London. [GDS blog](https://accessibility.blog.gov.uk/2017/02/24/what-we-found-when-we-tested-tools-on-the-worlds-least-accessible-webpage/)
- **The "20–30%" figure** counts WCAG criteria a tool can fully test, not issues found.

### The state of the web

- **WebAIM Million 2026:** 95.9% of home pages had detectable WCAG 2 failures (up from 94.8%), with 56.1 errors per page on average and low-contrast text on 83.9% of pages. Six error types make up 96% of everything detected. **Verify before use:** coverage attributes the rise partly to AI-assisted coding, but that comes from secondhand reports, not the report itself.

### People and precedents (credit them on the slide)

- **The User Is Drunk:** Richard Littauer, 2015 (he credits the idea to Will Dayble). $250 bought a screen-recorded review of your site, made while drunk. Littauer is colour blind, so the reviews already stacked a permanent impairment on a situational one. [G2 glossary](https://www.g2.com/glossary/the-user-is-drunk-definition)
- **Manuel Matuzović, 2019:** "Building the most inaccessible site possible with a perfect Lighthouse score". A fact for ALSO NO ③, not a joke line. [matuzo.at](https://matuzo.at/blog/building-the-most-inaccessible-site-possible-with-a-perfect-lighthouse-score)
- **The persona spectrum** (permanent / temporary / situational) is Microsoft Inclusive Design's. Drunk is situational.

### To verify before use

- Uber designs for drunk riders with big buttons (Lemon's note). Related: Uber's 2018 patent application on predicting a rider's state from how they use the app.
- WCAG 2.2 has 86 success criteria: 31 at A, 24 at AA, 31 at AAA.
- The European Accessibility Act applies from 28 June 2025, and what it points at (EN 301 549).
- UK: the Equality Act 2010 and the Public Sector Bodies Accessibility Regulations 2018.
- WCAG 3 is still a Working Draft (latest seen: September 2026).
- GTA 6 is dated 19 November 2026. Check the week of each talk.

## Material by section

- **YES:** the free-win hotlist: icon buttons with no name, `outline: none`, `<div onclick>`, unlabeled inputs, a missing `lang`, heading skips, contrast as a computed ratio. "They know WCAG cold, which is exactly why you don't need a skill that re-teaches it."
- **ALSO NO ①, the ladder:** knock-over cases are 1.1.1 (is there alt text? machine. is it right? human), 2.1.1 keyboard (someone has to operate it), 1.4.3 contrast (AA, and a formula), 2.4.7 focus visible (needs the render), 3.3.8 accessible authentication. The evidence rungs: the code, the rendered page, someone operating it, a person's judgment. The skill records which rung it could reach.
- **ALSO NO ②, it wants to say yes:** "You're absolutely right!" on a slide, said by Lemon, then "never trust me when I say that". The ASSETS '25 numbers. "Yes, the model I use every day. That's why the third verdict exists."
- **ALSO NO ③, the marketing bar:** the accessiBe ad copy on screen, the escalating numbers, Matuzović's Lighthouse 100, the three coverage numbers.
- **Three verdicts:** ✅ pass cites its evidence, ❌ fail cites file:line, 🕵️ needs a human and is never guessed as a pass. "No evidence, no pass."
- **Homework:** the agent that fixed it really wants it to be fixed. The certifier gets a clean context and no author story.
- **The floor:** the audit receipt's banner ("I can't guarantee AA, and no automated task can"), the tally, and the over-to-you checklist (screen reader / keyboard / vision and zoom / design and content calls).
- **The ratchet:** impact 1–4 names a group (blind, low vision, keyboard-only, motor, cognitive, deaf/HoH, vestibular); effort 1–4, with the auto-fix line between 2 and 3. Output: Top 3, free wins, a human to-do list, and a deferred pile. The PR receipt carries commit SHAs.
- **The habit:** what a drunk user hits: 2.5.8 target size, 1.4.3 contrast, 3.3.7 redundant entry, 3.3.8 auth puzzles, 2.2.1 timers. Uber's big buttons. "A little better than you found it, forever."
- **Bookend:** the Slack reply. Still an open question in [`DECISIONS.md`](DECISIONS.md).

## Last Orders: features with a11y surface area

Seed list for the demo app's own session. Last Orders (working name) is for a group of friends drinking together: everyone orders their own drinks onto a shared tab, one person pays at the end of the night, and the app settles who owes whom once everyone is sober. Think Tricount, with a specific purpose. Every feature is there to give the talk something to find.

- **Join the tab by QR**, with a typed-code fallback. Scanning needs aiming, steady hands and eyesight, so the fallback is the accessibility story. Drop QR if it stops earning its place.
- **Order a drink:** big tap targets (2.5.8), labelled quantity steppers, drink photos (1.1.1).
- **The running tab:** a real table (1.3.1), live updates when friends add rounds (4.1.3 status messages), toasts that vanish ("Tim added 4 shots") (2.2.1).
- **Balances shown in red and green only** (1.4.1). Littauer is colour blind.
- **A dark "bar mode"** (1.4.3, 1.4.11).
- **Slide to pay and shake to undo** (2.5.1, 2.5.4, 2.5.7).
- **The tab auto-closes at closing time** (2.2.1 timing adjustable).
- **"Close the tab" moves real money** (3.3.4 error prevention).
- **An age check or login puzzle** (3.3.8).
- **The morning-after settle-up:** re-entering payment details (3.3.7), error identification (3.3.1), zoom and reflow on a phone (1.4.10).
- **Two languages and currencies** for Vilnius and London (3.1.1, 3.1.2).

## Jokes and gags

### Standing rules

1. **Claude proposes; Lemon signs off joke by joke.** Nothing goes on a slide without his yes.
2. **Overshoot, never undershoot.** The bar is "oh shit, that was brutal", not "sensible chuckle". Lemon would much rather pull back a joke that went too far than tease a better one out of a timid draft. Scaling back is his job, and that's the system working.

### Avenues

Where the jokes live. Actual jokes get written during slide sessions, then go up for sign-off.

- **Victory declarers:** the Slack poster, the 🎉 PM, "basically done", certificates and trust badges.
- **The overlay industry, strictly on the FTC record:** one line of code, the 48-hour promise, $490 a year, paid ads dressed as impartial reviews (complaint ¶8), the $1M.
- **AI sycophancy and its fabrications,** including Lemon's own daily reliance on Claude.
- **Lemon himself:** never trust him, his friends and their drinking, his questionable internet projects.
- **Developer crimes:** `outline: none` and the war on a blue rectangle, `<div onclick>`, the 400-ticket Jira board.
- **Compliance theatre:** lawyers discovering the word "accessibility" because of the EAA.
- **The drunk user:** Last Orders' actual customers, Uber's big buttons, Littauer's $250 reviews.
- **The room:** Build Stuff's pre-lunch slot, NDC's post-lunch slump in Room 1, backend and .NET devs who think CSS is someone else's problem.
- **Standards that never ship:** WCAG 3 as vaporware.
- **LinkedIn thought leaders and AI hype vendors.**
- **This deck's own non-compliance.** The acknowledgement stays (decks here are built for legibility, not WCAG). It still needs a punchline.
- **Local:** Vilnius (the EAA, beer); London ("last orders", GOV.UK's tool study, British understatement).

### Signed off by Lemon (2026-10-14)

- "Yes. Also no." as a call-and-response, paid off when the title turns out to be the three verdicts.
- The drunk user as a running persona: the human in "needs a human". "Your AI has never been drunk."
- "A skill is just an extremely bossy Markdown file."
- A Jira board so red it fails 1.4.3 on its own.
- `+gag` an overlay toolbar bolted onto a burning building.
- The room hooks.
- Lemon's own lines:
  - The cold open: interrupted about 8 seconds into the intro by a fake in-deck Slack message, acted out.
  - `<div onclick>` "is a button in the same way that Nickelback is death metal."
  - "You're absolutely right!" said on a slide, then "never trust me when I say that."
  - Fabricated alt text: "…that's me reading your LinkedIn post."
  - The price-tag pair: $490 a year to be compliant in 48 hours, or "$35 to buy Tim a bottle of Evan Williams."

### Directions from Lemon

- `outline: none`: escalate to someone whose life was absolutely ruined by a blue rectangle.
- WCAG 3 vs GTA 6 is a maybe. A bit cliché, and a Duke Nukem Forever version may cost too many words.

### Cut, don't re-propose

- "1.1.1 is two checks in a trenchcoat."
- The 4.48:1 "recount" line (plays better to an American audience).
- "My site scores 100 in Lighthouse" as a joke (Matuzović stays, as a fact).
- The talks-page typo.
