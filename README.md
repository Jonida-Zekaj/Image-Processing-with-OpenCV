# Image Processing with OpenCV - Color Space Conversion & Detection

This project demonstrates fundamental image processing techniques using OpenCV, focusing on color space conversions and binary mask creation for color detection.

## Project Overview

This assignment covers essential concepts in digital image processing:
- **RGB to BGR color space conversion** for OpenCV compatibility
- **BGR to HSV color space transformation** for color-based image analysis
- **Binary mask creation** for targeted color detection

## Features

### 1. Color Space Conversion
- **RGB → BGR**: Converts standard RGB images to OpenCV's native BGR format
- **BGR → HSV**: Transforms images to HSV color space for more intuitive color detection
  - **Hue (H)**: 0-179 (light wavelengths)
  - **Saturation (S)**: 0-255 (color vibrancy and intensity)
  - **Value (V)**: 0-255 (brightness/darkness)

### 2. Binary Masking
- Creates binary masks to isolate specific colors in images
- Defines lower and upper HSV bounds for target color ranges
- Produces white (255) pixels for matching colors and black (0) pixels for non-matching areas

### 3. Visualization
- Displays original, converted, and processed images side-by-side
- Provides immediate visual feedback on transformations

## Installation

### Requirements
```bash
pip install opencv-python
pip install numpy
pip install matplotlib
pip install Pillow
```

Or install all dependencies at once:
```bash
pip install -r requirements.txt
```

## Quick Start

### Running in Google Colab (Recommended)
Click the badge at the top of the notebook to open directly in Google Colab.

### Running Locally
1. Clone this repository
2. Install dependencies (see Installation section above)
3. Open the Jupyter notebook:
   ```bash
   jupyter notebook "Image Processing with OpenCV.ipynb"
   ```
4. Modify the image path in the notebook to point to your local images
5. Run all cells

## Dependencies

| Library | Version | Purpose |
|---------|---------|---------|
| opencv-python | Latest | Computer vision operations |
| numpy | Latest | Numerical computations |
| matplotlib | Latest | Image visualization |
| Pillow | Latest | Image processing utilities |

## Usage

### For Google Colab
1. Mount your Google Drive when prompted
2. Ensure `RGBImage.jpg` is in your Google Drive root (`/content/drive/MyDrive/`)
3. Run all cells sequentially

### For Local Execution
1. Replace Google Drive paths with local file paths
2. Replace `cv2_imshow()` with `plt.imshow()` and `plt.show()` for visualization
3. Run cells in order

## Project Structure

```
Image Processing with OpenCV     # Main Jupyter notebook
README.md                        # This file
requirements.txt                 # Python dependencies
```

## Learning Outcomes

After completing this project, you will understand:
- How different color spaces represent color information
- Why OpenCV uses BGR instead of RGB
- How HSV relates to human perception of color
- How binary masks isolate specific colors in images
- Image processing pipeline fundamentals

## Color Space Reference

### RGB vs BGR
- **RGB** [255, 0, 0] → Red color (Red channel first)
- **BGR** [255, 0, 0] → Blue color (Blue channel first)

OpenCV uses BGR because it was optimized for this format historically.

### HSV Color Cone
Use the HSV Color Cone to identify the range of values for your target color:
- **Reds**: H ≈ 0-10, 170-179
- **Greens**: H ≈ 40-80
- **Blues**: H ≈ 100-140
- **Yellows**: H ≈ 15-40

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Image fails to load | Verify file path and permissions; ensure image format is supported (JPG, PNG, etc.) |
| AttributeError: cv2_imshow | You're not in Google Colab; use `plt.imshow()` instead |
| ImportError: google.colab | This project requires Google Colab; remove/modify Colab-specific imports for local use |
| Colors appear incorrect | OpenCV reads images in BGR format; use `cv2.cvtColor()` to convert if needed |

## References

- [OpenCV Documentation](https://docs.opencv.org/)
- [HSV Color Space](https://en.wikipedia.org/wiki/HSL_and_HSV)
- [Digital Image Processing Fundamentals](https://en.wikipedia.org/wiki/Digital_image_processing)