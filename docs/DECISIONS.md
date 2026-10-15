# Decisions

Open questions on top, settled ones below. When a question gets answered, move it to the log. The log is append-only: add new rows at the bottom, and if a decision gets reversed, add a row that says so rather than editing the old one.

## Open questions

| Question | Where | Issue |
|---|---|---|
| What exactly does the Slack reply say? It's the bookend and one of the takeaways, so it has to be postable as-is. | `pug/sections/talk/_bookend.pug` | |
| Does the "Yes / No / Also" title reveal land, or is it too cute? Test it in the first full run-through. | `pug/sections/talk/_verdicts.pug` | |
| How do we word the ASSETS '25 caveat on stage (2024-era models, PDFs) without blunting the finding? | `pug/sections/talk/_also-no-agreeable.pug` | |
| How is the cold open's fake Slack message built: an HTML component in the deck, or an image? | `pug/sections/talk/_cold-open.pug` | |
| What's the public skill called? It must contain "a11y", and the name waits until the skill exists. | closing slide, `docs/TIMELINE.md` | |
| What's the demo app's final name? "Last Orders" is a working name. | `docs/RESERVOIR.md` | |
| Does QR earn its place in Last Orders, or does it go? | `docs/RESERVOIR.md` | |
| What's the punchline for "this deck isn't WCAG compliant"? | `docs/RESERVOIR.md` | |
| What's the drunk user's visual? | `docs/ASSETS.md` | |

## Decided, recorded here so it does not get re-litigated

| Date | Decision | Rationale |
|---|---|---|
| 2026-10-14 | Reference Blank Metal freely, but use none of its assets: not `workshop-exercises`, not honest-a11y's files, not the Smelter deck or its Lectern receipts. Ideas and phrasing Lemon authored are his to use ("I built a version of this at work"). Every artifact is made fresh. | Blank Metal work product isn't Lemon's to put on a public stage. His own ideas are. |
| 2026-10-14 | The spine is "A machine can prove a fail. It can never prove a pass." The closing line is "a receipt, not a certificate." | It's the title's real answer: yes, it finds the failures; no, it can't pass your audit. The earlier "faster, not smarter" is true of every AI talk and memorable in none. |
| 2026-10-14 | Three tenets: three answers, not two; nobody grades their own homework; floor once, ratchet forever. "Every finding names a person" lives inside the ratchet. | Three is enough to cut against, and they double as the takeaways. |
| 2026-10-14 | The talk runs in the abstract's order: good news first. Compliance vs. purpose folds into floor vs. ratchet; there's no standalone empathy opener. | The abstract promised "good news first" and "an actual workflow, not just the philosophy" in print. The earlier outline didn't show the system until 22:00. |
| 2026-10-14 | The A/AA/AAA ladder stays, but gets set up and knocked over: 1.1.1 is Level A and needs a human; 1.4.3 is AA and is a formula. No unsourced percentages. | A conformance level says nothing about whether a machine can check it. A room at NDC will know that, so the talk says it first. |
| 2026-10-14 | One 50-minute path for both venues. Build Stuff's 45 is soft. | One deck, no fork. NDC's 60-minute slot runs closer to 50 in practice. |
| 2026-10-14 | No Q&A inside the slot, ever. Questions happen after the monologue. | How Lemon gives talks. |
| 2026-10-14 | The run of show is a living draft. Every slide PR updates `docs/TIMELINE.md` to the real `data-timing` and calls out sections over or under budget before it opens. | The timeline was set before any slides existed. It's guidance, and it only stays useful if it tracks reality. |
| 2026-10-14 | FTC v. accessiBe is never cut. | Lemon's favourite fact of the planning session, and the concrete version of the abstract's "marketing bar". |
| 2026-10-14 | Demos are in-deck receipts: real skill runs against the demo app, captured into demo pages, with the live GitHub links on the closing slide. No live LLM on stage. | Works on dead venue wifi, and agent runs are slow and nondeterministic. |
| 2026-10-14 | The takeaways are three tool-agnostic habits plus the tool. | They still work where installing skills is banned. The tool is the fastest way, not the only way. |
| 2026-10-14 | The public skill is built fresh, in its own repo. Its name stays open until it exists and must contain "a11y". It adapts to what the agent can see (a browser or axe when available, source code when not), and every verdict records the evidence it used. | The concept comes first and the name follows it, not the other way round. A public skill can't assume what any given setup lets the agent see. |
| 2026-10-14 | The talk repo is `AhoyLemon/ai-a11y`. | Short and topical, like the other talk repos, and it leaves the memorable names for the skill. |
| 2026-10-14 | The Blank Metal intro stays. | Naming your employer is identification, not using its work. |
| 2026-10-14 | The personal beat is the drunk user, as a running persona: the human in "needs a human". | Situational impairment that touches motor, vision, memory and attention at once, and it's funny. |
| 2026-10-14 | "Yes. Also no." becomes a call-and-response, paid off when the title turns out to be the three verdicts. | It makes the title do work, and it gets the room talking. |
| 2026-10-14 | The demo app is Last Orders (working name): a shared drinks tab for a group of friends, settled once everyone is sober. It lives in its own public repo, and its features exist to give the talk accessibility surface area. | Its real users are the drunk persona. A fresh, public app also keeps every receipt showable. |
| 2026-10-14 | Joke rules: Claude proposes, and Lemon signs off joke by joke. Overshoot, never undershoot. The bar is "oh shit, that was brutal". | Pulling back a joke that went too far is cheap. Rescuing a timid one isn't. |
| 2026-10-14 | The TODO list carries no dates. | Lemon schedules his own time. |
