# Output Format

The exact shape of a weekly plan. Adapt wording to the user, but keep these structures —
they're what make the plan scannable and editable.

## The weekly plan

One block per cooking night. Order nights the way the user's week actually runs.

```
### <Day> — <Dish name>
<One or two sentences: the dish, the technique, what goes on the table.>
Table: <family-scale quantities and any kid/spice notes>.
Count math: <state it explicitly, e.g. "8 patties → table uses 5 → 3 leftover">.
[Primary eater]: <specific plate>.  [macros if enabled — see below]
Leftovers: <estimate + where they go>.
Flag: <optional — missing ingredient, heavy-fat night, thaw reminder, prep timing>.
```

Notes:
- **Count math is not optional** when packs/multiples are involved. It's the #1 source of
  errors and the fastest thing for the user to sanity-check.
- **`Flag:` only when there's something to say** — don't pad every night.
- End the plan with a **leftover summary** ("3 patties + 2 chops = lunch proteins Thu–Sat")
  and note what staples went *unused* and could anchor a flex day or next week.

## Macro line (only if preferences provide targets)

Format, for the primary eater's plate:

```
~<cal> cal / <P>g P / <total C>g C (<net>g net) / <F>g F
```

- **Lead with the plate total**, then flag the **binding constraint** for the day (e.g.
  "fat's the watch item tonight — skip the cheese"). Don't annotate every macro.
- **Mark confidence** on estimates you're unsure of ("moderate confidence — check the pack").
- If the user shares a logged actual (e.g. a MyFitnessPal screenshot), **defer to it** and
  carry that number forward; don't relitigate.
- Report **both total and net carbs** unless preferences say otherwise.

## Grocery list

Grouped by store section, with have/buy split. See `templates/grocery-list-template.md`.

```
## Grocery List — <store(s)>

### Produce
- [ ] <item> — <qty>        (need)
- [x] <item>                 (have)
...
### Meat & Seafood
...
```

- **Only put "need" items on the buy path**; mark on-hand items as already covered.
- **Flag substitutions** inline for anything missing ("no feta on hand — grab a block, or
  shave parmesan").
- If two stores, tag items to the right store.

## Prep & cook notes

A short list, front-loaded with anything time-sensitive:
- **Day-before:** thaw/defrost, marinate, soak.
- **Make-ahead / batch:** what to cook once and reuse.
- **Timing:** if a target dinner time is set, when to start each night to hit it.

## Recipes

Keep them tight — a few numbered steps, one pan where possible. Only expand a recipe when
the user asks or when the dish isn't obvious. Echo the user's cooking sources/style.
