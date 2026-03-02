# Model Benchmarking & Results

This study evaluates four widely used face recognition models under identical preprocessing conditions.

---

## Models Compared

- FaceNet512
- Dlib
- VGG-Face
- ArcFace

All models were tested using:
- Same dataset
- Same augmentation
- Same normalization
- Same matching strategy

This ensures fair comparison.

---

## Evaluation Metric

Accuracy (%) was used to measure identification performance.

Cosine similarity was used as the distance metric.

---

## Results

![Results Comparison](../images/results_comparison.png)

---

## Key Observations

- FaceNet512 performed best overall.
- High-resolution compatibility improved performance.
- Preprocessing quality had significant impact.
- ArcFace underperformed due to input constraints.
