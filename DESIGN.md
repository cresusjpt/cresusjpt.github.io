---
name: Jean-Paul Tossou
description: A personal site drawn as one technical drawing sheet, graphite on cool white, cyanotype at night.
colors:
  papier: "#f6f7f5"
  encre: "#16191c"
  encre-2: "#4b545b"
  trait: "#c3cacf"
  reprise: "#c4122f"
  sur-reprise: "#ffffff"
  chaine: "#1d6a57"
  papier-nuit: "#0d2e4d"
  encre-nuit: "#e9f1f8"
  encre-2-nuit: "#a8c0d4"
  trait-nuit: "#2d587c"
  reprise-nuit: "#f3c14b"
  chaine-nuit: "#94d6c4"
typography:
  display:
    fontFamily: "Osifont, Arial Narrow, sans-serif"
    fontSize: "clamp(2.5rem, 1.2rem + 4vw, 4.75rem)"
    fontWeight: 400
    lineHeight: 1.02
  headline:
    fontFamily: "Osifont, Arial Narrow, sans-serif"
    fontSize: "clamp(1.9rem, 1.3rem + 1.7vw, 2.75rem)"
    fontWeight: 400
    lineHeight: 1.08
  title:
    fontFamily: "Osifont, Arial Narrow, sans-serif"
    fontSize: "1.6rem"
    fontWeight: 400
    lineHeight: 1.15
  title-text:
    fontFamily: "Atkinson Hyperlegible Next, system-ui, sans-serif"
    fontSize: "1.25rem"
    fontWeight: 700
    lineHeight: 1.3
  lead:
    fontFamily: "Atkinson Hyperlegible Next, system-ui, sans-serif"
    fontSize: "1.25rem"
    fontWeight: 400
    lineHeight: 1.55
  body:
    fontFamily: "Atkinson Hyperlegible Next, system-ui, sans-serif"
    fontSize: "1.125rem"
    fontWeight: 400
    lineHeight: 1.65
  lettering:
    fontFamily: "Osifont, Arial Narrow, sans-serif"
    fontSize: "1.1rem"
    fontWeight: 400
    lineHeight: 1.3
  label:
    fontFamily: "Osifont, Arial Narrow, sans-serif"
    fontSize: "0.85rem"
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: "0.04em"
  code:
    fontFamily: "ui-monospace, SF Mono, Menlo, Consolas, monospace"
    fontSize: "0.9rem"
    fontWeight: 400
    lineHeight: 1.6
rounded:
  none: "0"
  balloon: "50%"
spacing:
  marge: "clamp(.5rem, 1.5vw, 1.25rem)"
  gouttiere: "clamp(1.25rem, 4vw, 3.5rem)"
  bloc: "clamp(3.5rem, 8vw, 6.5rem)"
  largeur: "76rem"
  mesure: "42rem"
components:
  button-primary:
    backgroundColor: "{colors.reprise}"
    textColor: "{colors.sur-reprise}"
    typography: "{typography.lettering}"
    rounded: "{rounded.none}"
    padding: ".75rem 1.35rem"
    height: "3.1rem"
  button-primary-hover:
    backgroundColor: "{colors.encre}"
    textColor: "{colors.papier}"
  button-outline:
    backgroundColor: "transparent"
    textColor: "{colors.encre}"
    typography: "{typography.lettering}"
    rounded: "{rounded.none}"
    padding: ".75rem 1.35rem"
    height: "3.1rem"
  button-outline-hover:
    backgroundColor: "{colors.encre}"
    textColor: "{colors.papier}"
  nav-link:
    textColor: "{colors.encre}"
    typography: "{typography.lettering}"
    padding: ".75rem 1.35rem"
  nav-link-hover:
    backgroundColor: "{colors.encre}"
    textColor: "{colors.papier}"
  nav-contact:
    backgroundColor: "{colors.reprise}"
    textColor: "{colors.sur-reprise}"
  field:
    backgroundColor: "transparent"
    textColor: "{colors.encre}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: ".35rem .9rem .8rem"
  balloon:
    textColor: "{colors.encre}"
    rounded: "{rounded.balloon}"
    size: "1.8rem"
  balloon-active:
    backgroundColor: "{colors.reprise}"
    textColor: "{colors.sur-reprise}"
  table-head:
    textColor: "{colors.encre}"
    typography: "{typography.label}"
    padding: ".55rem .75rem"
  fiche-label:
    textColor: "{colors.encre-2}"
    typography: "{typography.label}"
  fiche-value:
    textColor: "{colors.encre}"
    typography: "{typography.body}"
  cartouche-caption:
    textColor: "{colors.encre-2}"
    typography: "{typography.label}"
  cartouche-value:
    textColor: "{colors.encre}"
    typography: "{typography.lettering}"
    padding: ".45rem .8rem .55rem"
