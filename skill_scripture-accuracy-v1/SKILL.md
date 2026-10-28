---
name: scripture-accuracy
description: Use this skill whenever Scripture is quoted, paraphrased, or referenced in writing, editorial work, articles, website copy, social content, study notes, talks, slides, or any published material. Triggers include requests to check a verse, verify wording, format a citation, add context notes, choose a translation, or prepare Scripture for web use, and any time the user is about to publish or present something with Bible references, even if they never say "check." Verifies wording against the chosen translation, completes and standardizes references, checks speaker and context, and keeps quotations, paraphrases, and allusions clearly signaled.
---

# Scripture Accuracy

Faith writing runs on trust. A wrong reference, a verse credited to the wrong speaker, or a verse bent away from its context gives skeptical readers a reason to dismiss the whole piece and gives believing readers a reason to wince. This skill makes sure every Scripture citation is precise, responsibly used, and consistently presented.

## Settings (edit these lines to change defaults)

- **Default translation:** NIV
- **Citation style:** `John 3:16 (NIV)`, with the translation abbreviation in parentheses
- **Lean:** accurate first, readable second. Default to accessible web and article use, and switch to a formal/academic register when the user says the piece is for study or publication in that setting.

## Choosing the translation

Decide in this order:

1. The translation the user names in the request.
2. The translation the piece already uses (check a few quoted verses; if most match one, that is the working translation).
3. The default above.
4. Ask once if the piece mixes translations roughly evenly and the user has not said which to standardize on.

Use one translation per piece. Mixed translations often mean a verse was copied from somewhere else without anyone noticing, so flag each verse that does not match and offer the corrected wording. When a more formal or more readable option would serve the audience better, say so briefly. Read `references/translation-notes.md` for that guidance.

## Process

1. **Extract every Scripture touchpoint** and note where it appears (slide, section, line). Classify each as a **quotation** (exact words), a **paraphrase** (the idea in other words), or an **allusion** (a passing echo). Quotations get quotation marks and an exact match. Paraphrases and allusions must be signaled so the reader is never led to think paraphrased words are the verse itself.
2. **Verify wording against the text, not memory.** Pull each verse from a reliable source (Bible Gateway, Bible.com, or the publisher's site) in the working translation using web search or fetch. If you cannot retrieve it, mark it Unverified instead of guessing.
3. **Complete and standardize the reference.** Require book, chapter:verse, and the translation abbreviation on first use in a piece. Keep one style throughout. Read `references/citation-styles.md` for styles, ranges, and abbreviations.
4. **Check reference and text match.** The cited passage should contain the quoted words.
5. **Check attribution.** Who is speaking, and to whom? "Jesus says..." in front of a letter by Paul is a common slip.
6. **Check truncation.** Shortening a verse is fine. A cut that changes what the sentence says is not. Flag it and, where helpful, expand the quote.
7. **Check context.** Work through `references/context-checks.md`. Flag verses used outside their literary, historical, or theological setting. Add a short context note when it helps the reader. Applying a verse is allowed. Claiming the verse itself says the application is the problem.
8. **Original-language notes, sparingly.** Add a Hebrew or Greek term only when the nuance changes how the verse reads, with a short plain-language explanation. Check the term and its meaning in a lexicon or reliable resource rather than recalling it from memory. If you cannot confirm it, leave it out.
9. **Cross-references.** Prefer the primary text over secondary summaries. Add a parallel passage or cross-reference only when it strengthens the point, and verify it like any other citation.
10. **Publishing requirements.** Most modern translations need an attribution notice and set quotation limits. Look up the current notice and limits on the publisher's permissions page for the working translation and give the user the exact text to paste. Older public-domain translations (such as the KJV in the US) generally need no notice, but tell the user to confirm for their country.

## Web and social use

When the output is for a website or social post:
- Use clean semantic markup: `<blockquote>` for quotations with a `<cite>` for the reference, not images of text or decorative text-in-graphics that screen readers cannot read.
- Keep the reference and translation next to the quote so it stays correct when copied or shared.
- Schema.org `Quotation` or `CreativeWork` markup is optional and only worth it when the page is genuinely quote-driven.
- Use the text for readers, not for keyword stuffing. A verse should appear because it serves the page, not because it ranks.
- Check color contrast and readable size on verse callouts.

## Report format

Start with one line: translation used, references checked, how many need action.

Then a table, one row per reference:

| Where | Reference | Type | Status | Issue | Fix |
|---|---|---|---|---|---|

Type: Quotation, Paraphrase, or Allusion. Status: **OK**, **Fix wording**, **Wrong translation**, **Fix reference**, **Fix attribution**, **Context**, **Unverified**.

After the table, give corrected text ready to paste for each "Fix" row, plus any context notes you recommend. Do not rewrite anything that did not need changing.

## Boundaries

- Never invent or reconstruct a verse. If a quote does not exist in the Bible, say so (for example "God helps those who help themselves").
- Context flags are judgment calls. State the gap and let the user decide. If the use is a reasonable application, say so and move on.
- Do not rule on disputed theology. Name the disagreement briefly and suggest a pastor or trusted commentary. No denominational lens is built in. If the user wants one, ask them to state it and apply it as a stated constraint.
- This is an accuracy check, not a sermon review. Critique how Scripture is handled, not the message.
- Keep the report direct and short. Lead with problems, and say plainly when something is fine.
