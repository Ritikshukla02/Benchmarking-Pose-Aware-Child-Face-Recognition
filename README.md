# Benchmarking Pose-Aware Child Face Recognition
Pose-aware child face recognition pipeline (Under Publication at ICICIC 2025)

**Best Accuracy Achieved: 97.53%(FaceNet512)**

## Why This Project Matters
Recognizing children's faces is significantly harder than recognizing adults.

Children:
- Have very similar facial structures
- Are still growing, causing facial changes
- Have fewer distinctive features
- Show high variation across poses

Most modern face recognition models are trained primarily on adult datasets.  
When applied to children, their performance often drops due to poor generalization.

This project focuses on building a structured and reliable pipeline specifically designed for child face identification.

## Core Idea
Instead of comparing every test image with all stored embeddings, this system:

- Stores embeddings separately for each pose (Front, Left, Right)
- Matches test images only with embeddings of the same pose
- Removes noisy embeddings using cosine similarity filtering
- Applies L2 normalization for stable comparison

This reduces pose mismatch errors and improves classification stability.

---

## System Pipeline Overview
The system follows a carefully designed multi-stage pipeline:

1. Face Detection (DSFD)
2. Face Cropping
3. Image Resizing (256×256)
4. Data Augmentation
5. Embedding Extraction
6. L2 Normalization
7. Outlier Filtering (Cosine threshold = 0.75)
8. Pose-Specific Embedding Averaging
9. Cosine Similarity Matching (Threshold = 0.65)

### Complete Pipeline Diagram

![Pipeline Overview](images/pipeline_overview.png)

---

## Models Benchmarked
The following face recognition models were evaluated under identical preprocessing conditions:

- FaceNet512
- Dlib
- VGG-Face
- ArcFace

All models were accessed using the DeepFace framework to ensure consistent embedding extraction.

---

## Key Technical Contributions

- Designed a pose-specific embedding pipeline
- Implemented cosine-based outlier filtering
- Applied L2 normalization for embedding stability
- Conducted structured benchmarking of four models
- Demonstrated 97.53% identification accuracy in a controlled setting

---

## Detailed Documentation
- [dataset_description](docs/dataset_description.md)
- [System Pipeline](docs/system_pipeline.md)
- [Model Benchmarking & Results](docs/model_benchmarking.md)
- [Pose-Specific Matching Strategy](docs/pose_matching_strategy.md)
- [limitations_and_future_work](docs/limitations_and_future_work.md)
  
---

## 🔐 Dataset Availability

Due to privacy and ethical considerations involving children, the TriPose-Kids dataset is not publicly available.
Sample structure is shown in the documentation.
