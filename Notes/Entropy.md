# **Entropy in Image Processing**

Entropy in image processing is a measure of **uncertainty, randomness, or information content** in an image. It helps determine the level of variation in pixel intensities.

## **Mathematical Definition**

![alt text](image.png)

where:

- \( P(i) \) is the probability of pixel intensity \( i \) in the image.
- The summation runs over all possible pixel values (0-255 for grayscale images).
- A **higher entropy** indicates more complexity, while **lower entropy** suggests uniformity.

## **Entropy Characteristics in Images**

- **High Entropy**: Images with a lot of details, textures, and edges (e.g., natural scenes).
- **Low Entropy**: Plain or smooth images with little variation (e.g., solid color background).

## **Examples**

1. **Low-Entropy Image**: A plain white or black image (all pixels have the same intensity).
2. **High-Entropy Image**: A complex scene with multiple textures (e.g., trees, rocks).
3. **Medium-Entropy Image**: A semi-blurred image where some variations exist but not as much detail.

## **Applications**

✅ **Edge Detection** - High-entropy regions highlight textures and edges.  
✅ **Watermark Detection** - Watermarked images may have distinct entropy patterns.  
✅ **Compression** - Low-entropy images can be compressed efficiently.  
✅ **Image Segmentation** - Helps separate objects from the background.

## **Python Code for Image Entropy**

```python
import numpy as np
from skimage.measure import shannon_entropy
from skimage.io import imread

# Load image
image = imread("example.jpg", as_gray=True)

# Calculate entropy
entropy_value = shannon_entropy(image)
print(f"Image Entropy: {entropy_value}")
```
