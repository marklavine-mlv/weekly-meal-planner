# Weekly Meal Planner — a Claude Skill

Plan a week of meals around the staples you already keep on hand. The skill produces:

- an **editable N-day plan** (default: 5 cooking nights + 2 flex days for leftovers / eating out),
- a **grocery list grouped by store section**, split into *already have* vs *need to buy*,
- **prep & cook notes** with thaw/make-ahead timing, and
- **short recipes** in your cooking style.

It optionally estimates **per-plate calories and macros** for one "primary eater" when you
provide targets — otherwise it skips macros entirely.

It's built around the things that make a plan actually get cooked: planning around a small
rotation of reliable meals, one batch for the whole table, honest count/portion math, and
routing every leftover to a job.

## Install

### Claude Code (CLI / desktop / IDE)
Clone or copy this folder into your skills directory:

```bash
git clone <your-repo-url> ~/.claude/skills/weekly-meal-planner
```

The skill is available the next time you start Claude Code. Trigger it by asking, e.g.,
"plan my meals for the week" or "help me build a dinner plan and grocery list."

### Claude Chat / Projects
Upload the skill folder (or its zip) as a Skill, or paste `SKILL.md` into a Project's custom
instructions. Add your filled-in `preferences.md` to the Project's knowledge so it's used
every week.

## Set it up (once)

1. Copy `preferences.example.md` to `preferences.md`.
2. Fill in your household, staples, stores, dietary rules, and (optionally) macro targets.
   Anything you leave blank falls back to a sensible default.
3. Keep `preferences.md` where Claude can see it (your project knowledge, or paste it when
   you start planning).

If you don't provide a preferences file, the skill asks a short intake before planning.

## Use it

> "Plan this week — I've got ground turkey, pork chops, and frozen shrimp, cooking for 4,
> five nights."

The skill drafts the plan, grocery list, and prep notes. **Expect to edit it** — correct any
counts or portions and it will recompute leftovers, macros, and quantities. When you're happy,
it can *offer* to add calendar invites or reminders (only with your go-ahead).

## What's in here

```
weekly-meal-planner/
├── SKILL.md                          # the skill: workflow + rules
├── preferences.example.md            # copy to preferences.md and fill in
├── references/
│   ├── output-format.md              # exact plan / grocery / prep / recipe layout + macro format
│   └── satiety-and-adherence.md      # reusable principles: volume, rotation, leftovers
├── templates/
│   ├── weekly-plan-template.md
│   └── grocery-list-template.md
└── examples/
    └── sample-week.md                # a worked example (family of four)
```

## Customize

The behavior lives in plain markdown — edit `SKILL.md` and the `references/` files to change
how it plans. The `preferences.md` file is for *your* data; the reference files are for
*everyone's* rules. Keep personal specifics out of the shared files so the skill stays
shareable.

## License

MIT — see [LICENSE](LICENSE).
