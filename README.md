# Parole Volanti 🇮🇹

A **Space Invaders-style** word shooter. Italian words drift down from the sky — some spelled correctly, some misspelled. Pilot your shuttle, and **shoot only the words spelled correctly**.

## Avvio rapido / Quick start

1. Doppio click su `index.html`.
2. Scegli difficoltà e tema.
3. Premi ▶ INIZIA e fai fuoco solo sulle parole giuste!

## Comandi / Controls

| Tasto | Azione |
|---|---|
| `←` / `→` | Muovi la navetta / Move the shuttle |
| `Space` | Spara / Shoot |
| `Enter` | Chiudi la scheda parola / Close word card |
| `P` | Pausa / Pause |
| `R` | Ricomincia / Restart |

## Come si gioca / How it works

- La tua navetta sta in fondo allo schermo.
- Le parole scendono dall'alto, una alla volta. Alcune sono **scritte correttamente** (esempio: `GATTO`), altre sono **sbagliate** (esempio: `GATO`).
- **Spara solo a quelle giuste.** Quando colpisci una parola giusta, vedi una scheda con il significato e una frase di esempio.
- Se spari a una parola sbagliata, perdi un cuore.
- Quando colpisci abbastanza parole giuste, completi il livello e passi a quello dopo (più veloce).
- Sulla schermata iniziale vedi i tuoi **progressi**: parole giuste totali, livello massimo, record, e quante parole diverse hai padroneggiato.

## Obiettivo educativo / Learning goals

- **Riconoscimento ortografico**: imparare a vedere errori comuni (doppie consonanti, accenti, GN/GL/SC, parole con CH/QU).
- **Vocabolario di base**: animali, cibo, famiglia, scuola, natura, città.
- **Lettura veloce**: avere il tempo di leggere ogni parola prima che arrivi in fondo.

## Difficoltà / Difficulty

| Livello | Velocità parole | Bersaglio | Cuori | Parole corrette |
|---|---|---|---|---|
| Facile | Lenta | 6 a livello | 5 | 70% |
| Medio | Normale | 8 a livello | 4 | 55% |
| Difficile | Veloce | 10+ a livello | 3 | 50% |

A ogni livello successivo le parole arrivano un po' più veloci e il bersaglio cresce di 2.

## Temi / Themes

- 🌌 **Spazio** — sfondo notturno, stelle, navetta argentata
- 🌊 **Mare** — fondale azzurro, bollicine, sottomarino
- ☁️ **Cielo** — sereno con nuvole, navetta arancione

## Punteggio / Scoring

- Parola giusta colpita: **+50 punti**
- Parola sbagliata colpita: **−15 punti** (e -1 cuore)
- Parola giusta che ti scappa in fondo: **−5 punti**
- Parola sbagliata che ti scappa: nessun effetto (è giusto lasciarla passare!)

I progressi (parole giuste totali, livello massimo, record, parole padroneggiate) sono salvati nel browser.

## Vedi anche / See also

- [`DESIGN.md`](./DESIGN.md) — design rationale + lista parole
- [`../DEPLOYMENT.md`](../DEPLOYMENT.md) — pubblicazione online
