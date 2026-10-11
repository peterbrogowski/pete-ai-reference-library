# 🍎 Kid Chef Recipe — Claude Skill

**Owner:** Pete Brogowski
**Built:** 2026-10-11  |  **First recipe:** Apple Crisp (Eating on a Dime)
**Status:** ✅ Saved as a Claude skill (`kid-chef-recipe`)

---

## 🗺️ Big Picture

Turns any cluttered recipe into a **printable 8.5×11 PDF** a 12-year-old with ADHD can cook from on her own (with a grown-up for knife and heat).

```
GATHER ──► MEASURE (mise en place) ──► COOK ──► CLEAN UP ──► HOW DID IT GO?
get it out   one cup per item,           pour cups    put it      circle a face,
by where     labeled by step (4A)        by label,    all away    note what was hard
it lives     NO bowls yet                one job/step
```

## ▶️ How to use it

- In Claude, type `/kid-chef-recipe` plus a recipe link, a photo, pasted text, or just a dish name.
- Print at **100% / Actual size**, single-sided.
- Cut out the cup labels (last page) before starting.

## 💡 Lessons that shaped it

- **Never say which bowl things go in on page 1.** She started adding ingredients early. Bowls appear only inside the cooking steps.
- **Mise en place teaches organization.** Each ingredient goes into its own labeled cup. A "divided" ingredient becomes two cups (e.g. 4B and 6E), so nothing gets mixed up.
- **Print, don't share links.** She doesn't use a Claude account, so the output is always a PDF.

## 🔧 Things to update over time

- **Kid settings:** move items from "Grown-up job" to "Can do" as she's ready (stove, chef's knife).
- **Her feedback:** bring her "How did it go?" answers back to Claude to tune the next guide.

---

## 📄 Full SKILL.md