---

# Design System: Jean-Paul Tossou

## Overview

**Creative North Star: "The Drafting Sheet"**

Every page is one sheet of a technical drawing set. The viewport is framed by a thick ink border inset from the screen edge, a zone ruler numbered 1 to 8 runs across the top, a title strip carries the name and navigation, and a title block (cartouche) closes the sheet as the footer, with drawn-by, revision, folio, title, date and scale cells. Content between those borders behaves like drawing content: parts lists, revision tables, section views, dimension lines, circled balloons. Nothing floats, nothing glows; hierarchy comes from line weight, lettering and position on the sheet.

The palette is drafting material, not brand color. Light mode is a cool white sheet with graphite ink and one red redline reserved for the action and the active state. Dark mode is not an inverted theme but a different print process: a cyanotype blueprint, white lines on deep blue, where the redline becomes yellow because red cannot reach AA on the blue. Type splits along the same line as a real drawing: ISO 3098 lettering (Osifont) for everything that is drawn on the sheet (headings, labels, table heads, navigation, buttons, balloons), Atkinson Hyperlegible Next for everything meant to be read at length.

The system rejects the dark neon developer portfolio and its logo grids: stacks are named in lettering, never shown as logos, and the dark mode is a blueprint, not a terminal.

**Key Characteristics:**
- One sheet frame per page: 2px ink border inset by the margin, zone ruler, title strip, cartouche footer.
- Two line weights only, thin (1px) and thick (2px), used with ISO meaning.
- Square corners everywhere; the only circles are balloons.
- One action color (redline) that changes hue per print process, never a second accent.
- Opposed 45° hatching marks cut material, in the section view (A-A) and in every mini-section (project rows, mission register).
- The five layers of the section view (1 objet connecté, 2 liaison, 3 services, 4 données, 5 applications) are the site's index: the same balloon numbers key the parts list, the trade rows, the mini-sections and the legend.
- Depth is never shadow; it is line weight and hatching.

## Colors

Drafting materials: a sheet, two inks, a construction line, and one redline; each has a light (sheet) and a dark (cyanotype) value swapped by `prefers-color-scheme`.

### Primary
- **Redline Red** (`reprise`, light): the single action color. Primary button, Contact tab in the navigation, active-nav underline, focus ring (3px outline, 3px offset), text selection, link hover, keyword color in code, the latest revision triangle, active balloon and parts-list row, the dimension line when the "Architecture" row is hovered, the invalid-field label and error status, and the "Note" caption of a blockquote.
- **Blueprint Yellow** (`reprise-nuit`, dark): the same role on the cyanotype sheet. It is not a second accent; it is the redline in the other print process.

### Secondary
- **Drafting Green** (`chaine` / `chaine-nuit`): strings and numbers in syntax-highlighted code only. Nowhere else.

### Neutral
- **Cool Drafting White** (`papier`) / **Cyanotype Blue** (`papier-nuit`): the sheet. Page background, balloon fill, text on inverted (inked) surfaces.
- **Graphite Ink** (`encre`) / **Blueprint White** (`encre-nuit`): primary text and every thick line: sheet border, table frames, section rules, button outlines.
- **Soft Graphite** (`encre-2`) / **Faded Line Blue** (`encre-2-nuit`): secondary text: leads, metadata, dates, table "material" column, label captions in the cartouche, placeholders.
- **Construction Line** (`trait`) / **Grid Blue** (`trait-nuit`): thin dividers only (row separators, block top rules, ruler ticks). Never text.

Derived mixes: a red veil (`reprise` at 16% over transparent) tints the hovered parts-list row and the matching zone in the section view; code backgrounds are `encre` at 5% over `papier`.

