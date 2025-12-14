# George David Dickinson - Research Website

Personal research website showcasing work in calcium signaling, super-resolution microscopy, and computational biology.

**Live Site:** https://gddickinson.github.io

---

## About

This site documents my research career across multiple labs and institutions, focusing on:

- PIEZO1 mechanosensitive channels
- DNA-based information storage
- Single-molecule calcium imaging
- Super-resolution microscopy
- Scientific software development

---

## Structure

```
├── Research
│   ├── Current Position (Pathak Lab - PIEZO1)
│   ├── Boise State (DNA Memory)
│   ├── Parker Lab (IP3R Calcium Imaging)
│   ├── Patel Lab (NAADP Receptors)
│   ├── Sanders Lab (Plant Calcium)
│   └── Sound Science (Conservation)
├── Python Projects
│   ├── FLIKA Plugins
│   └── Other Projects
├── Publications (34 papers)
└── CV
```

---

## Local Development

### Setup

```bash
# Clone repository
git clone https://github.com/gddickinson/gddickinson.github.io
cd gddickinson.github.io

# Install dependencies
pip install -r requirements.txt

# Run local server
mkdocs serve
```

Visit http://127.0.0.1:8000

### Building

```bash
mkdocs build
```

---

## Deployment

The site automatically deploys to GitHub Pages when you push to the main branch.

### Manual Deployment

```bash
mkdocs gh-deploy
```

---

## Built With

- [MkDocs](https://www.mkdocs.org/)
- [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)
- GitHub Pages

---

## Adding Content

### Research Pages

Add new research sections in `docs/research/`

### Python Projects

Add project documentation in `docs/python-projects/`

### Publications

Update `docs/publications.md` with new publications

### Images

Add images to appropriate directories and reference in markdown:

```markdown
![Description](path/to/image.png)
```

---

## Configuration

Main configuration in `mkdocs.yml`:

- Site metadata
- Navigation structure
- Theme settings
- Extensions

---

## Contact

- GitHub: [gddickinson](https://github.com/gddickinson)
- LinkedIn: [Profile](https://www.linkedin.com/in/george-dickinson-3bb24b89/)
- Google Scholar: [Publications](https://scholar.google.com/citations?user=IyfrHWkAAAAJ&hl=en)

---

## License

Content © 2024 George Dickinson

---

*Last updated: December 2024*
