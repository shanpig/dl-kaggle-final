# Experiment 18 - Full Choice-Likelihood Inference (No Retrain)

Date: 2026-05-03

Base:
- Copied from Exp17 (best current submission recipe).

Goal:
- Improve answer selection by replacing single-letter next-token scoring with full-choice likelihood scoring.
- Reuse Exp17 adapter without retraining.

Key changes:
1. Inference scoring upgrade:
   - For each candidate option, score log-likelihood of completion text:
     `" {letter}. {choice_text}"`
   - Select option with highest summed candidate token log-probability.
2. Prompt alignment:
   - Evaluator now uses `build_prompt_cfg(...)` when available, so evaluation prompt matches training prompt configuration.
3. No retrain mode:
   - `mode.do_train = False`
   - Loads adapter via `PeftModel.from_pretrained(...)`.

Config notes:
- `paths.pretrained_adapter_dir` is set to:
  `/kaggle/input/exp17-best-adapter/best_adapter`
- On Kaggle, attach the Exp17 output as a dataset and adjust this path if dataset mount name differs.

Run mode:
- `do_val_eval = True`
- `do_test_inference = True`
- Produces both validation metrics and `submission.csv`.

## Outcome / Decision

Run observation (Kaggle logs):
- Early validation progress was significantly below expected baseline:
  - 10/400: running_acc=0.3000
  - 20/400: running_acc=0.3000
  - 30/400: running_acc=0.2333
  - 40/400: running_acc=0.3000
- Throughput was ~0.15-0.17 samples/s, with ETA ~35-42 minutes for val(400).

Decision:
- Skipped/aborted this experiment for final selection.

Reason for skipping:
- Early accuracy trend was far below prior strong runs (Exp14/Exp16/Exp17 around ~0.65-0.67 val on comparable settings), so continuing would likely consume quota without leaderboard upside.
