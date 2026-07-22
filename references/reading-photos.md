# Reading Photos Into a Plan

Claude sees attached images natively, so a user can skip typing and just show you what
they've got. This is often the *fastest* way to start a plan. Handle these image types:

## What each photo type gives you

- **Fridge / pantry shot** → the on-hand inventory. Identify visible ingredients and rough
  quantities. This tells you what the plan should *use up* first.
- **Grocery receipt** → what they just bought / want to build around this week. Itemize the
  food lines (ignore non-food), with counts/weights where the receipt shows them.
- **Handwritten or notes-app list** → transcribe the items as the shopping or on-hand list.
- **Cookbook / recipe photo** → what they want to cook. Capture the *dish and technique in
  your own words* for planning. Do **not** reproduce the copyrighted recipe text in your
  output or anywhere in this repo — point to the source instead (see `references/recipes.md`).
- **Plate / meal photo** → for macro estimates: identify the components and estimate portions.

## Rules for reading photos

1. **Extract only what you can actually see.** Never invent items that "should" be there. A
   fridge photo shows the front row — assume nothing about what's hidden behind it.
2. **Show your read, then confirm.** Reply with a quick "Here's what I found:" list and let
   the user correct it *before* you build the plan. Photos miss things, and a wrong inventory
   quietly corrupts the whole plan and grocery list.
3. **Estimate quantities conservatively and flag low confidence.** "Looks like ~1 lb ground
   beef, a half-used block of feta, a bag of spinach (maybe half gone?)." Mark the guesses.
4. **Ask only about what changes the plan.** Proteins and anything you'd otherwise put on the
   shopping list are worth a question; a jar of mustard is not.
5. **Combine the photo with everything else.** Household size, allergies, macro targets, and
   store still come from `preferences.md` or the intake — the photo only replaces the
   "what's on hand / what to build around" input.
6. **Multiple photos are fine.** A fridge shot + a receipt together is a great signal — one is
   what's on hand, the other is what's incoming. Merge them into a single on-hand list.

Once the inventory is confirmed, proceed with normal planning (Step 1 onward).