### Named Rules
**The One Redline Rule.** The redline marks the action and the current state, nothing else. Filled red is limited to the Contact tab and at most one primary button per view; everything else red is a thin line, a focus ring, a hover response or the latest revision mark.

**The Print Process Rule.** Dark mode swaps the whole material set at once (sheet, inks, line, redline). Never ship a dark value without its light twin, and never let the red survive onto the blue sheet.

## Typography

**Display Font:** Osifont (ISO 3098 lettering, with Arial Narrow, sans-serif)
**Body Font:** Atkinson Hyperlegible Next (variable 200-800, with system-ui, sans-serif)
**Label/Mono Font:** Osifont for labels; ui-monospace stack for code only

**Character:** Osifont is the stencil lettering of the drawing, narrow and mechanical; Atkinson is the legible note written beside it. The pairing follows what is drawn versus what is read.

### Hierarchy
- **Display** (Osifont 400, `clamp(2.5rem, 1.2rem + 4vw, 4.75rem)`, 1.02): page H1s, max ~16ch. Home H1 runs slightly smaller (`clamp(2.4rem, 1.1rem + 3.4vw, 4.25rem)`), note H1 smaller still (`clamp(2.2rem, 1.3rem + 3vw, 3.6rem)`, 1.05).
- **Headline** (Osifont 400, `clamp(1.9rem, 1.3rem + 1.7vw, 2.75rem)`, 1.08): section H2s; in prose `clamp(1.6rem, 1.3rem + 1vw, 2rem)`, 1.15.
- **Title** (Osifont 400, 1.6rem, 1.15): project names in the project list and trade names in the trade rows.
- **Title Text** (Atkinson 700, 1.25rem, 1.3): default H3, note titles, prose subheads.
- **Lead** (Atkinson 400, 1.25rem, 1.55, `encre-2`): the paragraph under an H1 or H2, 40-52ch.
- **Body** (Atkinson 400, 1.125rem, 1.65): running text; article measure 42rem, summaries 60-62ch. Tables, sheets and excerpts step down to 1rem.
- **Lettering** (Osifont 400, 1-1.15rem): navigation, buttons, arrow links, stack lists, legends, figure captions, parts-list designations, trade proof lines, register row heads, cartouche values, note numbers (NT-001).
- **Label** (Osifont 400, 0.72-0.9rem, 0.04-0.05em, uppercase): table heads, form field labels, sheet (fiche) labels, stacked-register labels, cartouche cell captions, contact channel names, the "Note" header of a blockquote.

### The Ramp (literal steps in the stylesheet)
The shipped stylesheet uses exactly these sizes; a new rule picks one of them rather than inventing a neighbour.

- **0.72rem**: cartouche cell captions.
- **0.75rem**: zone ruler numerals.
- **0.85rem**: table heads (parts list, register, revisions, prose tables), form labels, sheet labels, stacked-register labels, signature role line, legend balloon numerals.
- **0.88em**: inline code, relative to its paragraph.
- **0.9rem**: contact channel names, "À préciser" marks, revision triangle letters, blockquote "Note" caption, code blocks.
- **0.95rem**: project period, note date and reading time, portrait caption, colophon, review stamp.
- **1rem**: table body text (parts list, register, prose tables), sheet values, stack lists, legends, balloon numerals, note excerpts, form status, phone navigation.
- **1.05rem**: note numbers, article metadata, cartouche values.
- **1.1rem**: navigation, arrow links, parts-list designations, figure captions, trade proof lines, form field values, previous/next note links.
- **1.125rem**: body.
- **1.15rem**: buttons, register row heads.
- **1.25rem**: lead, Atkinson H3.
- **1.4rem**: signature name in the title strip.
- **1.5rem**: name cell of a cartouche.
- **1.6rem**: project and trade names.
- **Clamps**: H1 `clamp(2.5rem, 1.2rem + 4vw, 4.75rem)`, home H1 `clamp(2.4rem, 1.1rem + 3.4vw, 4.25rem)`, note H1 `clamp(2.2rem, 1.3rem + 3vw, 3.6rem)`, H2 `clamp(1.9rem, 1.3rem + 1.7vw, 2.75rem)`, prose H2 `clamp(1.6rem, 1.3rem + 1vw, 2rem)`.
- **Inside the section view** (SVG user units, scaled with the drawing): balloon numerals 18, dimension lettering 13.5 with 0.06em tracking.

