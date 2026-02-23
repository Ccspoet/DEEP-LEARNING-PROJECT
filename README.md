# DEEP-LEARNING-PROJECT
# Rose Flower Classification Dataset

## Overview
This dataset is a curated collection of high-quality images of roses, designed for computer vision tasks such as image classification, detection, and quality grading. It categorizes roses primarily by color, providing a robust baseline for machine learning models to distinguish between subtle botanical variations.

## Dataset Structure
The data is organized into categorical folders based on flower color:
- **Red Roses**: Primary collection featuring various shades from bright scarlet to deep crimson.
- **Yellow Roses**: Includes varieties ranging from lemon yellow to golden hues.
- **Pink Roses**: Captures variations from soft pastel blush to vibrant fuchsia.
- **White Roses**: Features pure white, cream, and off-white rose varieties.

## Data Specifications
- **Format**: `.jpg` or `.png` images.
- **Resolution**: High-quality captures from multiple angles and lighting conditions.
- **Diversity**: Includes roses at various growth stages (buds to full bloom) and diverse backgrounds to ensure model generalization.

## Usage
### Requirements
- Python 3.x
- TensorFlow/Keras or PyTorch
- OpenCV / PIL (for image processing)

### Loading Data
```python
import tensorflow as tf

train_ds = tf.keras.utils.image_dataset_from_directory(
  'path_to_data',
  validation_split=0.2,
  subset="training",
  seed=123,
  image_size=(224, 224),
  batch_size=32)
