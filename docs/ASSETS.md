# Assets

Every visual the deck needs, where it lives and where it's used. The deck works offline, so everything is local and `.webp` where it can be, sized for the projected slide. Talk-specific images go in an unprefixed folder such as `img/gag/`; folders starting with `_` are shared across talks.

## Adding a visual gag

Draft the bit as a `+gag` placeholder, a dashed yellow box with a description, so it can be judged before anyone hunts for the image. It can't ship by accident:

```pug
+gag("An overlay toolbar bolted onto a burning building.")(data-timing="20")
  h2 One line of code.
  aside.notes
    ul
      li …
```

When the asset lands, swap the call for an ordinary section with a background, and keep its timing, caption and notes:

```pug
section.over-media(data-background-image="img/gag/overlay-fire.webp" data-background-size="cover" data-timing="20")
  h2 One line of code.
  aside.notes
    ul
      li …
```

Only signed-off bits get a placeholder (see the joke rules in [`RESERVOIR.md`](RESERVOIR.md)).

## Shopping list

| Where | Slide | Asset | Status |
|---|---|---|---|
| `_cold-open.pug` | The interruption | A fake Slack notification sliding in over the intro. Probably built in HTML/CSS rather than as an image (open question in [`DECISIONS.md`](DECISIONS.md)). | needed |
| `_also-no-marketing.pug` | One line of code | An overlay toolbar bolted onto a burning building. | needed |
| `_ratchet.pug` | The backlog | A Jira board so red it fails 1.4.3 on its own. | needed |
| `_habit.pug` | The drunk user | To be proposed. | open |
