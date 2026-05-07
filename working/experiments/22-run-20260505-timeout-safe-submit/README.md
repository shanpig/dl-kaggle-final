# Experiment 22 - Timeout-Safe Final Submission

Date: 2026-05-05

Purpose:
- Ensure completion within time limit after repeated training timeouts.

Mode:
- `do_train = False`
- `do_val_eval = False`
- `do_test_inference = True`

Inference speed settings:
- `scoring_mode = "letter"` (fastest single-pass choice scoring)
- `verbose_every = 50`

Adapter source:
- Uses pretrained adapter via `CFG["paths"]["pretrained_adapter_dir"]`
- Ensure Kaggle input dataset path is valid.
