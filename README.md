# ⛏️ minespeer — Minesweeper AI Solver

> A browser-based Minesweeper AI assistant that analyzes your board in real-time and tells you the next safest move.

[![HTML](https://img.shields.io/badge/Built%20With-HTML-orange?style=flat-square&logo=html5)](https://github.com/banzoxOG/minespeer/blob/main/index.html)
[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](https://github.com/banzoxOG/minespeer/blob/main/LICENSE)
[![Live Demo](https://img.shields.io/badge/Live%20Demo-Click%20Here-brightgreen?style=flat-square)](https://banzoxog.github.io/minespeer)
[![Repo](https://img.shields.io/badge/GitHub-minespeer-181717?style=flat-square&logo=github)](https://github.com/banzoxOG/minespeer)

---

## 📖 Table of Contents

- [About](#-about)
- [Live Demo](#-live-demo)
- [Features](#-features)
- [Difficulty Levels](#-difficulty-levels)
- [How It Works](#-how-it-works)
- [Controls & Shortcuts](#-controls--shortcuts)
- [Getting Started](#-getting-started)
- [Project Structure](#-project-structure)
- [Tech Stack](#-tech-stack)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🧠 About

**minespeer** is a pure HTML/CSS/JavaScript Minesweeper AI solver. You mirror your Minesweeper board into the app — clicking cells, flagging mines, and entering numbers — and the AI instantly analyzes all visible constraints to recommend your next move: either a safe cell to open or a mine to flag.

No backend. No frameworks. Just open `index.html` and play.

---

## 🌐 Live Demo

👉 **[Try it here](https://banzoxog.github.io/minespeer)**

Or clone and open locally — no build step required.

---

## ✨ Features

- 🎯 **Real-time AI analysis** — recommends safe opens or guaranteed mine flags after every input
- 🧩 **4 difficulty modes** — Beginner, Intermediate, Expert, and fully Custom
- 🖱️ **Multi-cell selection** — use `CTRL + Click` to update multiple cells at once
- ⌨️ **Full keyboard support** — `Space` for empty, `1–8` for numbers, right-click to flag
- 📊 **Live stats** — tracks Opened, Flagged, and Hidden cell counts
- 📱 **Responsive layout** — works on mobile and desktop
- 🚫 **Zero dependencies** — single `index.html` file, no install needed

---

## 🎮 Difficulty Levels

| Level        | Grid Size | Mines | Link |
|--------------|-----------|-------|------|
| Beginner     | 9 × 9     | 10    | [Select in app](https://banzoxog.github.io/minespeer) |
| Intermediate | 16 × 16   | 40    | [Select in app](https://banzoxog.github.io/minespeer) |
| Expert       | 30 × 16   | 99    | [Select in app](https://banzoxog.github.io/minespeer) |
| Custom       | You choose | You choose | [Select in app](https://banzoxog.github.io/minespeer) |

---

## 🤖 How It Works

The AI uses **constraint-based logic** — the same strategy strong human players use:

1. **Flag detection** — if a numbered cell has exactly as many unrevealed neighbors as its number, all of them must be mines → flag them.
2. **Safe open detection** — if a numbered cell already has all its mines accounted for (flagged), the remaining unrevealed neighbors are safe → open them.
3. **Next move display** — the best move is shown at the top of the board after every input.

```
Example:
  Cell [2] has 2 flagged neighbors and 1 unrevealed → that last cell is SAFE ✅
  Cell [3] has 0 flagged neighbors and 3 unrevealed → all 3 are MINES 🚩
```

> If no definite move can be found, the solver tells you to keep revealing to find new patterns.

---

## ⌨️ Controls & Shortcuts

| Action               | Method                        |
|----------------------|-------------------------------|
| Select a cell        | Left Click                    |
| Multi-select cells   | `CTRL` + Left Click           |
| Flag as mine         | Right Click                   |
| Mark as empty        | Select cell → `Space`         |
| Set a number (1–8)   | Select cell → press `1`–`8`   |
| Clear selection      | Click "Clear Selection" button |
| Change difficulty    | Click "← Change Level"        |

---

## 🚀 Getting Started

### Option 1 — Use Live (Recommended)

Open [https://banzoxog.github.io/minespeer](https://banzoxog.github.io/minespeer) in any browser.

### Option 2 — Run Locally

```bash
git clone https://github.com/banzoxOG/minespeer.git
cd minespeer
open index.html   # macOS
# or just double-click index.html on Windows/Linux
```

No npm. No build. No setup. It just works.

---

## 📁 Project Structure

```
minespeer/
└── index.html    # Everything — HTML, CSS, and JS in one file (895 lines)
```

All logic is contained in [`index.html`](https://github.com/banzoxOG/minespeer/blob/main/index.html):

- **HTML** — UI layout and board grid
- **CSS** — Responsive styling, color-coded number cells
- **JavaScript** — Board state management, AI analysis engine, keyboard shortcuts

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| [HTML5](https://developer.mozilla.org/en-US/docs/Web/HTML) | Structure & layout |
| [CSS3](https://developer.mozilla.org/en-US/docs/Web/CSS) | Styling & responsive design |
| [Vanilla JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) | Game logic & AI solver |

No libraries. No frameworks. No bundlers.

---

## 🤝 Contributing

Contributions are welcome! Ideas to improve the solver:

- [ ] Probability-based guessing when no deterministic move exists
- [ ] Board auto-detection via screenshot (image processing)
- [ ] Move history / undo support
- [ ] Dark mode

To contribute:

1. [Fork the repo](https://github.com/banzoxOG/minespeer/fork)
2. Create a feature branch: `git checkout -b feature/my-improvement`
3. Commit your changes: `git commit -m "Add probability solver"`
4. Push and [open a Pull Request](https://github.com/banzoxOG/minespeer/pulls)

Found a bug? [Open an issue](https://github.com/banzoxOG/minespeer/issues).

---

## 📄 License

This project is open source. See the [LICENSE](https://github.com/banzoxOG/minespeer/blob/main/LICENSE) file for details.

---

<p align="center">Made with ❤️ by <a href="https://github.com/banzoxOG">banzoxOG</a></p>
