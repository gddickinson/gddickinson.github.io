# HexChess Python

PyQt-based hexagonal chess game with custom piece movement rules.

**GitHub:** [gddickinson/hexchess_python](https://github.com/gddickinson/hexchess_python)

---

## Overview

A fully-featured implementation of hexagonal chess using PyQt5, offering a unique twist on traditional chess by adapting all piece movements to a hexagonal grid system.

---

## Features

### Core Gameplay
- **Hexagonal Grid**: Custom hexagonal board layout
- **Adapted Piece Movement**: All standard chess pieces with hex-adapted rules
- **Interactive GUI**: Point-and-click interface built with PyQt5
- **Move Validation**: Complete rule enforcement for hexagonal movement
- **Game State Management**: Turn tracking, game history, move validation

### User Interface
- **Visual Board**: Clean, intuitive hexagonal board display
- **Piece Graphics**: Custom-designed pieces for hex board
- **Move Highlighting**: Visual indicators for valid moves
- **Drag-and-Drop**: Intuitive piece movement interface

---

## Piece Movement (Hexagonal Adaptation)

### Pawns
- Move forward one hex
- Capture diagonally forward
- Special first-move rules adapted for hex grid

### Knights
- Extended L-shaped jump pattern
- Adapted for hexagonal geometry

### Bishops
- Diagonal movement along hex lines
- Three diagonal directions per hex

### Rooks
- Straight-line movement
- Six directions (hex axes)

### Queen
- Combines rook and bishop movement
- Nine total movement directions

### King
- One hex in any direction
- Standard chess king rules

---

## Installation

```bash
# Clone repository
git clone https://github.com/gddickinson/hexchess_python.git
cd hexchess_python

# Install dependencies
pip install PyQt5

# Run the game
python hexchess.py
```

---

## Technical Implementation

### Technologies
- **PyQt5**: GUI framework
- **Python 3.x**: Core language
- **Custom Graphics**: Hex board rendering
- **Game Logic**: Object-oriented piece and board classes

### Architecture
- **Board Class**: Manages hex grid state
- **Piece Classes**: Individual piece movement logic
- **Game Controller**: Turn management and rule enforcement
- **UI Layer**: PyQt5 interface

---

## Related Projects

- [JavaScript HexChess](hexchess-js.md) - Web-based version with AI opponent

---

*Hexagonal chess variant built with PyQt5*
