# Experiment 24 - Continue from Exp23 Adapter (Short Run)

Date: 2026-05-06

Goal:
- Fit one more run within ~7 hours by continuing from Exp23 instead of retraining from scratch.

Key changes from Exp23:
- `continue_from_adapter = True`
- `pretrained_adapter_dir = /kaggle/input/exp23-best-adapter/best_adapter`
- Short continuation training:
  - `num_epochs = 0.35`
  - `learning_rate = 5e-5`
  - `warmup_ratio = 0.02`

Expected behavior:
- Model loads base + LoRA structure, then initializes adapter weights from Exp23 and continues training.
- Submission is generated at the end (`do_test_inference=True`).

Important:
- In Kaggle, attach the dataset containing Exp23 `best_adapter` and confirm mount path matches `pretrained_adapter_dir`.
