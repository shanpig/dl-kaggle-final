# Best Result Repro (Main Branch)

This folder contains the best-performing reproducible run from our main branch experiments.

## Contents
- `baseline-starter-notebook__exp23-left-inspired-trainval__20260505.ipynb`
- `exp23_best_adapter.zip`

## Target Result
- Experiment: `E23`
- Public score: `0.70623`

## Dataset Setup (Required)
You must download the competition dataset from Kaggle and place it in this repo before running.

Expected local layout:

```text
input/competitions/pixels-to-predictions/
  train.csv
  val.csv
  test.csv
  images/
```

## Reproduce on Kaggle Notebook
1. Upload/open `baseline-starter-notebook__exp23-left-inspired-trainval__20260505.ipynb`.
2. Attach competition data in Kaggle (`/kaggle/input/...`).
3. Keep GPU enabled (T4).
4. If you want to reuse the trained adapter, upload `exp23_best_adapter.zip` as a Kaggle dataset and point the notebook path to it.
5. Run all cells and export `submission.csv` from the output run directory.

## Notes
- This is the best result on our main branch. The left branch achieved a higher score with a different versioned pipeline.