Lettered rows set tighter leading (1.2-1.3) because they are short lines on a drawing; anything that can wrap (cartouche values, register row heads, note titles) keeps at least 1.3. Reading text never goes below 1.45.

### Named Rules
**The Drawn Versus Read Rule.** If it would be lettered on a real drawing (heading, label, designation, reference, dimension), it is Osifont. If it is a sentence to read, it is Atkinson. Osifont never sets a paragraph.

**The Ramp Rule.** Sizes come from the ramp above. Two steps 0.05rem apart (1.05 and 1.1, 0.9 and 0.95) are not interchangeable: each marks a role, so a new element takes the step of the role it shares.

**The Upright Ink Rule.** Headings are weight 400; emphasis comes from size and lettering, not bold. Bold (700) belongs to Atkinson H3s and `strong`.

## Layout

The sheet is a full-height flex column: inset by `marge` (`clamp(.5rem, 1.5vw, 1.25rem)`) on all sides, framed by a 2px ink border, with `main` stretching between the title strip and the cartouche. The zone ruler is an 8-column grid (4 columns under 44rem). Content sits in a centered column `min(100% - 2 * gouttiere, 76rem)`; articles narrow to the 42rem measure.

Sections (`bloc`) are separated by a thin construction-line top rule and padded `clamp(3.5rem, 8vw, 6.5rem)` vertically. Section headers put the H2 and its side note on one baseline, wrapped and space-between. Lists of projects, notes and contact channels open with a thick ink rule and separate rows with thin construction lines, like a schedule on a drawing.

The home's first view is a two-column assembly (text and parts list left at 1.12fr, section view right at 1fr). On desktop the drawing is capped to `calc(100dvh - 16rem)` so the whole section view and the parts list fit in the first screen; the cap is lifted (and the drawing limited to 34rem wide) once the assembly stacks. Projects are a three-track row (3rem mini-section, up to 15rem name, rest summary). Trades (métiers) are a three-track row: 3rem column of layer balloons, 1.5fr body (name, proof line, text), 1fr sheet. The mission and education register is a full-width framed table with a 27% lettered first column. Notes are a four-track row (number, date, title, reading time) with the excerpt under the title. A case study opens with a 4-cell title-block strip under its H1 and keeps its prose blocks at the 42rem measure.

Breakpoints: at 60rem, all two-column grids stack, the cartouche drops under the colophon and the trade sheet moves under the trade text (2.6rem balloon column); at 44rem, the navigation becomes a full-width 4-cell strip, forms go single-column, the project row folds its summary under the name, the case-study title block becomes 2 by 2, and tables restack as described under Components (parts list, revisions, register). Reduced motion removes all transitions and the plotter animation. Print hides the ruler, navigation and colophon and drops the sheet border.

**The Stacked Table Rule.** A table that changes `display` on phones keeps explicit ARIA roles (`table`, `rowgroup`, `row`, `columnheader`, `rowheader`, `cell`) in its markup and a visually hidden caption, so its semantics survive the restack. Its header row is visually hidden, never removed; where a cell loses its column context, the label is repeated from a `data-titre` attribute in label lettering.

## Elevation & Depth

Flat. There is no `box-shadow` used for elevation anywhere in the system; the only inset box-shadow is the 2px redline focus frame on a form field. Depth is conveyed the way a drawing conveys it: line weight (thick for outlines and frames, thin for subdivisions), opposed 45° hatching for cut material, reduced opacity (0.22) for pencil construction lines, and inversion (ink fill, paper text) for hovered navigation and buttons.

### Named Rules
**The Line Weight Rule.** Two weights: thin (1px) and thick (2px). Thick draws outlines and frames (sheet, tables, forms, buttons, list tops, the title strip); thin draws subdivisions (cells, rows, ruler ticks). In SVG drawings, visible edges run 1.8-2.5, detail lines 1.25-1.5, hatching 1. No third CSS weight except the 1.5px balloon and mini-section strokes (1.25px for the smaller mini-sections inside the register).

**The Hatch Rule.** Cut material is hatched at 45°, and neighbouring parts take opposite directions (45° against -45°), with spacing indicating the part (4.5, 7, 10 units). The project mini-section applies the same rule with alternating 1px/4px gradients.

