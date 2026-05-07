# Experiment 20 - Fast Final Submission (Timeout-Avoidance)

Date: 2026-05-04

Why this edit:
- Exp19 timed out after long training (~42k s) and did not finish the full eval/submission pipeline.
- To avoid wasting final quota, Exp20 is switched to fast inference mode using a proven adapter.

Current mode:
- `do_train = False`
- `do_val_eval = False`
- `do_test_inference = True`
- Loads pretrained adapter from:
  - `CFG["paths"]["pretrained_adapter_dir"]`
  - default: `/kaggle/input/exp17-best-adapter/best_adapter`

Model and scorer:
- Base model: `HuggingFaceTB/SmolVLM-500M-Instruct`
- Hybrid scorer retained (`full-choice` + `letter` blend) for stronger inference quality.

Notes:
- Attach the dataset containing Exp17 `best_adapter` in Kaggle and verify the mount path.
- This configuration prioritizes finishing and producing `submission.csv` within time limits.
