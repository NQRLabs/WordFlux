<img width="1310" height="939" alt="Screenshot 2025-10-11 223940" src="https://github.com/user-attachments/assets/8ca75e0e-8cdf-4f01-937f-cff95e08735a" />

# Wordflux

A sleek, Wordle-style puzzle in a dark, modern aesthetic. Play with **click-to-edit tiles**, **arrow-key caret movement**, **sequential flip reveals**, and a **Daily / Random** mode toggle. The whole game ships as a single static `index.html`—no build step.

---

## Features

- **Instant play** — open `index.html` in any modern browser.
- **Editing UX** — click a tile in the active row to place the caret; use **← / →** to move.
- **Smooth reveals** — per-tile, sequential flip animation (clean left-to-right cascade).
- **Modes** — **Daily** (deterministic by date) or **Random** (new word each time), persisted in `localStorage`.
- **Responsive QWERTY keyboard under the board** — physical layout with ENTER/DEL; board and keyboard scale together for mobile.
- **Stats** — played / wins / streak saved locally in `localStorage`.
- **Online word lists** — large “allowed” and curated “solutions” sets are fetched at runtime; a small fallback list is used automatically if the fetch fails.

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

Wordflux uses open, community-maintained word lists. See their repos for license details and updates:

- **Tab Atkins — Wordle List (valid guesses)**  
  https://github.com/tabatkins/wordle-list

- **DarkerMango — 5-Letter Words (valid guesses)**  
  Repo: https://github.com/DarkerMango/5-Letter-words  
  Raw list: https://darkermango.github.io/5-Letter-words/words.txt

- **Charles Reid — five-letter words (solutions pool)**  
  https://github.com/charlesreid1/five-letter-words (file: `sgb-words.txt`)

- **DWYL — english words (backup source; filtered to 5 letters)**  
  https://github.com/dwyl/english-words (file: `words_alpha.txt`)

> The app de-duplicates and uppercases words, filters to exactly 5 letters, and ensures the **solutions** set is a subset of **allowed** guesses. If online lists can’t be fetched, a small built-in fallback set is used.

---

## Quick Start

1. Clone or download the repository.
2. **Recommended:** serve locally to allow cross-origin fetches for word lists.
   ```bash
   # Python 3
   python3 -m http.server 8080
   # then open:
   http://localhost:8080/index.html

