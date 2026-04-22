# Vault conventions

## Folder purposes

| Folder | What goes here | SR-tagged? |
|---|---|---|
| `es/` | Spanish notes, one per vocab item / grammar point | yes, `#sr/es` |
| `fr/` | French notes, same structure | yes, `#sr/fr` |
| `ja/` | Japanese notes | yes, `#sr/ja` |
| `zh/` | Chinese notes (doesn't exist yet, created at week 13) | yes, `#sr/zh` |
| `hanzi-kanji/` | Cross-linguistic CJK character study | yes, `#sr/cjk` |
| `concepts/` | Cross-language reference maps | **NEVER** |
| `inbox/` | Quick capture from commutes | no — these get processed into language folders |
| `templates/` | Copy-ready note formats | no |
| `resources/` | Curated external links and vaults | no |

## The SR tagging scheme

Install the **Spaced Repetition** plugin (by st3v3nmw). Configure:

- **Flashcard tag:** `#sr`
- **Separator:** `::`

With those settings, any line like `word::definition #sr/es` becomes a flashcard in the `es` sub-deck. Obsidian shows you the left side, you recall the right, and rate yourself.

## The one-card-per-note rule

One SR line per note, placed near the top on its own line. Don't stack five cards in one note — they'll review in clumps and overwhelm you. If a word has multiple meanings worth separate cards, make separate notes and link them.

## The French-Spanish bridge rule

When a Spanish note has a useful French cognate, include it in the note body as a reference, **not** in the SR prompt. Example:

```markdown
# trabajar

trabajar::to work #sr/es

FR cognate: *travailler*. Same root, just -er → -ar.
```

The card tests `trabajar → to work`, not `trabajar → travailler`. Putting French in the prompt would train translation-mediated retrieval (Spanish → French → meaning) which slows you down and corrupts both languages. The French line is only for the note's reader, i.e. future-you.

Same rule in reverse for French notes that cognate with Spanish.

## Filenames

- Use the target-language lemma as the filename: `trabajar.md`, not `to-work.md`.
- For Japanese, use kanji where possible: `稲妻.md`, not `inazuma.md`.
- For Chinese (later), same — `闪电.md`.
- Grammar points: descriptive kebab-case, language prefix optional, e.g. `ser-vs-estar.md` or `fr-passé-composé.md`.

## Rules

- **Don't polish notes.** A sloppy note reviewed beats a beautiful note never finished.
- **Delete bad cards.** If a card keeps failing and you can't figure out why, delete it and write a better one with more context. Don't grind through a broken card for weeks.
- **Concept notes never get `#sr` tags.** They exist to *navigate* between per-language notes, not to test anything.
