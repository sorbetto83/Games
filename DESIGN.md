# Math Quest — Design Document

## Theme

**Space exploration.** A young astronaut hops between asteroid platforms, dodges craters, and powers through energy gates by solving math problems. Background features parallax stars and distant planets. Color palette: deep navy + cyan + electric purple, with warm yellow highlights for collectibles.

## Core gameplay loop

1. Run to the right.
2. Jump over gaps and onto platforms.
3. Collect coins and stars for score.
4. Reach a math gate → pause → solve the problem.
5. Repeat until the rocket at the level's end.

## Why a platformer for math?

A pure quiz app is dry. By embedding math inside a small movement challenge, the player **earns the right to think** — they got there by playing, so the math feels like a reward, not a test. The gate mechanic also gives kids unlimited "thinking time" without making the moving parts harder.

## Educational design

- Problems are randomly generated per gate based on the difficulty setting.
- Easy difficulty avoids any operation a 7-year-old hasn't seen.
- Medium adds multiplication tables up to 10×10.
- Hard adds clean-divisor division (no remainders) for ages 10–12.
- After 3 wrong answers, the level restarts — no game-over screen, no shame.

## Scoring system

| Event | Points |
|---|---|
| Correct gate answer | +100 |
| Star pickup | +25 |
| Coin pickup | +10 |
| Level complete | +500 |
| Wrong answer | −25 + lose heart |

High score persists across sessions via `localStorage`.

## Difficulty matrix

| Setting | Operators | Range | Lives | Player speed |
|---|---|---|---|---|
| Easy | + − | 0–10 | 5 | Slow |
| Medium | + − × | 0–20 | 3 | Normal |
| Hard | + − × ÷ | 0–50 | 3 | Normal |

## Controls philosophy

Every game in this collection is **keyboard-only**. We use the standard arrow-keys + Space layout that kids already know from other games, plus the number row for typing answers. Nothing requires the mouse.

## Accessibility notes

- Color is never the only signal: gates have geometric shapes too.
- The font is large and high-contrast.
- The math problem display pauses the game; there is no time-out failure on Easy mode.
- Volume is off by default (no audio in v1, can be added later).

## Future ideas

- Multiple levels with increasing layout complexity.
- Boss fights: solve 5 problems in a row.
- "Word problem" gates ("If you have 3 apples and find 4 more...").
- Replace number-key input with a virtual keypad to support touchscreens.
