# Experiment 20 - Aggressive Final Push

Date: 2026-05-03

Base:
- Copied from Exp19 hybrid scorer setup.

Goal:
- Maximize final leaderboard upside with one aggressive run.

Changes vs Exp19:
- `run_name`: `qlora-final-aggr-<timestamp>`
- `training.num_epochs`: `2` (from `1`)
- `training.learning_rate`: `8e-5` (from `1e-4`)
- `training.warmup_ratio`: `0.03` (from `0.05`)
- `inference.hybrid_weight_fullchoice`: `0.85` (from `0.70`)

Unchanged:
- Same model family and QLoRA target modules as best-performing pipeline.
- Validation + test inference both enabled, producing `submission.csv`.

Risk/Reward:
- Higher potential gain from stronger training + semantic-heavy choice scoring.
- Higher overfit/time risk than conservative runs.
