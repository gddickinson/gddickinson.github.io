# FLIKA Plugins

Plugins extending FLIKA (Fluorescence Image Analysis) for advanced microscopy workflows.

**FLIKA:** [flika-org.github.io](https://flika-org.github.io)  
**GitHub:** [github.com/gddickinson](https://github.com/gddickinson)

---

## Available Plugins

### thunderSTORM
Single Molecule Localization Microscopy analysis.

**Features:**
- Super-resolution image reconstruction
- Localization precision analysis
- Drift correction
- Batch processing

[Documentation →](thunderstorm.md)

---

### SPT Batch Analysis  
Automated particle tracking for large datasets.

**Features:**
- Multiple tracking algorithms
- U-Track integration
- Interpolation and gap-closing
- Comprehensive export options

[Documentation →](spt-batch.md)

---

### Cell Edge Movement
Membrane dynamics and protein localization analysis.

**Features:**
- Edge detection and tracking
- Velocity field calculation
- Protein colocalization
- PIEZO1 analysis tools

[Documentation →](cell-edge.md)

---

### Mask Editor
Interactive ROI and mask editing tool.

**Features:**
- Frame-by-frame editing
- Boolean and morphological operations
- Multiple selection tools
- Export to multiple formats

[Documentation →](mask-editor.md)

---

## Installation

```bash
# Install FLIKA
pip install flika

# Clone plugins
git clone https://github.com/gddickinson/flika-plugins

# Copy to FLIKA plugins directory
cp -r flika-plugins/* ~/.flika/plugins/
```

---

## Development

All plugins follow FLIKA's plugin architecture with:
- `__init__.py` - Module initialization
- `plugin_main.py` - Core functionality
- `info.xml` - Plugin metadata
- `about.html` - Plugin description

---

*Detailed documentation for each plugin available via links above.*