## Shapes

Every interface corner is square (radius 0), including inputs, selects, buttons and tables. Objects drawn inside a section view keep their real geometry (the phone's rounded body, the browser's address bar, round leader dots); that is drawing content, not interface shape. The only round interface form is the balloon (`border-radius: 50%`, 1.8rem, 1.5px stroke, numeral in Osifont), used to reference parts between the parts list, the legend and the section view. Revision markers are inked triangles (clip-path polygon). Arrows are drawn, not glyphs: a 28x10 SVG with a 1.6 stroke shaft and a filled head, mirrored for "previous"; the select chevron is two thick borders rotated 45°. Dashed construction outlines mark empty states.

## Components

### Buttons
Lettered, framed, square: a button is a labelled box on the sheet.
- **Shape:** square (0), 2px ink frame, min height 3.1rem, padding `.75rem 1.35rem`, Osifont 1.15rem, optional drawn arrow at 1.6em.
- **Primary:** redline fill and frame, `sur-reprise` text. One per view.
- **Hover / Focus:** inverts to ink fill with paper text (0.2s color transition); focus is the global 3px redline outline offset 3px.
- **Outline:** transparent with ink frame; hover fills with ink.
- **Arrow link:** Osifont 1.1rem text plus drawn arrow, no underline until hover.

### Cards / Containers
There are no cards. Grouping is done with ruled lists and framed tables: thick ink rule on top, thin construction-line row separators, no background, no radius, no shadow. Row hover may tint with ink at 4% or the red veil.

### Inputs / Fields
The contact form is a title-block grid: a 2px framed two-column table of cells divided by 1px ink lines, each cell holding an uppercase Osifont label above a borderless, transparent field (1.1rem). Focus draws a 2px inset redline frame around the whole cell. An invalid field after interaction turns its label red and appends "· à compléter". The select uses a drawn chevron. Submit sits in a full-width bottom row with a polite status line.

### Navigation
The title strip: signature block (name in Osifont 1.4rem, role in secondary ink) on the left, navigation cells on the right, each cell separated by a 1px ink line, Osifont 1.1rem. Hover inverts the cell. The current page gets a 2px redline underline offset 0.4em. Contact is the permanent redline-filled cell. Under 44rem the navigation becomes four equal cells across the full width.

### Parts List (signature)
The nomenclature table: 2px frame, uppercase Osifont heads, columns Rep. / Désignation / Ce que j'y fais ("Ce que j'ai construit" on a case study) split by 1px ink lines. Designations are lettered at 1.1rem; the third column is reading text at 1rem. Each row carries a balloon; hovering a row tints it with the red veil, fills its balloon red, and highlights the matching zone and balloon in the section view. A last "Architecture" row carries a drawn double arrow in its balloon and, on hover, turns the vertical dimension line red. The home version keeps one line per row (rows padded 0.4rem, text kept under 45 characters) so it fits the first screen; the detailed variant (`detaillee`) pads rows 0.85rem and top-aligns them for paragraph-length cells. On phones the header row is hidden and each row becomes a two-column grid: the balloon centered on the left spanning two lines, the designation above its text on the right.

### Section View (signature)
One shared drawing (`_includes/coupe.html`, parameters `titre` for the accessible title and `legende` for the caption), used on the home page and the Lockey You case study. An inline SVG (viewBox `0 -64 440 606`) drawn in `currentColor`, five layers from bottom to top: 1 objet connecté (board, sensor, module), 2 liaison (radio waves and exchanges), 3 services (server rack), 4 données (a pipeline in section: blind flange, gauge, flange, filter, feeding a warehouse tank), 5 applications (phone and browser seen beyond the cutting plane). Parts have thick visible edges, opposed hatching, dimension lines with filled markers, leader lines ending in balloons, pencil construction at 0.22 opacity. A vertical dimension spanning the full height reads "ARCHITECTURE". Captioned by a figcaption over a 2px rule (the `legende` text left, "Éch. 1:1" right). On first paint it is inked by a plotter reveal (clip-path from bottom, 2.2s, `cubic-bezier(.16, 1, .3, 1)`); without the reveal it stays fully inked.

