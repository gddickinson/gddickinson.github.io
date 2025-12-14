# FLIKA Plugins

Plugins extending FLIKA (Fluorescence Image Analysis) for advanced microscopy workflows.

**FLIKA:** [flika-org.github.io](https://flika-org.github.io)
**GitHub:** [github.com/gddickinson/flika_plugins](https://github.com/gddickinson/flika_plugins)

---

## Available Plugins

### [thunderSTORM](thunderstorm.md)
Single Molecule Localization Microscopy analysis.

**Features:**
- Super-resolution image reconstruction
- Localization precision analysis
- Drift correction
- Batch processing

---

### [SPT Batch Analysis](spt-batch.md)
Automated particle tracking for large datasets.

**Features:**
- Multiple tracking algorithms
- U-Track integration
- Interpolation and gap-closing
- Comprehensive export options

---

### [Cell Edge Movement](cell-edge.md)
Membrane dynamics and protein localization analysis.

**Features:**
- Edge detection and tracking
- Velocity field calculation
- Protein colocalization
- PIEZO1 analysis tools

---

### [Mask Editor](mask-editor.md)
Interactive ROI and mask editing tool.

**Features:**
- Frame-by-frame editing
- Boolean and morphological operations
- Multiple selection tools
- Export to multiple formats

---

## Installation

```bash
# Install FLIKA
pip install flika

# Clone plugins
git clone https://github.com/gddickinson/flika_plugins

# Copy to FLIKA plugins directory
cp -r flika_plugins/* ~/.flika/plugins/
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
