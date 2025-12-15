# self-aware_game

A Python simulation featuring self-aware game characters who realize they're in a game. The project includes a meta "game within a game" structure, where a self-aware snake game exists inside a larger world with a roaming self-aware character.

**[View on GitHub →](https://github.com/gddickinson/self-aware_game)**

---

## Overview

**Languages:** Python

## Documentation

# Self-Aware Game

A Python simulation featuring self-aware game characters who realize they're in a game. The project includes a meta "game within a game" structure, where a self-aware snake game exists inside a larger world with a roaming self-aware character.

## Features

- **Self-aware Snake Game**: A snake game where the snake gradually becomes aware it exists in a simulation
- **Roaming Character**: A character that wanders around the world, thinks about its existence, and interacts with the snake game
- **Dialogue System**: Characters express their thoughts about being in a game
- **Expandable World**: Framework for adding more buildings, games, and characters
- **Debugging Tools**: Comprehensive error tracking and performance monitoring

## Project Structure

```
self-aware-game/
│
├── main.py                   # Main entry point for the game
├── modules/
│   ├── __init__.py           # Package initialization
│   ├── snake_game.py         # The self-aware snake game
│   ├── character.py          # Self-aware character implementation
│   ├── world.py              # Game world and buildings
│   ├── dialogue.py           # Dialogue and thought system
│   └── debug.py              # Debugging tools
│
├── assets/
│   ├── character_sprites.png # Character sprite sheet
│   └── sounds/               # Game sounds
│
├── debug.log                 # Log file (created when running)
├── requirements.txt          # Required Python packages
└── README.md                 # This file
```

## Requirements

- Python 3.8 or higher
- Pygame 2.0.0 or higher

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/self-aware-game.git
   cd self-aware-game
   ```

2. Create and activate a virtual environment (recommended):
   ```
   python -m venv venv
   
   # On Windows:
   venv\Scripts\activate
   
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

##

*[View full README on GitHub]*

