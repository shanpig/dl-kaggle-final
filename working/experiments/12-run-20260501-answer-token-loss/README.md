# Experiment 12: Answer-Token-Only Loss

Source: `07-run-20260430-lr-recovery-from-exp05`
Notebook: `baseline-starter-notebook__qlora-answer-token-loss__20260501.ipynb`

## Goal
High-effect change: train only on the answer token after `Answer:`.

## What changed
- Replaced training dataset/collator logic to supervise only the final answer token.

## What stayed fixed
- Same config/hyperparameters as exp07 baseline unless edited in CFG.
