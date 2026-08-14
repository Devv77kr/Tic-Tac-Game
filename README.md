# Tic‑Tac‑Toe

> A clean, easy-to-read guide for the classic 3×3 Tic‑Tac‑Toe game — rules, strategy highlights, and developer notes.

<p align="center">
  <img alt="hc" src="https://github.com/user-attachments/assets/81e8cc1f-f5ba-47d5-8e51-7c981c2029a2" width="600" />
  <img alt="tic" src="https://github.com/user-attachments/assets/ad8e475c-1c73-4d6d-a089-9ef01614d7ef" width="600" />
  <img alt="won" src="https://github.com/user-attachments/assets/546e918b-7027-46f6-adb9-89e39c736bca" width="600" />
</p>

---

## Quick Summary

**Tic‑Tac‑Toe** is a two‑player, turn‑based game on a 3×3 grid. Players alternate placing their mark (X or O). The first player to place three of their marks in a straight line (horizontal, vertical, or diagonal) wins. If all nine cells are filled without a line, the game is a **draw**.

---

## Rules & Setup

- **Board:** 3 rows × 3 columns.
- **Players:** 2 (X and O). **X goes first** by convention.
- **Move:** On your turn, place your mark in any empty cell.
- **Win condition:** Three of the same mark in a row, column, or diagonal.
- **Draw condition:** All cells filled and no winner.
- **Illegal move:** Placing a mark in an occupied cell.

---

## Notation (example layout)

```
 1 | 2 | 3
---+---+---
 4 | 5 | 6
---+---+---
 7 | 8 | 9
```

Use either 1–9 or (row, column) coordinates to reference cells.

---

## Strategy — Key Highlights

- Best opening: take the **center (5)** when possible.
- Prefer **corners** over edges when the center is taken.
- Always **block** your opponent's immediate winning move.
- Aim to **create forks** (two simultaneous threats) or prevent your opponent's forks.
- With perfect play from both players, the result is a **draw**.

---

## Developer Notes (implementation)

- Represent the board as a 1D array of length 9 or a 3×3 2D array.
- Core functions:
  - `makeMove(board, index, player)` — place a mark if the square is empty.
  - `checkWinner(board)` — return the winner (X or O) or null.
  - `isBoardFull(board)` — detect a draw.
  - `getLegalMoves(board)` — list available indices.
- Win check: test the 8 winning lines (3 rows, 3 columns, 2 diagonals).
- For a perfect-playing AI: use **minimax** with alpha‑beta pruning.

---

## Screenshots

The demo images are shown above. If you'd like the images committed into the repo (e.g., `/assets/hc.png`), I can upload them and update the README to use local paths.

---

Next steps I can take for you:
- Add a Play/Build/Run section for a specific implementation (JavaScript, Python, etc.).
- Upload your provided images into `/assets` and update the README to reference them locally.
- Add a small embedded demo GIF or link to a live demo.

*Commit: improved readability, highlighted key rules and strategy.*
