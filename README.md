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
