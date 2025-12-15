# news_depoliticizer

A tool that aggregates news from multiple sources, ranks stories by importance, and uses a local LLM to rewrite them without political bias or inflammatory language.

**[View on GitHub →](https://github.com/gddickinson/news_depoliticizer)**

---

## Overview

**Languages:** Python

## Documentation

# News Depoliticizer

A tool that aggregates news from multiple sources, ranks stories by importance, and uses a local LLM to rewrite them without political bias or inflammatory language.

## Overview

News Depoliticizer helps readers consume news without the political spin and inflammatory language that often accompanies today's reporting. The project:

1. Legally collects news from multiple APIs (no web scraping)
2. Identifies and groups similar stories across sources
3. Ranks stories by prominence/importance
4. Uses a local LLM (via Ollama) to rewrite each story in a neutral, balanced tone
5. Presents the depoliticized stories through a clean web interface

## Features

- **Multi-source aggregation**: Collects news from NewsAPI, NY Times API, and The Guardian API
- **Story grouping**: Identifies the same stories across different sources
- **Importance ranking**: Orders stories based on their prominence across news outlets
- **Bias removal**: Rewrites stories to remove political bias and inflammatory language
- **Local processing**: All LLM operations run on your local machine, ensuring privacy
- **Clean web interface**: Mobile-friendly display of depoliticized news stories

## Requirements

- Python 3.8+
- Ollama (with llama3 model installed)
- API keys for news sources (optional, sample data provided)

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/news-depoliticizer.git
cd news-depoliticizer
```

### 2. Create a virtual environment (recommended)

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install required packages

```bash
pip install requests pandas numpy scikit-learn python-dotenv flask
```

### 4. Install Ollama (if not already installed)

Follow the [Ollama installation instructions](https://ollama.ai/download) for your platform.

Make sure the `llama3` model is installed:

```bash
ollama pull llama3
```

### 5. Set up API keys (optional)

Create a `.

*[View full README on GitHub]*

