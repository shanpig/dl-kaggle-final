# Experiment 21 - Train on Train+Val for Final Submission

Date: 2026-05-04

Purpose:
- Use all labeled data (`train + val`) to maximize final training signal before submission.

Key changes:
- `mode.do_train = True`
- `mode.do_val_eval = False`
- `mode.do_test_inference = True`
- Training dataframe changed to:
  - `train_df_run = pd.concat([train_df, val_df], axis=0).reset_index(drop=True)`

Notes:
- No validation metric is produced in this run (by design), because validation data is used for training.
- This run is intended purely for final submission generation.
