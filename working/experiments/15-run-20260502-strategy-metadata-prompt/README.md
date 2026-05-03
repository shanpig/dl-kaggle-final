# Experiment 16 - Strategy: Metadata + Prompt Cue

Date: 2026-05-02

Base:
- Copied from Exp14 full-context run (val_acc 0.65 on 400-val subset).

Strategy-file changes applied:
1. Add metadata to prompt (`subject`, `grade`, `topic`).
2. Change answer cue from `Answer:` to `The correct answer is:`.

Implementation details:
- New prompt config:
  - `use_metadata: True`
  - `answer_cue: "The correct answer is:"`
- `build_prompt_cfg` now appends a `Metadata:` block when available.
- Existing lecture+hint context remains enabled from Exp14.

Run mode:
- Validation-first (no test submission) to measure pure impact.
