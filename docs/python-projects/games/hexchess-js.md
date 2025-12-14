# HexChess (JavaScript)

Web-based hexagonal chess with evolutionary AI opponent.

**GitHub:** [gddickinson/hexChess](https://github.com/gddickinson/hexChess)  
**Live Demo:** [gddickinson.github.io/hexChess](https://gddickinson.github.io/hexChess/)

---

## Overview

A browser-based implementation of hexagonal chess featuring standard chess pieces adapted for hexagonal geometry, plus an AI opponent that evolves and improves through gameplay using an evolutionary algorithm.

---

## Features

### Gameplay
- **Hexagonal Board**: Custom hex-grid chess board
- **Adapted Pieces**: All standard pieces with hex-optimized movement
- **Special Piece**: Dragon with extended movement capabilities
- **Standard Rules**: Adapted chess rules for hexagonal geometry
- **Intuitive Interface**: Click-to-move piece selection

### AI Opponent
- **Evolutionary Learning**: AI improves through gameplay
- **Parameter-Based**: Multiple strategy parameters
- **Mutation System**: Random variations in strategy
- **Strategy Evolution**: Successful tactics are preserved
- **Adaptive Play**: AI adjusts to different situations

### Visual Design
- **Clean Board Layout**: Easy-to-read hexagonal grid
- **Piece Graphics**: Clear piece identification
- **Move Highlighting**: Valid move indicators
- **Responsive Design**: Works on desktop and tablets
- **Animation**: Smooth piece movements

---

## Play Online

**[Try it now →](https://gddickinson.github.io/hexChess/)**

---

## Piece Movement Rules

### Standard Pieces (Hex-Adapted)

**Pawns**
- Move forward one hex
- Capture diagonally forward
- No en passant (simplified for hex board)

**Knights**
- Extended L-pattern for hexagonal grid
- Jump over pieces
- 12 possible moves from center position

**Bishops**
- Diagonal movement along hex lines
- Three diagonal axes
- Any distance along diagonal

**Rooks**
- Straight-line movement
- Six hex axes (vs 4 in standard chess)
- Any distance along axis

**Queens**
- Combines rook and bishop movement
- Nine total movement directions
- Most powerful piece

**Kings**
- One hex in any direction
- Can move to any of 6 adjacent hexes
- Castling not implemented

**Dragons** (Special Piece)
- Enhanced movement capabilities
- Can move like queen but with extended range
- Experimental piece

---

## How the AI Works

### Evolutionary Algorithm

The AI uses a parameter-based evolutionary approach:

1. **Parameters**: Each game state is evaluated using multiple factors:
   - Board position value
   - Piece values and threats
   - Attack potential
   - Defense strength
   - King safety
   - Center control
   - Mobility

2. **Game Play**: AI selects moves based on current parameters

3. **Evolution**: When games conclude:
   - Winning strategies have parameters saved
   - "Mutate & Play" introduces random variations
   - Successful mutations are kept
   - Poor strategies are discarded

4. **Improvement**: Over time, the AI develops better playing strategies

### Strategy Factors

The AI considers:
- **Material**: Piece count and value
- **Position**: Board control
- **Tactics**: Immediate threats and opportunities
- **Strategy**: Long-term planning
- **King Safety**: Defensive positioning

---

## Controls

### Player Moves
1. Click piece to select
2. Click destination hex to move
3. Valid moves are highlighted

### AI Controls
- **"Mutate & Play"**: Evolve AI strategy
- **New Game**: Reset board
- **Undo Move**: Take back last move (if available)

---

## Technical Implementation

### Technologies
- **JavaScript**: Core game logic
- **HTML5 Canvas**: Board rendering
- **CSS3**: Styling and layout
- **LocalStorage**: Save AI parameters

### Architecture
```javascript
// Core components
- Board: Hexagonal grid management
- Pieces: Individual piece logic
- AI: Evolutionary decision-making
- Renderer: Visual representation
- GameController: Turn management
```

### Hex Grid System
- **Axial Coordinates**: Efficient hex addressing
- **Neighbor Calculation**: Fast adjacency checks
- **Path Finding**: Valid move generation
- **Collision Detection**: Piece interaction

---

## Development

### Running Locally

```bash
# Clone repository
git clone https://github.com/gddickinson/hexChess.git
cd hexChess

# Open in browser
# No build step required - just open index.html
open index.html
```

### Code Structure

```
hexChess/
├── index.html          # Main page
├── css/
│   └── styles.css     # Styling
├── js/
│   ├── board.js       # Hex grid
│   ├── pieces.js      # Piece logic
│   ├── ai.js          # AI system
│   ├── render.js      # Graphics
│   └── game.js        # Game controller
└── assets/
    └── pieces/        # Piece graphics
```

---

## Customization

### Adjusting AI Difficulty

Edit `ai.js` parameters:
```javascript
const AI_PARAMETERS = {
    aggression: 0.7,      // 0-1, how aggressive
    defense: 0.6,         // 0-1, defensive priority
    mobility_weight: 0.5, // Value of piece movement
    center_control: 0.6,  // Importance of center
    // ... more parameters
};
```

### Board Appearance

Edit `styles.css`:
```css
.hex-tile {
    fill: #f0d9b5; /* Light square color */
}

.hex-tile.dark {
    fill: #b58863; /* Dark square color */
}
```

---

## Comparison with Python Version

| Feature | JavaScript Version | Python Version |
|---------|-------------------|----------------|
| Platform | Web browser | Desktop app |
| Graphics | HTML5 Canvas | PyQt5 |
| AI | Evolutionary algorithm | (Varies by implementation) |
| Multiplayer | Local only | Local only |
| Offline | Yes (after first load) | Yes |

---

## Known Limitations

- No online multiplayer
- AI can be slow on older devices
- No move history/replay
- Limited game analysis features
- Dragon piece balance needs tuning

---

## Future Enhancements

- Online multiplayer support
- Move history and replay
- Save/load games
- Multiple AI difficulty levels
- Tutorial mode for new players
- Sound effects
- More piece types
- Tournament mode
- Opening book for AI

---

## Contributing

Contributions welcome! Areas for improvement:
- AI strategy refinement
- Performance optimization
- Mobile responsiveness
- Additional features
- Bug fixes

---

## License

Open source - see repository for details

---

## Related Projects

- [HexChess Python](hexchess-python.md) - Desktop PyQt5 version

---

*Play hexagonal chess against an evolving AI opponent - no installation required!*
