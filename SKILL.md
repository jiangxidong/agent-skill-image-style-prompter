---
name: image-style-prompter
description: Style-name direction for image generation — recommends named design styles (Wabi-Sabi, Neo-Brutalism, Y2K…) and two-style combinations, then writes a copy-paste prompt for an external image model (GPT Image, Midjourney, Nano Banana, etc.). Use when the user wants an image prompt written or improved, wants style options for an image, or names a style to apply.
---

# Image Style Prompter

A style name beats a vibe. "Clean" points the image model at ten looks; "Utilitarian" points it at one. This skill turns a fuzzy image request into a named style choice, then into a prompt the user pastes into another image model. It writes prompts and does not render images.

Reference files:

- [`references/image-types.md`](references/image-types.md): per image type, what to ask, what to lock, what goes wrong, and which style families fit.
- [`references/styles.md`](references/styles.md): the style library, grouped into families, each style with its **style DNA**, misfires, and pairings.

Talk with the user in their language. Write the final prompt in English, keeping any in-image text verbatim in its original language.

## 1. Brief

Pull from the user's message: subject, image type, aspect ratio, in-image text, and whether a reference image is attached. Match the image type to its section in `image-types.md` and read that section; its **Ask** line names the gaps worth filling for that type.

If essentials are missing, ask one round of at most 3 questions, covering the gaps that change the image most. Fill everything else with sensible defaults instead of asking.

Done when subject, image type, and aspect ratio are known, and in-image text is either given verbatim or confirmed as none.

## 2. Named style?

If the user already named a style (or two), skip recommending: look it up in `styles.md` and go to step 4. A style missing from the library is still valid; build its DNA from your own knowledge using the same fields.

## 3. Recommend

Read `styles.md`. Shortlist from the families the image-types section marks as fitting, then pick **4 options that spread** across different families, so the user sees the real range rather than four versions of one safe idea:

- Default: 2 single styles + 2 combinations. When the brief is already narrow (e.g. "premium skincare hero shot"), use 3 singles + 1 combination.
- Option 1 is the safe pick; append ` (Recommended)` to its label.

Present them with `AskUserQuestion`, `multiSelect: true`, header `Style`:

- **label**: the style name, or `Primary + Accent` for a combination.
- **description**: one sentence on what the image will look like, plus why it fits this brief.
- **preview**: the style DNA: palette, type, texture, signature motifs (for a combination, which comes from which).

The built-in "Other" field handles the rest: "more" or similar means a fresh batch of 4 with no repeats; a typed style or combination is taken as the user's pick. Without `AskUserQuestion`, show the same 4 as a numbered list and let the user reply with numbers.

Done when the user has picked at least one option.

### Combinations

A combination is **primary + accent**, never a 50/50 blend. The primary sets layout, palette, and type; the accent contributes texture and motifs. Name the split explicitly (e.g. "Wabi-Sabi palette and negative space, with Scrapbook washi tape and handwritten notes"). Check the **Pairs** and **Clashes** lines in `styles.md`; a clash is fine only when the tension is the point and you say so.

Cap at two styles. If the user asks for three, say once that a third usually muddies the result; if they insist, add the third as a faint accent of one or two motifs.

## 4. Write the prompt

Fill this skeleton. Each line is one or two sentences; keep the whole prompt tight.

```
Subject: <what the image is and its main subject>
Composition: <layout, viewpoint, hierarchy, focal point>
Style: <Primary>[ with <Accent> accents] — <which elements come from each>
Palette & Materials: <colors, textures, finishes, lighting, drawn from the style DNA>
Text: "<exact text>" — <placement and hierarchy>; no other text.
Reference: <what to keep from the attached image; what to restyle>
Format: <ratio and orientation>, <deliverable, e.g. finished single poster>
Avoid: <3–6 short items>
```

- **Content blocks** are Subject, Composition, Text, Reference, Format. **Style blocks** are Style, Palette & Materials, and the style half of Avoid.
- Text: when the image has no text, write `Text: none — no lettering in the image.`
- Reference: include the line only when the user supplied a reference image.
- Format: state the ratio in words ("3:4 vertical"). Add model-specific syntax (`--ar 3:4`, `--style raw`) only when the user named that model.
- Avoid: combine the image type's **Avoid** items with the style's **Misfire** line.

Deliver, in this order:

1. One summary line in the user's language: style choice, image type, ratio.
2. The prompt in a fenced code block.
3. Up to 2 optional tweaks ("for a busier feel, add …").

When the user picked several options, write one prompt per option. Keep the content blocks word-for-word identical and the image-type Avoid items fixed, and swap only the style blocks, so the renders compare fairly.

## 5. Revise

When the user comes back with feedback on the result:

- A fix within the current style ("too plain", "wrong colors", "text garbled"): edit only the block that causes it, re-output the full prompt, and name the block you changed.
- A style swap: keep every content block, then either apply the named style or return to step 3 for a fresh set of 4.
