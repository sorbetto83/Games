# Parole Volanti — Design Document

## Tema / Theme

**Borgo italiano al tramonto.** A small Italian village square at sunset — terracotta roofs, a fountain, climbing ivy. The hero is a small bookworm-character (a friendly green creature with glasses and a little book). Floating letters are paper sheets that drift gently up-and-down. The visual mood is warm — orange, terracotta, sage green, cream.

## Core gameplay loop

1. The game shows the target word at the top: e.g., **GATTO**.
2. Letters spawn on platforms across the screen — both letters of the word *and* a few wrong-letter distractors.
3. The player jumps and runs to **collect letters in the correct order**.
4. After completing the word, a card appears with the meaning + sample sentence.
5. A new word is chosen, the level reshuffles, and play continues.

## Why a platformer for spelling?

Spelling drills get boring fast. By making the kid *physically navigate* the word — jumping toward a letter forces them to commit visually to the next character — we turn passive recognition into active selection. The mistake-cost is real (lose a heart) but forgiving (you don't have to start the word over; you just keep going from your current position).

## Educational design

### Word selection

- Words are chosen from a curated kid-vocabulary list, organized by difficulty.
- Easy words are 3–4 letters with simple sounds (SOLE, MARE, PANE, GATTO).
- Medium words introduce trigrams kids learn around age 8–10 (NUVOLA, FORMICA, FAMIGLIA).
- Hard words include orthography traps Italian schoolkids actually study: double consonants (GIRAFFA, FARFALLA), `gn`/`gl`/`sci` (LASAGNA, FOGLIA, PESCE), and accents (PERCHÉ, CITTÀ, CAFFÈ).
- Each word ships with: its **English translation** and an **Italian example sentence** translated to English.

### Sentence design

Sentences are deliberately:
- short (≤ 8 Italian words)
- present-tense or near-present
- using common verbs (è, ha, mangia, vede, gioca…)
- naming the target word in context

Example for `GATTO`:
> *Il gatto dorme sul divano.* — The cat sleeps on the sofa.

## Scoring system

| Event | Points |
|---|---|
| Correct letter pickup | +10 |
| Word completed | +200 |
| Wrong letter pickup | −15 + lose heart |
| Star pickup | +50 |

High score persists in `localStorage`.

## Difficulty matrix

| Setting | Word pool | Hearts | Distractors |
|---|---|---|---|
| Facile (Easy) | 3–4 letters | 5 | Few |
| Medio (Medium) | 5–6 letters | 4 | Normal |
| Difficile (Hard) | 6+ letters, doppies, accents | 3 | Many |

## Controls philosophy

Same arrow-keys + space + enter convention as the rest of the collection. Italian keyboard or English keyboard both work — we don't bind any letter keys for movement.

## Accessibility & kid-friendliness

- The current target letter pulses gently (subtle scale), so kids can easily spot what they need next.
- Already-collected letters are shown in a row at the top, lit up.
- After a word is completed, the game **pauses** for the explanation card — no time pressure.
- Wrong letters cost a heart but **don't reset** word progress — the kid never feels punished into giving up.
- Both Italian and English are shown side-by-side, so non-Italian-speaking parents can play with their kids and so the game doubles as an English-Italian vocabulary tool.

## Word list (sampled)

| Word | Meaning | Example |
|---|---|---|
| SOLE | sun | Il sole è caldo. |
| LUNA | moon | La luna brilla. |
| GATTO | cat | Il gatto dorme. |
| CANE | dog | Il cane corre. |
| PANE | bread | Mangio il pane. |
| ALBERO | tree | L'albero è alto. |
| NUVOLA | cloud | La nuvola è bianca. |
| FORMICA | ant | La formica è piccola. |
| GIRAFFA | giraffe | La giraffa ha il collo lungo. |
| FARFALLA | butterfly | La farfalla vola. |
| OMBRELLO | umbrella | Apro l'ombrello. |
| PERCHÉ | why / because | Perché ridi? |

(Full list lives inside `index.html` in the `WORDS_*` arrays — easy to extend.)

## Future ideas

- Antonym / synonym mode (collect letters of the opposite word).
- Verb-conjugation mode (collect letters that form the right verb form).
- Themed packs (animals only, food only, school only).
- Two-player mode: split-screen race.
