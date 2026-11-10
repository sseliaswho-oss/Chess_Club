# Bella's Chess Adventure — Stage 1

**Think Before You Move!** An original, self-contained English-language chess course designed for a young learner who knows the rules but often loses pieces.

## What's included

- 12 lessons across 4 weeks, with **48 original interactive puzzles**.
- Tap-to-identify, legal chess moves with hints, and yes/no exchange decisions.
- Guided lesson unlocks, progress tracking and a graduation screen.
- A playable practice game as White against a beginner-friendly "Coach Fox" opponent.
- Mobile, tablet, and desktop layouts, with no external libraries or account required.
- Progress saved in the same browser using `localStorage`. No analytics or uploads.

## Learning path

1. Spot attacks and identify safe pieces.
2. Find undefended pieces and escape attacks.
3. Protect a piece or capture its attacker.
4. Recognise good captures and fair exchanges.
5. Avoid tempting but bad captures.
6. Build a "three questions before moving" habit.

**Workbook connection:** This original course is organised around concepts in *Learning Chess — Workbook Step 1* by Rob Brunia and Cor van Wijgerden (attacking, defending, capturing unprotected pieces, exchanges). It does not reproduce the workbook diagrams or exercises. It is not affiliated with the publishers or authors.

## Use it on your own device

Open `index.html` in a modern browser. No server or dependency installation is needed. For reliable progress across sessions, a published HTTPS site is recommended, as browser storage behavior on local `file://` pages varies.

## Add it to Bella Learning Hub on GitHub Pages

1. Create a directory named `chess` within the folder **actually deployed by GitHub Pages**. It may be the repository root, `docs/`, or `public/`, depending on your Actions workflow.
2. Upload this `index.html` into the `chess` directory.
3. After the deployment succeeds, open `https://YOUR-USERNAME.github.io/Bella-Learning-Hub/chess/` (adjust the username and repository capitalization to match your setup).
4. Add the following navigation item to your existing Hub homepage, adjusting the relative path if necessary:

   ```html
   <a href="./chess/">Chess Thinking Skills</a>
   ```

**Important:** Moving this course to a different domain, browser or device does not transfer stored progress. Progress is specific to that browser and website origin; the "My Progress" page can copy a textual summary.

## Parent tips

Each lesson can be completed in about 15–20 minutes. Ask Bella to say what her opponent is attacking before every move. Let her try again after mistakes. A short practice three times per week is better than long rushed sessions.

## Privacy and accessibility

No account, ads, trackers, or network calls are built into this site. Lessons are in English. Board squares are keyboard-focusable buttons with accessible square/piece descriptions. The practice opponent is intentionally simple, not a certified chess engine.



# Bella Chess Club — Stockfish Post-game Review

This release extends Bella's existing Real-Game Coach website with a **post-game** Stockfish review. Original Stage 1 lessons and the existing browser progress storage key are unchanged.

## Required files

Upload to the **root of your Chess_Club GitHub repository** (not to Bella-Learning-Hub):

```
Chess_Club/
  index.html
  engine/
    stockfish-19-lite-single.js
    stockfish-19-lite-single.wasm
```

The HTML is included in this ZIP as `index.html`. The two Stockfish engine files **are not included** and must be downloaded from the project publisher. This is essential: the analysis button will not work until both are uploaded. The lessons and existing simple Coach Fox continue to work without them.

- JS: https://github.com/nmrugg/stockfish.js/releases/download/v19.0.1/stockfish-19-lite-single.js
- WASM: https://github.com/nmrugg/stockfish.js/releases/download/v19.0.1/stockfish-19-lite-single.wasm
- Official Stockfish.js README: https://github.com/nmrugg/stockfish.js

**Do not rename the two engine files.** The JavaScript worker expects the `.wasm` file next to it.

## How to use

1. Open https://github.com/sseliaswho-oss/Chess_Club
2. Replace the old root `index.html` with the version from this ZIP.
3. Add a folder `engine` and upload both the official files above into it. For GitHub web upload, you can create `engine/README.md` first or choose `Add file > Upload files` and drop the folder contents into `engine`.
4. Commit changes and wait for GitHub Pages to deploy.
5. Visit https://sseliaswho-oss.github.io/Chess_Club/ and open `Play Chess`.
6. Play a game with Coach Fox or a family member. Scroll to `Stockfish — After-game review` and select `Analyse this game`.
7. Review up to three candidate learning moments, see the board before/after, and only then reveal the explanation.

A saved-games dropdown stores the latest 20 games locally in the device/browser. `Export PGN` provides an independent backup. Previously solved lessons use the same localStorage key (`bella-chess-stage1-progress-v1`) and are preserved if you use the same browser/origin; switching devices does not sync progress.

## Notes and limitations

- Engine runs locally as a Web Worker in the player's browser, without an API key or external account.
- Reviews are **not** available via `file://` if the browser blocks workers or WASM. Use GitHub Pages.
- The analysis is approximate: a short 280ms evaluation per position, analyzing at most the first 100 half-moves, with up to three examples prioritised.
- First-time analysis may take longer on phones. Stay on the page while it analyses. Choose `Stop analysis` to cancel.
- Coach Fox is still the original lightweight opponent; Stockfish analyses completed games but does not play during the game.
- A few tactics and chess-specific game situations can be misinterpreted by short evaluations; parents should discuss the idea rather than treating the engine as an infallible grader.
- Stockfish.js GPLv3: https://github.com/nmrugg/stockfish.js/blob/master/Copying.txt . Follow its attribution and distribution terms when publishing engine files.
