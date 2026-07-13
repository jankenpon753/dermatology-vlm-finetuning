# Dermatology VLM: Parameter-Efficient Fine-Tuning for Skin Condition Classification

Machine Learning Sessional course project. Fine-tunes a vision-language model to classify dermatological conditions from images, and wraps it in a small web app for interactive querying.

## Overview

- **Dataset**: [`danielfdias98/derm-reasoning-full-reasoning`](https://huggingface.co/datasets/danielfdias98/derm-reasoning-full-reasoning) (Hugging Face) — 5,086 images across 25 skin condition classes (e.g. psoriasis, eczema, basal cell carcinoma, warts), split 80/10/10 train/val/test.
- **Approach**: Parameter-efficient fine-tuning (PEFT) of a multimodal model for classification, with an ablation/evaluation pipeline (loss curves, confusion matrix, per-class scores) documented in the report.
- **Demo app**: `VLM_app/` — a FastAPI web app (see its own README) that lets a user upload a medical image and ask natural-language questions about it, using a vision-capable LLM (Groq).

## Structure

```
.
├── ML_Project.pdf     # Dataset/spec handout
├── report/            # LaTeX report: methodology, results, figures
│   ├── report.tex / text.tex / ml_cover.tex
│   ├── report.pdf
│   └── assets/images/output/   # Loss curves, confusion matrix, class distribution, etc.
└── VLM_app/            # Standalone demo web app (own git history + README)
```

## Results

See `report/report.pdf` for the full write-up, including the confusion matrix, per-class F1 scores, and training curves.

## Demo App

`VLM_app` already has its own git history and README — it's kept as a nested project folder here since it was built as part of this same course project, but functions as a standalone app. See `VLM_app/README.md` for setup and usage.

## Author

Md. Tajim An Noor — Dept. of Electrical & Computer Engineering, RUET
