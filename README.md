# Image Bayer Filtering Project

This repository contains two Jupyter notebooks that explore the use of Bayer
matrices for ordered dithering and color reconstruction on a sample image
("swiss.jpg").

## Notebooks

### `Bayer_Expandable.ipynb`
- Defines a sequence of 4x4 Bayer matrices representing different threshold
  patterns.
- Plots the matrices to visualize the dithering patterns.
- Loads a grayscale version of `swiss.jpg` and applies an expanded Bayer
  matrix to each pixel, generating a larger, dithered output image.
- Saves the result as `bayer_4x4_swiss.jpg`.

### `Program.ipynb`
- Reads the same `swiss.jpg` image and preserves a color copy.
- Converts the image to grayscale, displays and saves the result.
- Thresholds the grayscale image to black-and-white.
- Defines a set of 2x2 Bayer filter matrices and visualizes them.
- Implements a function to select a filter based on local intensity.
- Applies the filter across the image, displays and saves the dithered
  grayscale and color-embedded versions (`swiss_bayer_2x2.jpg` and
  `swiss_bayer_color.jpg`).

## Usage

1. Place `swiss.jpg` in the workspace root or adjust the paths in the
   notebooks as needed.
2. Open either notebook in Jupyter or VS Code and run the cells sequentially.
3. Inspect generated images and modify thresholding or filter logic
   to experiment with different effects.

## Requirements

The notebooks use the following Python packages:

- `numpy`
- `matplotlib`
- `opencv-python` (imported as `cv2`)
- `Pillow` (optional)

Install them via `pip install -r requirements.txt` if you wish to run the
notebooks in a new environment.  

## Notes

This project is primarily educational and demonstrates how Bayer matrices
can simulate halftone patterns and how simple color reconstruction can be
performed by combining a monochrome mask with a color image.
