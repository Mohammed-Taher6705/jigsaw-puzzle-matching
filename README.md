# Jigsaw Puzzle Matching — Image Processing & Matching Suite

## Overview

This repository contains a set of Jupyter notebooks implementing a complete pipeline for jigsaw-puzzle piece matching. The goal is to take raw puzzle-piece images, preprocess them, extract meaningful features, and match them accurately. The project demonstrates image-processing techniques, descriptor extraction, and matching algorithms, with an optional interactive UI for Google Colab.

Key goals:
- Prepare and clean puzzle-piece images
- Improve visual quality (denoising, enhancement)
- Extract descriptors and match pieces
- Demonstrate an interactive UI (Colab-only)

## Project Structure

- `Cropping.ipynb` — Tools and workflows to detect and crop puzzle pieces from full images.
- `Denoising.ipynb` — Image denoising methods and comparative outputs.
- `Enhancing.ipynb` — Contrast/color enhancement and sharpening steps.
- `Matching.ipynb` — Core matching algorithms and evaluation (non-UI).
- `Matching_with_UI.ipynb` — Interactive matching demo with UI widgets (Colab only).
- Other assets: example images and generated outputs are stored alongside notebooks or produced at runtime.

If you open the repository in Jupyter, you'll find each notebook contains explanatory text, visual outputs, and cells to reproduce results step-by-step.

## Notebooks & What They Do

- `Cropping.ipynb`: Detects piece contours, crops pieces to individual images, and saves standardized piece images for downstream processing.
- `Denoising.ipynb`: Compares denoising filters (Gaussian) and demonstrates how denoising improves descriptor extraction.
- `Enhancing.ipynb`: Uses histogram equalization, CLAHE, and color adjustments to make features more prominent for matching.
- `Matching.ipynb`: Extracts features/descriptors edge-based, computes pairwise similarities, and demonstrates matching and scoring outputs.
- `Matching_with_UI.ipynb`: A notebook with interactive widgets (sliders/buttons) and a simple interface to try matching in a live session. NOTE: This notebook relies on interactive widget behavior and resources that are tested and supported on Google Colab; some widgets or file-handling steps may not work identically in a local Jupyter environment.

## Expected Outputs

- Cropped piece images (one file per piece) in an `cropped/` folder.
- Side-by-side comparisons showing raw vs. denoised vs. enhanced images.
- Matching results: pairs of matched pieces, similarity scores, and visualization overlays showing matched edges or keypoints.
- (Colab UI) An interactive interface to pick pieces and display top matches live.

## Requirements

Recommended (Python 3.8+). Exact dependencies depend on which notebook features you use; the most common packages are listed below.

- Python 3.8 or newer
- jupyter or jupyterlab
- numpy
- matplotlib
- opencv-python
- scikit-image
- scikit-learn
- ipywidgets (for interactive notebook)


## Installation (local)

1. Create and activate a virtual environment:

```powershell
python -m venv .venv
.\\.venv\\Scripts\\Activate.ps1   # PowerShell on Windows
```

2. Install core packages:

```powershell
pip install --upgrade pip
pip install jupyterlab numpy matplotlib opencv-python scikit-image scikit-learn ipywidgets
```

3. Start Jupyter Lab or Notebook:

```powershell
jupyter lab
# or
jupyter notebook
```

4. Open the notebook you want to run (e.g., `Cropping.ipynb`). Run cells top-to-bottom.

Notes:
- Some notebooks may save outputs to local `outputs/` or  folders — create them if needed.
- If a notebook imports packages you don't have installed, install them with `pip install <package>`.
- If runtime errors reference GPU or CUDA, either run on Colab or remove GPU-specific code paths.

## Running `Matching_with_UI.ipynb` (Colab)

`Matching_with_UI.ipynb` is designed and tested for Google Colab. To run it:

1. Open Colab: https://colab.research.google.com
2. Upload the `Matching_with_UI.ipynb` file or open it from your Drive.
3. Ensure runtime is set (GPU not required unless specified by the notebook).
4. Run all cells. Follow any file-upload prompts in the notebook to provide images.

Important: interactive widgets that rely on `ipywidgets` or browser integrations often behave more predictably in Colab. If a UI widget does not render locally, try the Colab environment.

## Tips & Troubleshooting

- If images are not found, ensure the working directory shown by Jupyter matches where your image files are stored.
- To reproduce results exactly, run each notebook from top to bottom without skipping cells.
- If a cell fails due to a missing package, error message usually shows which package to install.


## License & Contact

Author: Mohammed Magdy Taher

GitHub: https://github.com/Mohammed-Taher6705

Email: MohammedTaher.6705@gmail.com 


Questions or changes? message me.
