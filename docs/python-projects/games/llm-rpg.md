# LLM-Powered RPG

D&D-style RPG with AI-controlled NPCs using local Large Language Models.

**GitHub:** [gddickinson/llm_RPG](https://github.com/gddickinson/llm_RPG)

---

## Overview

A sophisticated role-playing game that uses local LLMs (via Ollama) to power autonomous NPCs with dynamic decision-making, realistic dialog, and emergent gameplay. Characters make independent choices based on their personalities, stats, and memories.

---

## Key Features

### LLM-Powered NPCs
- **Autonomous Decision Making**: Each NPC controlled by dedicated LLM instance
- **Parallel Processing**: Multi-threaded NPC AI for non-blocking gameplay
- **Dynamic Dialog**: Context-aware conversations based on character personality
- **Memory System**: NPCs remember past events and interactions
- **Emergent Behavior**: Unpredictable but logical character actions

### Gameplay Systems

#### Combat
- **Turn-Based System**: Stats-based combat resolution
- **Weapon Types**: Different damage calculations by weapon
- **Health Tracking**: HP management and defeat mechanics
- **Defeat System**: Characters drop items when defeated
- **Revival Mechanics**: Shrine-based resurrection system

#### World Interaction
- **Movement**: NPCs navigate the game world autonomously
- **Trading System**: Buy/sell items between characters
- **Item Management**: Inventory and equipment systems
- **World Exploration**: Dynamic environment interaction
- **Relationship Tracking**: Combat and interactions affect NPC relationships

### Character System
- **Character Classes**: Multiple D&D-style classes
- **Stat Sheets**: Strength, dexterity, intelligence, etc.
- **Equipment**: Weapons, armor, and items
- **Personality Profiles**: Unique character traits and goals
- **Experience & Leveling**: Character progression (planned)

---

## Installation

### Requirements
- Python 3.8+
- Ollama with Llama 3 model
- 32GB RAM recommended for optimal performance
- M1/M2 Mac, Windows, or Linux

### Setup

```bash
# Clone repository
git clone https://github.com/gddickinson/llm_RPG.git
cd llm_RPG

# Install dependencies
pip install -r requirements.txt

# Install and setup Ollama
# Download from ollama.ai
ollama pull llama3

# Run with GUI (recommended)
python main.py --ui gui

# Or use terminal interface
python main.py --ui terminal
```

---

## Configuration

### Command Line Options

```bash
python main.py [OPTIONS]

Options:
  --model MODEL         LLM model to use (default: llama3)
  --ui [gui|terminal]   Interface type (default: gui)
  --width WIDTH         Window width for GUI (default: 1200)
  --height HEIGHT       Window height for GUI (default: 800)
  --debug               Enable debug logging
```

### Performance Tuning

Edit `config.py`:
- `NUM_LLM_THREADS`: Number of parallel NPC threads
- `MODEL_NAME`: LLM model selection
- `WORLD_SIZE`: Game world dimensions

---

## How It Works

### LLM Integration
1. Each NPC runs in separate process with dedicated LLM
2. Game state sent to LLM as structured context
3. LLM generates JSON-formatted actions
4. Actions validated and executed in game world
5. Results fed back to NPC memory

### Action Types
- **Movement**: Navigate to locations
- **Combat**: Attack other characters
- **Dialog**: Speak with other NPCs
- **Trading**: Economic interactions
- **World Actions**: Use items, search areas

---

## Technical Stack

### Core Technologies
- **Python 3.8+**: Main language
- **Ollama**: Local LLM integration
- **Llama 3**: Default language model
- **Pygame**: Graphics and rendering
- **pygame_gui**: UI components
- **multiprocessing**: Parallel NPC processing

### Architecture
- **NPC Manager**: Handles NPC lifecycle and LLM coordination
- **World Manager**: Game state and physics
- **Combat System**: Battle resolution
- **Memory System**: Event tracking and recall
- **Revival System**: Character resurrection mechanics

---

## Development

### Creating Custom NPCs

```python
def create_custom_npc(self, position=(x, y)):
    npc = Character(
        id="custom_npc_01",
        name="CustomName",
        character_class=CharacterClass.WARRIOR,
        personality="brave and honorable",
        ...
    )
```

### Debugging
- Use `--debug` flag for detailed logs
- Monitor `logs/` directory for NPC decisions
- Check LLM response validation in console

---

## Troubleshooting

| Issue | Solution |
|-------|----------|
| NPCs Not Moving | Verify LLM generating valid actions; check debug logs |
| High Memory Usage | Reduce NUM_LLM_THREADS; use smaller LLM model |
| Slow Performance | Decrease number of active NPCs; optimize LLM parameters |
| Connection Errors | Ensure Ollama is running; check model availability |

---

## Future Enhancements

- Additional character classes and races
- Expanded world map and locations
- Quest and storyline systems
- Multiplayer support
- Advanced AI behaviors
- Character progression and leveling

---

## License

MIT License

---

*D&D-style RPG powered by local LLMs for dynamic, emergent gameplay*
