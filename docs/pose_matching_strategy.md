# Pose-Specific Matching Strategy

Traditional face recognition systems compare a test image against all stored embeddings.

This creates errors when pose differs between test and reference images.

---

## Proposed Strategy

If a test image is left-facing, it is compared only with stored left-facing embeddings.

Front and right embeddings are ignored during matching.

This reduces cross-pose mismatch.

---

## Why This Works

Facial geometry changes with pose.

Comparing left pose with front pose introduces embedding variance.

By restricting comparison to same-pose embeddings:
- Similarity scores become more stable
- False matches decrease
- Accuracy improves

---

## Example Illustration

![Pose Specific Matching](../images/pose_matching_example.png)

In the figure:
- Left test image → matched only with left references
- Other pose embeddings are excluded

---

## Impact on Performance

Pose-aware matching contributed significantly to achieving the final 97.53% accuracy.
