# Experiment 07: LR Recovery from Exp05

Source: `05-run-20260430-155832-qlora-scaleup-baseline`
Notebook: `baseline-starter-notebook__qlora-lr1e4__20260430.ipynb`

## Goal
Single controlled recovery test after exp06 degradation.

## Only change from Exp05
- `learning_rate`: `2e-4 -> 1e-4`

## Everything else fixed
- `max_train_samples=1024`
- `max_val_samples=400`
- `num_epochs=1`
- `gradient_accumulation_steps=16`
- `lora_r=8`, `lora_alpha=16`, `lora_dropout=0.05`
- `img_size=192`
- `use_hint=False`, `use_lecture=False`
- `do_test_inference=False`
