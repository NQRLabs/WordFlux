<img alt="wordflux-logo" src="./assets/images/logo.png" style="margin-left:auto; margin-right:auto; display:block; width:250px;"/>

# WordFlux

**WordFlux** is a compact, browser-based word puzzle inspired by *Wordle*, reimagined in a sleek dark aesthetic with responsive design, smooth animations, and intuitive controls. It’s a single-page game that runs entirely in your browser — no installation, no accounts, and no build tools required.

[**View Live Demo**](https://nqrlabs.com/WordFlux/)

## Overview

WordFlux blends clarity, responsiveness, and minimalism into a pure client-side experience.
Players can click tiles or use keyboard navigation to type guesses, with sequential flip animations revealing the results.
The game offers **Daily** and **Random** modes, tracks wins and streaks locally, and fetches its vocabulary from open, community-maintained word lists.

Everything operates fully client-side using standard browser APIs.

## Features

- **Instant play:** Open `index.html` directly in any modern browser.  
- **Daily and Random modes:** Deterministic daily puzzles or on-demand random words, persisted via `localStorage`.  
- **Interactive editing:** Click-to-edit tiles with full keyboard navigation (← / → / DEL / ENTER).  
- **Smooth reveals:** Sequential flip animations that visually echo the rhythm of manual solving.  
- **Responsive design:** Scales the board and keyboard together for comfortable mobile play.  
- **Statistics tracking:** Keeps played, wins, and streak stats in the browser.  
- **Online word lists:** Pulls multiple community-maintained word sets at runtime, with automatic fallbacks when offline.  
- **Offline-capable:** Once loaded, gameplay continues even without a connection.

## Controls

| Action | Input |
|--------|--------|
| Type letter | A–Z keys |
| Submit guess | **Enter** |
| Delete previous | **Backspace** |
| Clear current tile | **Delete** |
| Move caret | **← / →** |
| Jump to tile | Click on tile (current row only) |

## Word Sources & Attribution

WordFlux uses open, community-maintained English word lists.  
These data sources are credited here for transparency and acknowledgment:

- **Tab Atkins — Wordle List (valid guesses)**  
  https://github.com/tabatkins/wordle-list

- **DarkerMango — 5-Letter Words (valid guesses)**  
  https://github.com/DarkerMango/5-Letter-words  
  Raw list: https://darkermango.github.io/5-Letter-words/words.txt

- **Charles Reid — five-letter words (solution pool)**  
  https://github.com/charlesreid1/five-letter-words (file: `sgb-words.txt`)

- **DWYL — English words (backup source)**  
  https://github.com/dwyl/english-words (file: `words_alpha.txt`)

> The app automatically filters, uppercases, and de-duplicates words, ensuring all valid solutions are included within the allowed guess set.  
> If network access fails, a small built-in fallback list is used instead.

## Quick Start

1. Clone or download the repository.  
2. Serve the folder locally to enable cross-origin fetches for the word lists:
   ```bash
   python3 -m http.server 8080
   # then open:
   http://localhost:8080/index.html

## License

MIT License — free for modification and use. Attribution appreciated if used publicly.

### Third-Party Components

- Online word lists by Tab Atkins, DarkerMango, Charles Reid, and DWYL - publicly available and credited above.

## Credit

Created by **NQR** for puzzle solvers, designers, and curious thinkers who enjoy language as a system to decode.
If you use *WordFlux* in a puzzle hunt or ARG, I’d love to hear about it.
