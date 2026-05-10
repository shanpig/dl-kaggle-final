Your report must include the following sections:

| Section         | What to Cover                                                        |
| --------------- | -------------------------------------------------------------------- |
| Introduction    | Problem statement, motivation, summary of approach                   |
| Dataset         | Description of the provided dataset, any preprocessinor augmentation |
| Model           | Description Architecture, why you chose this approach                |
| Experimentation | Hyperparameter settings, training details, what you tried            |
| Results         | Quantitative results, comparisons, ablation studies                  |
| Conclusion      | Summary of findings, what worked, what didn’t, future directions     |

• Include a link to your GitHub repository with training/inference code.
• Include a link to your model weights (uploaded to cloud storage).
• Discuss what methods you tried, what worked, and what didn’t.
• Disclose any AI tooling (LLM assistants) used for coding/debugging.

---

## Note

Our github repos are:

- From Che Hung Liao: https://github.com/shanpig/dl-kaggle-final
  - Model weights:
    - exp17: https://www.kaggle.com/models/chehungliao/exp17-best-adapter
    - exp23: https://www.kaggle.com/models/chehungliao/exp23-best-adapter
- From Eleftherios Komvopoulos: https://github.com/lefteriskomvopoulos/PixelsToPredictions
  - Model weights:
    - exp 10: https://github.com/lefteriskomvopoulos/PixelsToPredictions/blob/main/lora-final-seed42.zip

## Comments of missing points from midterm (need to address more in the content of the final report):

- Full Comments: epo provided post-grading. C: production-quality inference (CLI, multi-GPU, SVG healing) but undefined resume_from_checkpoint bug (−1), no README, no requirements.txt (−4). M: dropout missing (−1), rank progression unexplained (−1). A: report prose thin without repo.

- Grading comment: Did not specify all hyperparameters: target modules like q_proj, v_proj, k_proj, dropout etc

- Grading comment: Click here to replace this description. (Placeholder not removed)

- Grading comment: README doesnt have proper reproducable steps (need to add reproducable steps in repo)

- The production-quality inference pipeline with CLI tooling, multi-GPU sharding, and SVG healing demonstrates real-world deployment thinking that goes well beyond the typical course submission. The undefined resume from checkpoint key is a critical bug that would prevent training resumption, and the total absence of documentation (no README, no requirements.txt) significantly diminishes the usability of an otherwise technically strong codebase.
