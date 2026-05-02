# QLoRA Screening Matrix (v1)

## Strategy
1. Phase A (Prompt screening): pick best prompt context style with fixed QLoRA settings.
2. Phase B (Core QLoRA sweep): tune `lora_r` and `learning_rate`.
3. Phase C (Epoch tuning): compare short vs moderate training.
4. Phase D (Stability check): re-run best config with second seed.

## Runtime notes
- Baseline strict pipeline: ~42 min.
- Expected QLoRA screening run (train + val strict): ~90-150 min.
- Run test inference/submission only for top candidates.

## Promotion rule
Promote a run to test submission if:
- It improves validation strict accuracy by >= 0.8% absolute over current best, or
- It ties within 0.3% and has better stability/runtime.

## Planned runs
See `experiment-matrix.csv` for machine-readable schedule.
