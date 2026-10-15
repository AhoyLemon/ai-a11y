# Timeline

How the talk breaks into sections and how long each one gets.

**This is a living draft.** The run of show below was set before any real slides existed, and it will move as they get written. That's expected. The rule: any PR that touches slides updates this file to match the real `data-timing`, and the PR description calls out every section running over or under its budget before the PR opens.

## The slots

| | Build Stuff | NDC London |
|---|---|---|
| When | Wed 2 Dec 2026, 12:15 | Wed 27 Jan 2027, 15:00 |
| Where | Vilnius, room Alpha | Queen Elizabeth II Centre, Room 1 |
| Listed | 45 min (soft) | 60 min |
| Tracks / tags | Developer, Machine, AI-native dev, Developer craft, Frontend & UX | Accessibility, AI Agents, AI Tools and Data, UX, Web |
| Level | Intermediate, Advanced | Not listed |
| The talk | **50:00, no Q&A** | **50:00, no Q&A** |

One path, the same in both rooms. **No Q&A inside the slot, ever.** Questions happen after the monologue, in the hallway. The lemon slide is just the end of the deck.

## The spine

Everything in the deck hangs off this. If a section serves none of the three tenets, it's a candidate to cut.

> **A machine can prove a fail. It can never prove a pass.**
>
> 1. **Three answers, not two.** Pass, fail, needs a human. A report without the third pile is lying by omission.
> 2. **Nobody grades their own homework.** Finder, fixer and certifier are separate, even when they're the same model.
> 3. **Floor once, ratchet forever.** Audit to know where you stand; improve on every PR, worst harm to named people first.

The closing line is **a receipt, not a certificate.**

## What they walk out with

- The three tenets as habits. They work with any scanner or agent, including at companies where installing skills is banned.
- The install line, as the fastest way to do all three: `npx skills add ahoylemon/<skill-tbd>` (the name waits until the skill exists).
- The exact reply to post in Slack the next time someone says "we're basically done".

## Run of show (50:00)

The order is the abstract's: good news first, then the limits, then the system, then the habit.

| Clock | Beat | Time | Serves |
|---|---|---|---|
| before | The intro reel (`_intros.pug`), `data-timing="0"` | 0:00 | tone |
| 0:00 | **Cold open.** Lemon starts his intro, about 8 seconds in, and a fake in-deck Slack message interrupts: "See? We're basically done." 🎉. Acted out. "Nobody misread the findings. They misread how final they were." | 2:00 | spine |
| 2:00 | Hello + Blank Metal (shared, 5 slides at the 10s default) | 0:50 | tone |
| 2:50 | **The question.** The title asks it, and the answer is "Yes. Also no." (seeds the call-and-response). Spine stated. Stakes: 95.9% of home pages fail; the EAA in Vilnius, the Equality Act in London. | 3:10 | spine |
| 6:00 | **YES.** Good news first: what the agent proves, fast. The six error types behind 96% of detected failures are all machine-provable. Real ❌ with file:line from Last Orders. | 8:00 | 1 |
| 14:00 | **ALSO NO ①, the ladder.** A/AA/AAA set up as "easy to hard", then knocked over: 1.1.1 is Level A and needs a human, 1.4.3 is AA and is a formula. What each check needs to see. The line moves when you give it eyes. | 5:00 | 1 |
| 19:00 | **ALSO NO ②, it wants to say yes.** ASSETS '25: Claude defaulted to pass, Gemini to fail, neither said "I don't know". | 4:00 | 1, 2 |
| 23:00 | **ALSO NO ③, the marketing bar.** One line of code, 48 hours, $490 a year, the $1M FTC order. Coverage three ways: 57% / 40% / 13%. | 4:00 | spine |
| 27:00 | **Three verdicts.** Pass, fail, needs a human. No evidence, no pass. Reveal: the title was the spec all along (Yes / No / Also). | 4:00 | 1 |
| 31:00 | **Nobody grades their own homework.** Finder, fixer, certifier. | 3:00 | 2 |
| 34:00 | **The floor.** The audit receipt, in-deck. | 5:00 | 1, 2 |
| 39:00 | **The ratchet.** Improve on a PR: every finding names a person, Top 3, free wins, the human to-do list. | 5:00 | 3 |
| 44:00 | **The habit.** Compliance is the floor, purpose is the ratchet. The drunk-user payoff. A little better, forever. | 3:00 | 3 |
| 47:00 | **Bookend.** The Slack reply, the three takeaways, "a receipt, not a certificate", the install line. | 2:20 | spine |
| 49:20 | Hit me up, thank you, the lemon slide (shared, 4 slides at the 10s default) | 0:40 | tone |
| **50:00** | **End.** Questions in the hallway. | | |

The clock column is the sum of every slide's `data-timing`, which is what reveal's speaker view paces against. Shared slides without their own timing fall back to `defaultTiming: 10` in `js/reveal-config.js`. Reset the speaker-view timer on the first cold-open slide, after the intro reel.

## Cut order

When running long, cut in this order:

1. The coverage numbers in ALSO NO ③.
2. Fold "Nobody grades their own homework" into the floor.
3. Trim the YES examples down to the strongest three.
4. Show one receipt (floor or ratchet) instead of two.

**Never cut:** the cold open, the ladder knock-over, FTC v. accessiBe, the three verdicts, the bookend.
