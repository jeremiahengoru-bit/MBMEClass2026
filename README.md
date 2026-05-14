# Group 2 Image Segmenter

A collection of classical and machine-learning–based image segmentation techniques implemented in a single Jupyter notebook (`Group2segmenter.ipynb`). The notebook compares multiple segmentation approaches (thresholding, K-Means clustering, morphological operations, etc.) and visualizes the results side by side.

> Originally developed in Google Colab. It also runs locally with a standard Python/Jupyter environment (see notes below).

## Features

- Image preprocessing (Gaussian blur, normalization, histogram equalization)
- Multiple segmentation techniques compared on the same input
- K-Means clustering–based segmentation (scikit-learn)
- Morphological post-processing (dilation / erosion)
- Visualization utilities to overlay masks on the original image
- TensorFlow available for deep-learning–based extensions

## Repository structure

```
.
├── Group2segmenter.ipynb     # Main notebook
├── requirements.txt          # Python dependencies
├── README.md                 # This file
├── LICENSE                   # MIT License
├── .gitignore                # Python / Jupyter ignores
└── sample_images/            # (Optional) put test images here
```

## Getting started

### Option 1 — Google Colab (recommended, zero setup)

1. Upload `Group2segmenter.ipynb` to [Google Colab](https://colab.research.google.com/).
2. Run all cells. When prompted, upload an image using the Colab file picker.

### Option 2 — Run locally

Requires Python 3.9–3.11.

```bash
# 1. Clone the repo
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>

# 2. Create a virtual environment
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Launch Jupyter
jupyter notebook Group2segmenter.ipynb
```

> **Note:** the notebook uses `from google.colab import files` to upload images. When running locally, replace those cells with a direct path, e.g.:
> ```python
> from PIL import Image
> import numpy as np
> image = np.array(Image.open("sample_images/your_image.png"))
> ```

## Dependencies

See [`requirements.txt`](./requirements.txt). Main libraries:

- numpy, scipy, scikit-learn
- opencv-python
- matplotlib, Pillow
- tensorflow
- jupyter

## Usage

1. Load and preprocess an image with `ImageUtils.preprocess_image()`.
2. Run one or more segmentation methods.
3. Use `ImageUtils.visualize_results(original, results_dict)` to compare outputs.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

[MIT](./LICENSE)

## Authors

Group 2
