# VulnuScope

**Lightweight AI Wound Analysis**

VulnuScope is a flask application powering automatic wound segmentation, metric extraction.

![App Screenshot](screen.png)

## Key Features

* **Instance Segmentation**: Precise masking via Mask R-CNN R50-FPN.
* **Clinical Metrics**: Area, perimeter, circularity, redness index, and depth proxy.
* **Tissue Analysis**: Heuristic segmentation of Granulation, Slough, and Necrotic tissue.
* **Visualizations**: Pseudo-3D surface plots, color histograms, and healing simulations.
* **Exportable Data**: Generates composite reports, CSV metrics, and full ZIP archives.

## Installation

### 1. Environment Setup (Python 3.12 Recommended)
We use a specific installation order to ensure Detectron2 compiles correctly with CPU support.

```bash
# Create and activate environment
python3 -m venv venv
source venv/bin/activate

# Step 1: Install Build Tools & PyTorch (CPU)
pip install torch==2.5.1 torchvision==0.20.1 --index-url https://download.pytorch.org/whl/cpu

# Step 2: Install remaining dependencies
pip install -r requirements.txt

# Step 3: Install Detectron2
pip install "git+https://github.com/facebookresearch/detectron2.git" --no-build-isolation
```

## License

© 2025 VulnuScope by XRadion Dynamics. See `LICENSE`.