### Title Block (signature)
The footer cartouche: a table bordered in ink with tiny uppercase captions (0.72rem, 0.05em) over Osifont values: drawn by, revision, folio (`01 / 05`), title, date, scale 1:1, and a links row. Every page sets its folio. The same grammar serves two framed variants: the case-study strip (`cartouche-projet`, four equal cells: role, since, status, site; 2 by 2 on phones) under a case study's H1, and the company block (`cartouche-societe`, two columns plus a full-width row) beside the Saltech section.

### Trade Rows (métiers)
Three ruled rows under a thick ink rule, one per trade. Left: the balloons of the section-view layers the trade covers, stacked. Middle: the trade name in Title lettering (1.6rem), a proof line under it in secondary-ink lettering (1.1rem: a date, a duration, a role), then the reading text at 62ch. Right: a sheet (fiche). The proof line sits under the name and states a fact; it never sits above a heading as a category label.

### Sheet (fiche)
A definition list read like one column of a title block: thick ink rule on top, each label/value pair separated by a thin construction line, the label in uppercase label lettering (0.85rem, secondary ink), the value in reading text (1rem, 1.45).

### Register (registre)
The missions and education table: thick frame, uppercase label heads, lettered row heads (1.15rem) for the entity or school, three columns (Pour, Période, Travail), all in primary ink. The work cell opens with a small mini-section (1.75rem wide, 1.25px strokes) of the layers touched. On phones each row becomes a block: the row head first, then each cell under its label repeated from the header; empty cells disappear.

### Prose Block
Inside a wide page, a block of article prose (`bloc-prose`) keeps the 42rem measure and the article rhythm (1.2em between elements).

### Revision Table
Same frame as the parts list; each revision index is an inked triangle, the latest one redline. On phones the header row is hidden and each row restacks: the triangle on the left spanning two lines, the date above the description on the right.

### Review Devices (temporary)
Two devices exist only while `site.hypotheses` is true, to mark copy awaiting the owner's confirmation: the rotated "À valider" stamp (`tampon`) and the red uppercase "À préciser" lettering (`a-preciser`, 0.9rem) that fills a register cell whose fact is missing. Neither is part of the system; both disappear when the hypotheses are confirmed. Do not reuse them as decorative badges, and do not count their red against the One Redline Rule.

## Do's and Don'ts

### Do:
- **Do** frame every page as one sheet: inset 2px border, zone ruler, title strip, cartouche footer with a folio.
- **Do** set anything lettered on a drawing (headings, labels, table heads, navigation, buttons, balloons, references) in Osifont at weight 400, and all reading text in Atkinson Hyperlegible Next.
- **Do** use only the thin (1px) and thick (2px) line weights, thick for frames and thin for subdivisions.
- **Do** hatch cut material at 45° with opposite directions between neighbouring parts.
- **Do** reserve the redline for the action, the current state, focus and selection, and let it become yellow on the cyanotype sheet.
- **Do** draw arrows, chevrons and markers as SVG or borders in `currentColor`.
- **Do** key every layer reference to the section view's five balloons (1 objet connecté to 5 applications), and every mini-section to the same five layers.
- **Do** give any table that restacks on phones explicit ARIA roles and a hidden caption.
- **Do** take font sizes from the ramp in Typography.
- **Do** name a reference in lettering as an entity or a sector with the work done (register columns Pour, Période, Travail); no contractual frame on the site (reference policy in PRODUCT.md).

### Don't:
- **Don't** add rounded corners, cards with backgrounds, or shadows for elevation to the interface; the only interface radius is the balloon circle (drawn objects inside a section view keep their own geometry).
- **Don't** show technology stacks as logo grids or badges; name them in lettering.
- **Don't** turn dark mode into a neon terminal; it is a blueprint (deep blue sheet, white lines, yellow redline).
- **Don't** introduce a second accent color; the green is confined to code strings and numbers.
- **Don't** keep red on the blue sheet, or use the construction-line color for text.
- **Don't** set paragraphs in Osifont or bold the lettered headings.
- **Don't** treat the rotated "À valider" stamp or the "À préciser" lettering as components; they are temporary review markers.
- **Don't** set an em dash in site copy; ranges take an en dash with spaces ("2020 – 2021").
- **Don't** show client logos; references stay lettered text.
