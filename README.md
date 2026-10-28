scripture-accuracy

A Claude skill that checks Bible references in your writing before you publish or present it.

Give it an article, a talk script, a slide deck, or web copy. It finds every verse, checks the wording against your chosen translation, and tells you what to fix.

Why this exists

Faith writing runs on trust. A skeptical reader needs one reason to dismiss the whole piece, and a believing reader winces at a verse credited to the wrong person.

These mistakes are easy to make and easy to miss:

A verse credited to Jesus that Paul wrote
A quote that blends two translations
A verse trimmed so the sentence says something it doesn't
A promise given to one audience, applied to everyone
A "verse" that isn't in the Bible at all

AI models know a lot of Scripture, but they don't automatically verify it, hold one translation steady, or catch decontextualized use. This skill builds that check into the workflow so it happens every time.

I built it while preparing a talk and a series of articles on faith and the design workplace, where every verse in front of an audience had to be right.

What it does

For every Scripture reference in a piece, it:

Classifies it as a quotation, a paraphrase, or an allusion, and makes sure each is signaled honestly.
Verifies the wording against the actual text of your translation, not memory.
Standardizes the citation (book, chapter:verse, translation) in one consistent style.
Checks the speaker and the audience the verse was written to.
Flags truncation that changes the meaning.
Checks context (literary, historical, theological) and adds a short note when it helps.
Flags mixed translations and offers corrected wording.
Looks up attribution requirements for the translation you're quoting.
Handles web use: clean markup, accessible presentation, no keyword stuffing.
What you get back

A short summary line, then a table:

Where	Reference	Type	Status	Issue	Fix
Slide 25	Romans 1:16	Quotation	Fix attribution	Introduced as "Jesus says," but Paul is the speaker	"Paul writes in Romans 1:16..."

Statuses: OK, Fix wording, Wrong translation, Fix reference, Fix attribution, Context, Unverified.

Below the table you get corrected text ready to paste. It doesn't rewrite anything that didn't need changing.

Settings

Open SKILL.md and edit these lines:

Default translation: NIV
Citation style: John 3:16 (NIV)
Lean: accessible web and article use by default, formal register for study material

You can also name a translation in the request ("check these against the ESV"). The skill picks the translation in this order: the one you name, the one your piece already uses, the default, then it asks.

Install
Claude Code: put the scripture-accuracy folder in ~/.claude/skills/ (all projects) or .claude/skills/ (one project).
Claude apps: zip the folder so scripture-accuracy/ is at the top level, then upload it in your skills settings.
Use it

Just ask:

"Check the Scripture in this article."
"Verify the verses in my slides against the ESV."
"Format these citations for my website."
"Is this verse being used in context?"
Structure
scripture-accuracy/
├── SKILL.md
└── references/
    ├── citation-styles.md      styles, formatting rules, translation abbreviations
    ├── context-checks.md       context checklist and commonly stretched verses
    └── translation-notes.md    formal vs. dynamic translations, choosing for an audience
Limits
It needs web access to verify verses. Without it, references come back marked Unverified instead of guessed.
It checks accuracy, not your message. It looks at how Scripture is handled, not whether the sermon is good.
Context flags are judgment calls. It states the gap and you decide.
It doesn't rule on disputed theology. Where traditions read a passage differently, it says so and points you to your pastor or a trusted commentary. No denominational lens is built in. If you want one, state it and the skill will apply it as a constraint.
Copyright terms change. It looks up the current notice for your translation. Confirm with the publisher before you publish.
Contributing

Issues and pull requests are welcome. Good additions: more commonly misused verses, citation styles for specific publishers, and translation notes for languages other than English.

License

MIT

Author

Tony Lopez (@theboringuxer)
