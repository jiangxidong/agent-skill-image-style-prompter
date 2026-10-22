# Image Types

Thirteen image types. Match the request to one and read its section:

- **Ask** lists the gaps worth one question each (step 1 caps the round at 3).
- **Lock** lists what the prompt must pin down in its content blocks.
- **Avoid** lists the type's typical failures; they go into the prompt's Avoid line.
- **Families** lists the style families in `styles.md` that fit naturally. They are a starting shortlist; one option outside them keeps the spread honest.

Adapted from the awesome-gpt-image-2 template handbook, rewritten for style-first prompting.

## UI & Interfaces

App screens, dashboards, web pages, social-platform screenshots, livestream overlays.

- **Ask:** Which platform (iOS, Android, web, a named social app)? Which screen and which key elements? The exact UI copy?
- **Lock:** platform chrome (status bar, tab bar, nav), screen hierarchy top to bottom, every visible label, light or dark mode.
- **Avoid:** lorem ipsum or placeholder text, garbled or tiny type, generic phone-mockup look, wrong-platform navigation.
- **Families:** Structured & Functional, Retro-Digital, Dreamy & Ethereal (glass), Bold & Loud (neo-brutalist UI).

## Infographics & Charts

Explainers, process flows, timelines, knowledge cards, scale diagrams (micro to macro).

- **Ask:** What are the 3–6 modules or stages? Who is the audience? Exact labels?
- **Lock:** module count, flow direction, one icon plus a short label per module, connectors.
- **Avoid:** paragraphs of body text, unbounded module count, identical-looking stages, unreadable labels.
- **Families:** Structured & Functional, Bold & Loud, Handmade & Collage (sketch, rebus), Cute & Character.

## Posters & Typography

Event posters, covers, thumbnails, campaign key visuals, invitations, typographic posters where the words are the image.

- **Ask:** Exact headline and secondary lines? What is the main visual? Is the lettering itself the hero?
- **Lock:** headline wording and spelling, text hierarchy (headline > subhead > small print), main visual, single finished poster.
- **Avoid:** collage of several poster drafts, stray extra text or symbols, misspelled headline, default word-art effects.
- **Families:** any; posters carry every family. Lead with Bold & Loud, Classical & Ornate, or Retro-Digital for impact, Calm & Natural for restraint.

## Product & E-commerce

Hero product shots, packaging, listing images, selling-point layouts, recommendation cards.

- **Ask:** What is the product, its material and size? The selling points to label? Background scene or plain?
- **Lock:** product as the clear hero (state share of frame), material and finish, props (named and few), label text.
- **Avoid:** props that compete with the product, invented packaging text, distorted product shape, medical claims on beauty items.
- **Families:** Calm & Natural, Dreamy & Ethereal, Classical & Ornate (luxury), Bold & Loud (streetwear, snacks), Structured & Functional.

## Brand & Logo

Logo systems, brand boards, identity kits, multi-touchpoint mockups (cups, bags, signage, social).

- **Ask:** Brand name and positioning? Existing colors or fonts to keep? Which touchpoints to show?
- **Lock:** brand name spelling, palette (hex if known), type pairing, list of touchpoints, one shared visual rule across all panels.
- **Avoid:** unrelated logo variants, mixed campaign styles, misspelled brand text, too many touchpoints crowding the board.
- **Families:** Structured & Functional, Calm & Natural, Classical & Ornate, Bold & Loud.

## Architecture & Space

Interiors, building renders, store concepts, illustrated maps.

- **Ask:** Room or building type and size? Viewpoint? For maps: which landmarks, and label language?
- **Lock:** camera position, scale and proportions, materials, light source and time of day; for maps, landmark labels and relative positions.
- **Avoid:** impossible perspective, furniture at wrong scale, mislabeled or misplaced landmarks.
- **Families:** Calm & Natural, Rustic & Heritage, Classical & Ornate, Structured & Functional.

## Photography

Portraits, lifestyle, food, product photography, street candids, cinematic stills.

- **Ask:** Staged or candid? Subject and action? Setting and light?
- **Lock:** lens and framing (e.g. 35mm half-body), light direction, setting, action, believable small imperfections.
- **Avoid:** plastic over-smoothed skin, broken hands, studio-ad gloss on a candid, nonsense text on signs.
- **Families:** apply the style as **art direction** (set design, wardrobe, palette, lighting), never as graphic overlays. Calm & Natural, Dark & Dramatic, Rustic & Heritage, Retro-Digital (flash, film look).

## Illustration & Art

Editorial illustrations, picture-book pages, watercolor, ink, decorative art, style experiments.

- **Ask:** What is in the frame and where is the focal point? Medium (watercolor, gouache, ink, digital)? Space reserved for text?
- **Lock:** composition and focal point, subject, medium and stroke quality, level of finish.
- **Avoid:** style with no composition (the generic-wallpaper result), muddy focal point, inconsistent characters across a series.
- **Families:** any; illustration is where the full library shines. Handmade & Collage, Dreamy & Ethereal, and Classical & Ornate are strong defaults.

## Characters & Mascots

Character sheets, turnarounds, pose grids, mascots, 3D collectible toys, avatars.

- **Ask:** Identity anchors (hair, face, signature clothing or prop)? How many poses or views? Reference image?
- **Lock:** identity anchors repeated in every view, proportions (e.g. three-heads-tall chibi), pose count, grid layout, material for 3D.
- **Avoid:** outfit details drifting between poses, crowded grid, generic faceless toy, packaging text errors.
- **Families:** Cute & Character, Retro-Digital (pixel), Bold & Loud, Dark & Dramatic (fantasy).

## Scenes & Storytelling

Storyboard frames, key story moments, worldbuilding shots, brand story scenes.

- **Ask:** Who, where, when? What is the conflict or emotion the viewer should read?
- **Lock:** characters and their relation, location, time of day, the visible story clue, camera distance.
- **Avoid:** generic fantasy backdrop, decoration that says nothing about the story, the key clue left out of frame.
- **Families:** Dark & Dramatic, Dreamy & Ethereal, Rustic & Heritage, Retro-Digital (synthwave, cyber).

## History & Classical

Period scenes, scrolls, dynastic costume, poetry illustration, cultural heritage visuals.

- **Ask:** Which era or dynasty exactly? Format (handscroll, album leaf, poster)? Is historical accuracy required?
- **Lock:** era, costume and object references from that era, format, cultural tone.
- **Avoid:** mixed eras in costume or objects, stray modern items, fantasy effects passing as history.
- **Families:** Classical & Ornate, Calm & Natural (ink and negative space), Dark & Dramatic, Rustic & Heritage.

## Documents & Publishing

Report spreads, white-paper pages, manuals, catalogs, field-guide pages.

- **Ask:** Page size and spread or single page? What goes on each page (title, chart, table, diagram)? Exact headings?
- **Lock:** grid and columns, heading hierarchy, chart or diagram type, alignment to the grid.
- **Avoid:** walls of tiny text, charts floating off-grid, fake unreadable body copy presented as content.
- **Families:** Structured & Functional, Classical & Ornate (editorial luxury), Calm & Natural, Handmade & Collage (field-guide).

## Concept & Product Breakdown

Exploded views, R&D boards, concept product sheets, component callouts.

- **Ask:** Which components to show? Format (exploded view, iteration strip, spec row)? Exact callout labels?
- **Lock:** component list, callout labels (short), central hero render, controlled technical rendering.
- **Avoid:** vague scope, long labels, unclear relations between parts.
- **Families:** Structured & Functional, Retro-Digital, Handmade & Collage (conceptual sketch), Dark & Dramatic (steampunk).
