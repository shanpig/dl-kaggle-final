# Experiment 23 - Left-Inspired Train+Val

Date: 2026-05-05

Base:
- Copied from Exp21 train+val submission notebook.

Changes borrowed from `left/` (0.75 reference):
1. Choice-order augmentation during training:
   - Randomly permute choices per sample and remap the answer index.
2. Inference scorer switched to robust per-choice answer-token log-likelihood:
   - Batch all candidate answer letters with right-padding,
   - score each choice by log-prob of its answer token position.

Existing setup retained:
- Train on `train + val`.
- No val eval (submission-focused).
- Test inference enabled to produce `submission.csv`.
