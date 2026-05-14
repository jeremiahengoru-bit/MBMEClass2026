# Brain CT Scan — Tumor vs. Normal Classifier

A deep learning notebook that classifies brain CT scan images as **Healthy** or **Tumor** using a convolutional neural network built with TensorFlow/Keras.

## Overview

`GroupClassifier.ipynb` loads a labeled dataset of brain CT scans, preprocesses the images (resize to 128×128, normalize), trains a CNN classifier, and reports accuracy/loss along with sample predictions.

- **Task:** Binary image classification (Healthy vs. Tumor)
- **Input size:** 128 × 128 × 3
- **Framework:** TensorFlow / Keras
- **Environment:** Google Colab (recommended) or local Jupyter

## Dataset

The notebook expects a folder structured by class:

```
CT scan Images (limited)/
├── Healthy/
│   ├── img001.jpg
│   └── ...
└── Tumor/
    ├── img001.jpg
    └── ...
```

In Colab the default path is `/content/drive/MyDrive/CT scan Images (limited)`. Update the `DATA_DIR` variable in the notebook to point to your own dataset location.

## Quick Start (Google Colab)

1. Open `GroupClassifier.ipynb` in [Google Colab](https://colab.research.google.com/).
2. Mount Google Drive when prompted.
3. Place your dataset under `MyDrive/CT scan Images (limited)` (or update the path in the notebook).
4. Run all cells.

## Local Setup

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook GroupClassifier.ipynb
```

When running locally, replace the Google Drive mount cell with a local path, e.g.:

```python
DATA_DIR = "./sample_images/CT scan Images (limited)"
```

## Dependencies

See `requirements.txt`. Core libraries:

- numpy, scipy, scikit-learn
- opencv-python, Pillow
- matplotlib
- tensorflow (Keras)
- jupyter / notebook

## Project Structure

```
.
├── GroupClassifier.ipynb   # Main notebook
├── requirements.txt        # Python dependencies
├── .gitignore
├── LICENSE
├── README.md
└── sample_images/          # Place local datasets here (gitignored)
```

## Results

Training and validation accuracy/loss curves, a confusion matrix, and sample predictions are produced inline in the notebook.

## Contributing

Pull requests are welcome. For major changes, open an issue first to discuss what you would like to change.

## License

[MIT](LICENSE)
