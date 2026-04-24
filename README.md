
<div align="center">
  <a href="https://github.com/iNuoers/nyt-midi-crossword-answers">
    <img src="https://crosswordanswers.today/icon.svg" alt="NYT MIDI Logo" width="120" height="120">
  </a>

  <h1 align="center">NYT MIDI Crossword — Puzzle Archive</h1>

  <p align="center">
    <strong>Open-source grid data and daily answers for every NYT MIDI Crossword.</strong>
  </p>

  <p align="center">
    <a href="https://midianswers.today">🌐 Website</a> ·
    <a href="https://midianswers.today/today">📖 Today's Answer</a> ·
    <a href="https://midianswers.today/archive">🗂️ Archive</a>
  </p>

  <p align="center">
    <img src="https://img.shields.io/badge/puzzles-latest-blue?style=flat-square" alt="Puzzles">
    <img src="https://img.shields.io/badge/updated-daily-brightgreen?style=flat-square" alt="Updated Daily">
    <img src="https://img.shields.io/badge/data-JSON-orange?style=flat-square" alt="JSON">
    <img src="https://img.shields.io/badge/license-MIT-yellow?style=flat-square" alt="License">
  </p>
</div>

---

## What is NYT MIDI Crossword?

The **NYT MIDI Crossword** is a specialized crossword format (often bridging the gap between the Mini and the Daily) provided by The New York Times. It offers a perfect balance of challenge and speed, requiring both vocabulary depth and logical deduction.

This repository serves as a permanent **open-source archive** of the grid structures, clues, and solutions for these puzzles. All data is structured in a clean, developer-friendly JSON format.

## Quick Start

```bash
# Clone the archive
git clone [https://github.com/iNuoers/nyt-midi-crossword-answers.git](https://github.com/iNuoers/nyt-midi-crossword-answers.git)

# Browse the puzzles directory
cd nyt-midi-crossword-answers/puzzles

# Inspect today's puzzle data (requires jq)
cat 2026-04-24.json | jq '.clues.across'
```

## Data Schema

### Puzzle File — `puzzles/YYYY-MM-DD.json`

```json
{
  "id": "nyt-midi-2026-04-24",
  "date": "2026-04-24",
  "title": "Friday MIDI",
  "author": "Puzzle Constructor",
  "grid": {
    "rows": 9,
    "cols": 9,
    "cells": ["A", "B", "C", "..."]
  },
  "clues": {
    "across": [{ "number": 1, "text": "The clue text", "answer": "WORD" }],
    "down": [{ "number": 1, "text": "The clue text", "answer": "WORD" }]
  }
}
```

### Field Reference

| Field | Type | Description |
| :--- | :--- | :--- |
| `date` | `string` | ISO 8601 formatted date (`YYYY-MM-DD`) |
| `author` | `string` | The constructor of the puzzle |
| `grid.rows` | `number` | Number of rows (usually 9x9 for MIDI) |
| `clues.across` | `array` | List of across clues with numbers and answers |
| `clues.down` | `array` | List of down clues with numbers and answers |

## Statistics

| Metric | Value |
| :--- | :--- |
| Total Puzzles | 100+ |
| Format | 9×9 MIDI |
| Data Quality | Verified Daily |
| Update Latency | < 1 hour from release |

## Use Cases

* 📊 **Linguistic Research** — Analyze word frequency and clue patterns in modern crosswords.
* 🤖 **Solver Benchmarking** — Test your LLM or NLP models on structured crossword data.
* 🎨 **Custom Clients** — Build your own minimalist crossword interface using our clean JSON API.
* 📚 **Offline Practice** — Access the archive for personal training without an active internet connection.

## Related Projects

| Project | Description |
| :--- | :--- |
| [Connections Answers](https://connectionsanswers.today) | Daily analysis for NYT Connections |
| [LinkedIn Patches Archive](https://github.com/iNuoers/linkedin-patches-answers-today) | Data for LinkedIn's logic puzzles |
| [Wordle Stats](https://github.com/iNuoers/wordle-stats) | Historical data for Wordle |

## Contributing

We welcome data corrections or structural improvements. If you notice a typo in a clue or a missing puzzle, please:
1. Open an Issue.
2. Submit a Pull Request with the corrected JSON.

## License

MIT © [iNuoers](https://github.com/iNuoers)

*Disclaimer: This project is an independent archive and is not affiliated with, endorsed by, or sponsored by The New York Times Company.*

