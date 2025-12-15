# ai_agent

An extensible, modular framework for creating embodied AI agents that can interact with the world through various sensors and actuators.

**[View on GitHub →](https://github.com/gddickinson/ai_agent)**

---

## Overview

**Languages:** Python

## Documentation

# Embodied AI Agent

An extensible, modular framework for creating embodied AI agents that can interact with the world through various sensors and actuators.

## Overview

This project implements a cognitive architecture for AI agents that aims to model aspects of human cognition, including:

- **Perception**: Processing sensory inputs from cameras, microphones, and other sensors
- **Memory**: Storing and retrieving experiences, knowledge, and working memory
- **Cognition**: Reasoning, planning, and emotional processing
- **Consciousness**: A high-level interface with the external world that coordinates actions
- **Autonomy**: Self-directed thinking, curiosity-driven learning, and conversation initiation

The architecture is designed to be flexible and adaptable to different hardware platforms, from desktop computers to physical robots.

## Key Features

- **Modular Design**: Each component can be developed and tested independently
- **Multi-LLM Architecture**: Uses specialized LLMs for different cognitive functions
- **Hardware Abstraction**: Adapts to available sensors and actuators on different platforms
- **Memory Systems**: Includes working memory, episodic memory, and semantic memory
- **Simulated Hardware**: Provides simulated sensors and actuators for testing and development
- **Autonomous Thinking**: Generates internal thoughts, questions, and reflections
- **Proactive Communication**: Can initiate conversations based on interests and curiosity

## Project Structure

```
embodied_agent/
├── core/                   # Core cognitive modules
│   ├── agent.py           # Main agent orchestration
│   ├── autonomy.py        # Autonomous thinking capabilities
│   ├── consciousness.py   # "Conscious" interface LLM
│   ├── perception.py      # Sensory processing modules
│   ├── cognition.py       # Reasoning, emotions, planning
│   └── memory.py          # Memory management system
├── hardware/               # Hardware interfaces
│   ├── sensors.py         # Sensor 

*[View full README on GitHub]*

