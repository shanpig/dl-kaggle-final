# Experiment Run: kaggle-friendly-v1

Run timestamp: 2026-04-25 19:19:21 (local)
Source notebook: `working/baseline-starter-notebook.ipynb`
Copied notebook: `baseline-starter-notebook__kaggle-friendly-v1__20260425-191921.ipynb`

## Why this run folder exists
This folder is a frozen snapshot for one experiment iteration so we can:
- avoid changing previous submit code
- keep reproducible run metadata
- track exactly what changed per run

## What was changed in this run
- Created a timestamped copy of the current baseline notebook.
- Added reproducibility docs (`README.md`) and experiment config manifest (`experiment-config.template.json`).
- No model/training logic has been changed yet in this run.

## Planned Kaggle-friendly upgrades for next edit pass
1. Build strict evaluator
- Evaluate by option-letter score among valid choices only (A..E as needed)
- Prevent invalid option predictions by masking to `num_choices`
- Report consistent validation accuracy metric

2. Add QLoRA fine-tuning pipeline
- 4-bit quantized base model + LoRA adapters
- Keep trainable params <= 5M
- Save adapter checkpoints and best checkpoint metadata

3. Centralize experiment controls at top of notebook
- Put all tunable settings in one config block
- Emit the resolved config to output artifacts for every run

## Required per-run artifacts (to produce in notebook)
- `submission.csv`
- `config.json`
- `metrics.json`
- `train_log.csv`
- `best_checkpoint/` (adapter + tokenizer/processor refs as needed)

## Changelog format for future edits
When this notebook is edited, append an entry below:

### YYYY-MM-DD HH:MM:SS - short title
- Changed:
- Reason:
- Expected impact:
- Validation result:


### 2026-04-25 19:21:00 - Strict evaluator appended
- Changed: Added section 4 in notebook with strict multi-choice evaluator, strict val loop, and strict test submission generation.
- Reason: Free-form generation can output non-choice text and unstable predictions.
- Expected impact: More stable and usually higher validation accuracy for MCQ by scoring only valid options.
- Validation result: Pending execution on Kaggle runtime.
