# DL Kaggle Final Project (ScienceQA VLM)

This repository contains our experiments for fine-tuning and evaluating `HuggingFaceTB/SmolVLM-500M-Instruct` on the course Kaggle multimodal science QA competition.

Competition link: https://www.kaggle.com/competitions/pixels-to-predictions

## Prerequisites

- Python 3.10+
- Kaggle account and access to the competition data

Install dependencies:

```bash
pip install -r requirements.txt
```

## Dataset Setup (Required)

Download the dataset from the Kaggle competition and place it in this repo with the following structure:

```text
input/competitions/pixels-to-predictions/
  train.csv
  val.csv
  test.csv
  images/
```

After the dataset is in place, you can run the notebooks/scripts.

## Repository Structure

- `working/experiments/`: numbered experiment folders, notebooks, and run notes
- `best-result-repro/`: best main-branch reproducible run assets (script + adapter)
- `report/latex/`: ACL-style final report source

## Reproducing the Best Main-Branch Result

Use files in `best-result-repro/`:

- `baseline-starter-notebook__exp23-left-inspired-trainval__20260505.ipynb`
- `exp23_best_adapter.zip`

Reference score:

- Exp23 public score: `0.70623`

## Reproducing Other Experiments

1. Open a target notebook in `working/experiments/<exp-folder>/`.
2. Run on Kaggle notebook with GPU (T4), unless explicitly inference-only.
3. Ensure dataset paths and optional adapter paths are correctly configured.
4. Export submission from `/kaggle/working/<run_name>/submission.csv`.

## Key Public Submission Scores

- Baseline (v1): `0.65392`
- Exp17: `0.69014`
- Exp20: `0.69818`
- Exp23 (best on this branch): `0.70623`

## Code and Model Links

- Main repo (Che Hung Liao): https://github.com/shanpig/dl-kaggle-final
  - Exp17 adapter: https://www.kaggle.com/models/chehungliao/exp17-best-adapter
  - Exp23 adapter: https://www.kaggle.com/models/chehungliao/exp23-best-adapter
- Teammate repo (Elefterios Komvopoulos): https://github.com/lefteriskomvopoulos/PixelsToPredictions
  - Left branch best LoRA weights (seed42): https://github.com/lefteriskomvopoulos/PixelsToPredictions/blob/main/lora-final-seed42.zip

## Report

ACL-style report source is in:

- `report/latex/acl_latex.tex`

Compile locally (if TeX is installed):

```bash
cd report/latex
pdflatex acl_latex.tex
```

## AI Tooling Disclosure

We used LLM assistants (ChatGPT/Codex-style tools) for coding support, debugging, experiment tracking, and report drafting/editing.