```markdown
---
name: kid-chef-recipe
description: Turn any recipe (URL, photo, pasted text, or dish name) into a printable 8.5x11 kid-friendly PDF for a child with ADHD that teaches mise en place: gather, measure into labeled cups, then cook one job at a time.
---

# Kid Chef Recipe

Converts any recipe into a printable, ADHD-friendly cooking guide for a kid (about 12) who cooks with a parent. The output is always a **US Letter PDF**, because the kid prints it and doesn't use a Claude account.

The guide teaches **mise en place** ("meez-on-plahs", French for "everything in its place"): get every ingredient out, measured, and lined up BEFORE cooking starts. Then each cooking step is just "pour in the cups labeled with this step's number."

## Kid settings (the parent edits these as she grows)
- **Can do on her own:** measuring, stirring, peeling with a peeler, microwave, cracking eggs, butter knife for soft things, reading timers.
- **Grown-up job for now:** chef's knife, stove burners, putting pans in or taking them out of the oven, boiling water, hand mixer on high.
- **Reading level:** short sentences of 12 words or fewer, one action per sentence.

Any step that uses something from the grown-up list is tagged **Grown-up job**. When the parent says something like "she can use the stove now," move that item to "Can do" for that run and suggest updating this section.

## Inputs
- A recipe URL (WebFetch the recipe card only; ignore story text, ads, and nutrition facts), a photo, or pasted text.
- A dish name only: find a simple, well-rated recipe that suits a kid, and say which one you used in one line.
- If servings or pan size are unclear, use the recipe's default and say so in one line. Ask only if the recipe can't be made without the answer.

## Workflow
1. **Extract** every ingredient with its exact amount, pan size, temperature, times, and the original steps.
2. **Simplify amounts:**
   - Use whole units: ½ cup butter becomes 1 stick.
   - Convert amounts that need unusual spoons, like ⅓ Tbsp, into something she can measure.
   - Split any "divided" ingredient into separate amounts, one per step that uses it.
   - Give every amount a plain hint: "big spoon, 2 times," "small spoon, half full," "pack it down," "level the top."
3. **Plan the cooking steps** with ONE job per step, 8 to 12 steps total. Apply the Kid settings. Add a "Halfway there!" note at the midpoint. Wait steps (bake, chill, simmer) get a big time badge plus a "how you know it's done" sign.
4. **Assign cup labels.** Every measured ingredient gets a label made of its step number plus a letter, in order: 4A, 4B, 4C, 6A, and so on. Whole items that need no measuring (6 apples, 1 stick of butter, 2 eggs) get a label too, so everything is lined up.
5. **Assign stations and colors**, used ONLY on the cooking steps: Bowl 1 = red #c8322a, Bowl 2 = gold #9a6413, Bowl 3 = green #2f7d4a, Bowl 4 = purple #6b3fa0, Oven/Stove/Pan = blue #2f4f9c. Every tag is also printed as words ("BOWL 1") so the page works in black and white.
6. **Time check:** work out total time, hands-on time, and wait time.
7. **Build the pages** (structure below), render the PDF, check it once, and deliver it.

## Page structure

### Cover strip (top of page 1)
- Dish name (big), recipe number for her binder ("Recipe #__", left blank for the parent to fill in), and "Page 1 of N".
- **Time check bar:** "About 1 hr 5 min total · You're busy for 25 min · 45 min wait." Add a line: "Do you have this much time right now? If not, pick another day."
- Key: Tbsp = big spoon · tsp = small spoon · cup = measuring cup.

### Part 1: GATHER (page 1)
- Group by **where things live**: Fridge, Pantry, Spice shelf, Fruit & veg, Drawer & cabinet (tools). NEVER group by bowl or step.
- Show checkbox + item, with no amounts here. This part is only about getting things out.
- Tools must include small cups or ramekins (give the exact count = number of cup labels), masking tape or sticky notes, and a marker. Also list the bowls and pans needed, by count only ("3 mixing bowls").
- **Set up your space** box: clear the counter, wash hands, put on an apron, set out the empty bowls and pan, measuring tools in one spot.

### Part 2: MEASURE — Mise en Place (page 2)
- A short intro: "Measure each thing into its own little cup. Put the label on the cup. Do NOT mix anything together yet."
- A table in label order, one row per cup: ☐ | **Label** (big, e.g. 4A) | **Amount badge** (neutral dark color, no station color) | item | hint.
- If an ingredient is used in two steps, it gets TWO rows and two cups (4B ½ tsp cinnamon, 6E 1 tsp cinnamon). This is how the "divided" problem disappears.
- Prep tasks (peel, chop, cube the butter) go in their own "Prep" list after the measuring table, each tagged Grown-up job when the Kid settings say so. Each prepped item also goes into a labeled cup or onto a labeled plate.
- **Line it up** box: "Put your cups in a row in label order, left to right. 3A is first."
- No bowl numbers or station colors anywhere in Parts 1 and 2. Use neutral black or grey only.
- End with a bold box: **"Everything in its place? Check the box, then turn the page. ☐ I'm ready to cook."**

### Part 3: COOK (step cards)
- Colored header bar with a big number circle, a short verb-first title, and the station tag.
- One instruction sentence that names the bowl in bold: "Pour cups 4A, 4B and 4C into **Bowl 1**. Stir."
- Rows for this step's cups: ☐ + **label** + amount badge in the station color + item. The amount is repeated so she can double-check the cup.
- Optional tip line: Grown-up job / Stop when... / Halfway there!
- Wait steps get a brain-break line: "45 min: go do something fun. Come back when the timer rings."
- A big **☐ DONE** box on every card. Cards never split across pages. Use 3 or 4 cards per page.

### Part 4: CLEAN-UP CREW (one card, grey)
- ☐ Empty cups into the sink · ☐ Put ingredients back where they live · ☐ Wipe the counter · ☐ Dishes in the sink or dishwasher · ☐ Oven off (Grown-up check).

### Part 5: HOW DID IT GO? (bottom of the last page)
- Circle one: 😀 😐 😕 (draw simple faces with CSS or SVG; emoji fonts may not render in the PDF).
- Lines for: "The hardest part was..." · "Next time I want to..." · "Would I make it again? Yes / No"
- A dashed "You made [dish]!" box.
- When the parent later shares her answers, use them to adjust the next guide (for example, more hints on measuring). Suggest updating Kid settings if a pattern repeats.

### Part 6: CUP LABELS (last page, optional but default ON)
- A cut-out sheet of labels in a grid of dashed boxes, one per cup: big label (4A) + amount + item. She cuts them out and tapes them to the cups.

## Rendering (Playwright + fontsource)
- Fonts: run `npm pack @fontsource/baloo-2 @fontsource/atkinson-hyperlegible` in the scratchpad and extract. Baloo 2 800/600 for numbers, titles, badges, and labels; Atkinson Hyperlegible 400/700 for body text. Load with local @font-face URLs, fallback DejaVu Sans.
- CSS essentials:
  - `@page{size:letter;margin:0.5in}`
  - `*{print-color-adjust:exact;-webkit-print-color-adjust:exact}`
  - Body 14pt, step titles 21pt, badges 16pt bold with white text, cup labels 18pt
  - Each `.page` is `height:10in` with `break-after:page`
  - Cards use `break-inside:avoid`
  - "Page X of N" in every page header
- Render: Chromium `page.pdf(format='Letter', print_background=True, prefer_css_page_size=True)`.
- Check once: run `pdftoppm -r 50` on all pages and view them as a contact sheet, then zoom one page at 110 dpi to confirm fractions (½ ¼ ¾ ⅓) render. Fix any overflow and re-render once.
- Name the file `<Dish>_Kid_Chef.pdf` and deliver it with SendUserFile (display: render).

## Reply to the parent (short)
- One line: the file name, page count, letter size.
- What changed: amounts simplified, how many cups to set out.
- Print tip: 100% / Actual size, single-sided. Cut the labels before starting.
- One next step at most.

## Don'ts
- Don't show bowl assignments or station colors before the cooking steps.
- Don't let two ingredients share a cup. One cup = one label = one ingredient.
- Don't put two actions in one step.
- Don't rely on color alone to carry meaning.
- Don't include story text, nutrition facts, or ads from the source.
```
