# EcoBlocks — Design Document

## Theme

**Living world / Earth & Cosmos.** The block colors are mapped to natural categories — green = plants, blue = ocean, brown = land animals, purple = space, yellow = sun/birds, cyan = water, red = body. The background is a soft gradient (sunrise sky) and clearing a row briefly reveals a glowing icon (🐙 🌳 🪐 …) of the fact's subject.

## Core gameplay loop

1. A piece falls from the top.
2. The player rotates and slides it.
3. When a row fills, it clears, the score updates, and a **fact card** appears on the right panel with a 4-second readable highlight.
4. As the player survives longer, fall-speed increases.

## Why a Tetris-like for science facts?

Tetris already requires undivided focus. The fact panel uses the player's *natural between-piece pauses*, when they're scanning the board. Facts are short (≤ 1 sentence), so they don't disrupt flow.

## Educational design

- The fact pool covers four kid-friendly domains: **animals, plants, space, human body**.
- Facts are written in everyday language (no jargon).
- Each fact is paired with an emoji icon that reinforces the subject visually.
- Facts repeat only after the entire pool has been used in a session, so kids see fresh content each time.
- A "Facts learned this game" counter rewards curiosity, not just speed.

## Scoring system

| Action | Points | Facts shown |
|---|---|---|
| 1 line | +100 | +1 |
| 2 lines | +300 | +1 |
| 3 lines | +500 | +2 |
| 4 lines (Tetris) | +800 | +3 |
| Soft drop | +1 / cell | — |
| Hard drop | +2 / cell | — |

Score and number of facts learned both persist as separate high scores in `localStorage`.

## Difficulty matrix

| Setting | Initial fall (ms/cell) | Speed-up rate | Hint preview |
|---|---|---|---|
| Easy | 800 | every 15 lines | Yes |
| Medium | 600 | every 10 lines | Yes |
| Hard | 400 | every 6 lines | No |

## Controls philosophy

Standard Tetris keyboard layout. We deliberately do not bind WASD because most kids already know arrows from other games. Nothing requires the mouse.

## Accessibility notes

- Pieces have distinct colors AND distinct silhouettes.
- Fact cards use a large readable font and stay long enough to read at age 7.
- Soft drop never instantly slams a piece — kids can recover.
- A "Pause" key (P) freezes the world if a fact is interesting and the player wants to read it longer.

## Fact pool (sampled)

The game ships with ~40 facts. Examples:

- 🐙 Octopuses have **three hearts** and blue blood.
- 🌳 The biggest tree on Earth is a **Giant Sequoia** named General Sherman.
- 🪐 Saturn's rings are made of **billions of icy chunks**.
- 🧠 Your brain uses about **20%** of your body's energy.
- 🐢 Some sea turtles can hold their breath for **5 hours**.
- 🌋 Earth has more than **1,500 active volcanoes**.

(Full list lives inside `index.html` in the `FACTS` array — easy to extend.)

## Future ideas

- Themed packs (one game-mode per topic — only animal facts, only space facts).
- Quiz mode: every 5 lines you answer a question instead of seeing a fact.
- "Unlocked species" gallery showing every animal you've seen across all sessions.
