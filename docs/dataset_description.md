# Dataset Description

This study uses a structured child face dataset collected in a controlled kindergarten environment.

---

## Dataset Composition

- 27 children
- 3 poses per subject (Front, Left, Right)
- Approximately 100 augmented images per pose
- Total images: ~8100

All images were resized to 256×256 resolution before processing.

---

## Directory Structure

![Dataset Structure](../images/dataset_structure.png)

Example folder organization:

Subject_01/
- front/
- left/
- right/

Each pose folder contains augmented variations.

---

## Purpose of Structured Dataset

The dataset was intentionally organized by pose to:

- Enable pose-specific embedding benchmarking
- Reduce cross-pose variance
- Ensure fair model comparison

---

## Privacy Note

Due to ethical and privacy considerations involving minors, the dataset is not publicly released.
