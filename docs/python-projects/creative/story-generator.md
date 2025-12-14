# Story Generator

Procedural narrative generation system with branching storylines and dynamic characters.

**GitHub:** [gddickinson/story-generator](https://github.com/gddickinson/story-generator)

---

## Overview

A Python-based procedural narrative generation system that creates branching interactive stories with rich world-building, complex character relationships, and emergent plot developments. The system combines narrative templates, character AI, and world simulation to produce unique storytelling experiences.

---

## Features

### Narrative Generation
- **Branching Storylines**: Multiple narrative paths based on choices
- **Dynamic Plot**: Adaptive story development
- **Character-Driven Events**: Actions driven by character personalities
- **World State Tracking**: Persistent world changes
- **Emergent Narratives**: Unexpected story developments from character interactions

### Character System
- **Complex Personalities**: Multi-dimensional character traits
- **Relationship Networks**: Dynamic social connections
- **Character Goals**: Individual motivations and objectives
- **Memory System**: Characters remember events and interactions
- **Character Development**: Personalities evolve through story

### World Building
- **Location Management**: Multiple interconnected settings
- **Object Tracking**: Items and their relationships
- **Historical Events**: World timeline and backstory
- **Faction Systems**: Group dynamics and conflicts
- **Environmental Factors**: Weather, time, seasonal changes

### Story Structure
- **Act-Based Narrative**: Three-act structure with climax
- **Plot Threads**: Multiple interwoven storylines
- **Conflict Generation**: Automatic tension creation
- **Resolution System**: Satisfying story conclusions
- **Pacing Control**: Rhythm and tempo management

---

## Installation

```bash
# Clone repository
git clone https://github.com/gddickinson/story-generator.git
cd story-generator

# Install dependencies
pip install -r requirements.txt

# Run the generator
python story_generator.py
```

---

## Usage

### Basic Story Generation

```python
from story_generator import StoryGenerator

# Create generator
generator = StoryGenerator()

# Generate a story
story = generator.generate_story(
    genre='fantasy',
    length='medium',
    num_characters=5
)

# Print the story
print(story.narrative)
```

### Interactive Mode

```python
# Create interactive story
story = generator.create_interactive(genre='sci-fi')

# Make choices during story
for scene in story:
    print(scene.text)
    choice = story.get_choices()
    story.make_choice(choice[0])
```

### Advanced Generation

```python
# Configure story parameters
generator = StoryGenerator(
    narrative_style='character-driven',
    complexity='high',
    themes=['redemption', 'sacrifice'],
    tone='dramatic'
)

# Add custom characters
generator.add_character(
    name="Aria",
    archetype="hero",
    traits=['brave', 'impulsive', 'loyal'],
    background="orphaned warrior"
)

# Generate with world state
story = generator.generate_story(
    world_seed=12345,
    starting_conflict="ancient_prophecy",
    ending_preference="bittersweet"
)
```

---

## Story Elements

### Genres Supported
- Fantasy
- Science Fiction
- Mystery
- Romance
- Horror
- Historical
- Adventure
- Thriller

### Character Archetypes
- Hero/Protagonist
- Mentor
- Shadow/Antagonist
- Trickster
- Herald
- Shapeshifter
- Guardian
- Ally

### Plot Structures
- Hero's Journey
- Three-Act Structure
- Save the Cat
- Kishōtenketsu (four-act)
- Custom templates

---

## Technical Implementation

### Core Components

```python
# Story generator architecture
- NarrativeEngine: Plot generation
- CharacterManager: Character creation/behavior
- WorldSimulator: Environment simulation
- ConflictGenerator: Tension creation
- DialogSystem: Character conversations
- EventChain: Causal event linking
```

### Algorithms
- **Narrative Templates**: Structured plot frameworks
- **Character AI**: Goal-driven behavior simulation
- **Causal Chains**: Event consequence tracking
- **Conflict Resolution**: Story tension management
- **Pacing Algorithms**: Rhythm optimization

---

## Configuration

### Story Parameters

| Parameter | Options | Description |
|-----------|---------|-------------|
| `genre` | fantasy, sci-fi, mystery, etc. | Story genre |
| `length` | short, medium, long | Approximate word count |
| `complexity` | low, medium, high | Plot intricacy |
| `num_characters` | 1-20 | Number of characters |
| `narrative_style` | plot-driven, character-driven | Focus type |
| `tone` | comedic, dramatic, dark, light | Overall mood |
| `pacing` | slow, moderate, fast | Story rhythm |

---

## Output Formats

```bash
# Export options
- Text (.txt)
- Markdown (.md)
- JSON (structured data)
- HTML (formatted story)
- PDF (via conversion)
- Interactive (web-based)
```

---

## Example Output

```markdown
**The Last Starship**

Chapter 1: The Discovery

Captain Zara stood on the bridge, her eyes fixed on the 
anomaly detected three parsecs away. The AI's analysis 
suggested it was artificial—a structure predating known 
civilization by millennia...

[Character Decision Point]
> Investigate immediately
> Report to Command first
> Analyze from safe distance
```

---

## API Reference

### Main Classes

```python
class StoryGenerator:
    def generate_story(**kwargs) -> Story
    def create_interactive(**kwargs) -> InteractiveStory
    def add_character(Character) -> None
    def set_world_state(WorldState) -> None
    
class Story:
    narrative: str
    characters: List[Character]
    events: List[Event]
    world_state: WorldState
    
class Character:
    name: str
    traits: List[str]
    relationships: Dict[str, Relationship]
    goals: List[Goal]
    memories: List[Memory]
```

---

## Technical Stack

- **Python 3.8+**: Core language
- **Natural Language Processing**: Text generation
- **Graph Algorithms**: Relationship networks
- **State Machines**: Character behavior
- **Random Number Generation**: Controlled randomness with seeds

---

## Use Cases

- **Creative Writing**: Story ideation and development
- **Game Development**: Dynamic quest generation
- **Interactive Fiction**: Branching narratives
- **Education**: Story structure teaching
- **Entertainment**: Automated storytelling

---

## Future Development

- Machine learning integration for improved coherence
- Voice narration output
- Visual novel generation
- Multi-language support
- Collaborative storytelling features
- Integration with game engines

---

*Create infinite unique stories with procedural generation*
