# The Plan

## Phase 1: Weeks 1–6 — Spanish and French alternating, Japanese ambient

### Why alternating?

Spanish and French are close enough that studying them in the same session causes interference — you'll reach for *avoir* when you mean *haber*, or *toujours* when you mean *siempre*. The mitigation is **time separation**: never fire both language networks in the same hour. Mon/Wed/Fri = Spanish. Tue/Thu = French. Weekends = light review only. Japanese is fine as a palette cleanser any day because it shares no grammar or roots with either.

### Weekly schedule

| Slot | Mon | Tue | Wed | Thu | Fri | Sat | Sun |
|---|---|---|---|---|---|---|---|
| Commute out (09:30, ~40 min) | LT Spanish | Coffee Break French | LT Spanish | Coffee Break French | LT Spanish | — | — |
| Lunch (12:00, 10 min) | ES SR review | FR SR review | ES SR review | FR SR review | ES SR review | — | — |
| 17:00 break (10 min) | JP ambient | JP ambient | — | JP ambient | JP ambient | — | — |
| Commute home (19:00, ~40 min) | Dreaming Spanish | InnerFrench | Dreaming Spanish | InnerFrench | News in Slow Spanish | — | — |
| Evening (20:00–21:00) | ES active | FR active | ❌ free | FR active | rest | 30 min mixed catch-up | 20 min SR only (mixed) |

**Total:** ~4 hrs Spanish, ~3 hrs French, ~45 min ambient Japanese, zero Chinese.

### Why this specific split

- **Language Transfer Spanish** on MWF mornings because it's the single best grammar foundation for Spanish and his method (pause + answer aloud) works in a car/train. Non-negotiable for weeks 1–6.
- **Coffee Break French** on T/R mornings because it assumes beginner knowledge and your French is already past that — you'll use it as revision-plus-extension rather than a ground-up course.
- **Dreaming Spanish / InnerFrench** home commute because they're comprehensible input you can mostly follow, building listening endurance without active work.
- **News in Slow Spanish Friday** as a weekly "can you follow current events?" checkpoint.
- **JP ambient** is deliberately not on Wednesday because Wednesday is fully off — infrastructure protection.

### What "active" means in each slot

- **LT / Coffee Break (commute):** listen. Pause and answer aloud when prompted (LT) or repeat phrases (CB). No notes during.
- **Dreaming Spanish / InnerFrench (commute):** listen. If a word jumps out three times across different episodes, note it in `inbox/` on your phone for tonight. Don't try to catch every word.
- **SR review (lunch):** open Obsidian → Spaced Repetition: Review flashcards. Ten minutes, hard stop. Deck alternates by day: `es` on MWF, `fr` on T/R.
- **Ambient Japanese (17:00 break):** Nihongo con Teppei, Japanese with Shun, or similar. Listen. No lookups, no cards. Ear training only.
- **ES active / FR active (evening):** rotate through three activities, one per evening, never all three:
  1. Process `inbox/` — take flagged words, expand into proper notes in `vault/es/` or `vault/fr/`, add SR line, delete from inbox.
  2. One grammar unit from LT / Coffee Break / a textbook.
  3. Write 3–5 sentences about your day in `vault/es/journal/` or `vault/fr/journal/`.

### The French-Spanish bridge

When adding a Spanish note for a word with a French cognate, include the French link in the note body (not in the SR prompt). Example in `vault/es/trabajar.md`:

```markdown
trabajar::to work #sr/es

FR: travailler (same root, -er → -ar)
```

This is just a human-readable reference. The SR card still tests Spanish→English, not Spanish→French. That's the interference-safe way to use your French.

When French grammar mirrors Spanish or diverges from it, note it in `concepts/` with `[[links]]` but no SR tag. See `concepts/ser-estar-être.md` as an example — French collapses ser/estar into *être*, Spanish splits it; worth remembering but not a flashcard.

### Rules

- **Wednesday is fully off.** Not "lighter" — off.
- **Don't add new SR cards on Saturday or Sunday.** Review only. This prevents the deck from growing faster than you can sustain.
- **Cap new cards at 10/day per language, 40/week per language.** More feels productive and isn't.
- **If you miss a day, skip it.** Don't "catch up." Doubling review load is how people quit.
- **Never run ES SR and FR SR in the same session.** Pick one per lunch slot. If you accidentally review both, expect increased interference that week.

## Phase 2 switchover: from week 7

Switchover happens at week 7 **if** you hit these criteria at the end of week 6:

- Spanish: can follow News in Slow Spanish at 1.0x speed and get the gist of every story.
- French: can follow InnerFrench without subtitles and describe the episode topic aloud afterwards.
- Journal: can write a 5-sentence entry in either language without looking up more than one word.
- Your SR retention rate in Obsidian is ≥80% on mature cards in both decks.

If you don't hit those, extend Phase 1 by two weeks. Don't switch early just because the calendar says so.

At switchover:
- **Spanish and French → maintenance:** 15 min/day each, mostly SR + one podcast on commute. No new grammar.
- **Japanese → primary:** 5 hrs/week. Genki or equivalent textbook, Nihongo con Teppei, kanji SRS (use your existing kanji app, not Obsidian).
- **Chinese → ambient:** 15 min/day of TeaTime Chinese. No active study.

## Phase 3: week ~13 onwards

When Japanese hits a similar milestone, Chinese becomes primary. Spanish, French, and Japanese all go to maintenance. The `hanzi-kanji/` folder starts getting real use then, because by that point you'll have enough kanji to anchor hanzi against.

## Anti-patterns to watch for in yourself

You're a data scientist. The failure modes for people like us:

- **Spending a weekend "improving the pipeline" instead of studying.** If you catch yourself writing a script to parse podcast transcripts, close the laptop.
- **Over-instrumenting.** You don't need a retention dashboard. The SR plugin tells you what you need.
- **Perfectionism on notes.** A sloppy card reviewed beats a beautiful card unmade.
- **Mixing languages in one session "just this once".** That's the whole point of alternating. The rule exists because your future self will find reasons to break it.
- **Treating this like a project with a ship date.** It's a practice. There is no deploy.
