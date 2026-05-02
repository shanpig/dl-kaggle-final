# Experiment 07: QLoRA Scale-Up 2048

Source: `05-run-20260430-155832-qlora-scaleup-baseline`
Notebook: `baseline-starter-notebook__qlora-scaleup-2048__20260430.ipynb`

## Goal
Continue non-ablation scaling with all hyperparameters fixed.

## Only change from Exp05
- `max_train_samples`: `1024 -> 2048`

## Fixed settings retained
- `max_val_samples=400`
- `num_epochs=1`
- `learning_rate=2e-4`
- `lora_r=8, lora_alpha=16, lora_dropout=0.05`
- `img_size=192`
- `use_hint=False, use_lecture=False`
- `do_test_inference=False`
