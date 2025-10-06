# Wordflux

A sleek, Wordle-style puzzle in a dark, modern aesthetic. Play with **click-to-edit tiles**, **arrow-key caret movement**, **sequential flip reveals**, and a **Daily / Random** mode toggle. The whole game ships as a single static `index.html`—no build step.

---

## Features

- **Instant play** — open `index.html` in any modern browser.
- **Editing UX** — click a tile in the active row to place the caret; use **← / →** to move.
- **Smooth reveals** — per-tile, sequential flip animation (clean left-to-right cascade).
- **Modes** — **Daily** (deterministic by date) or **Random** (new word each time), persisted in `localStorage`.
- **Keyboard under board** — keyboard is visible with the grid on one card; responsive sizing for shorter screens.
- **Stats** — played / wins / streak saved locally.

---

## Controls

- **Letters A–Z**: type into the selected slot.
- **Enter**: submit the guess (must be a valid 5-letter word).
- **Backspace**: delete the **previous** slot and move left.
- **Delete**: clear the **current** slot (caret stays).
- **← / →**: move the caret left / right within the current row.
- **Click a tile (current row)**: jump the caret to that slot.

---
## Word Sources & Attribution

Wordflux uses open, community-maintained word lists. See the source repositories for license details and updates:

Tab Atkins’ Wordle List (valid guesses)
https://github.com/tabatkins/wordle-list

DarkerMango — 5-Letter Words (valid guesses)
Repo: https://github.com/DarkerMango/5-Letter-words

Raw list (convenience): https://darkermango.github.io/5-Letter-words/words.txt

Shmookey — Common 5-Letter Words (solutions pool)
Gist: https://gist.github.com/shmookey/b28e342e1b1756c4700f42f17102c2ff

---

## Quick Start

1. Clone or download the repository.
2. Open `index.html` in a browser.

   > Some browsers are stricter about `file://` security. If your browser blocks network fetches, serve the folder locally:

   ```bash
   # Python 3
   python3 -m http.server 8080
   # then open http://localhost:8080/index.html
