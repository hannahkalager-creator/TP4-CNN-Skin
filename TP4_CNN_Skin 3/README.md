# TP4 — CNNs for Skin Lesion Classification (ISIC)

This repository contains the TP4 notebook for the Neural Networks course at ITBA. The notebook includes the course-provided experiment code, saved outputs from my run, and written analysis of the results.

## Contents

- `CNN_en_Skin_Dataset.ipynb`: the executed notebook, including experiment outputs and analysis.
- `requirements.txt`: Python dependencies.
- `data/Split_smol/`: **not included in this repository**. Download the dataset provided for the course and place it locally in this folder, with `train/` and `val/` subfolders and one class folder inside each.

The notebook removes duplicate images, creates a stratified train/validation/test split, and calculates normalization statistics from train only. Keep the split seed fixed. Augmentation is applied only to train, after the split. The test set is reserved for the final evaluation.

## Requirements

Python 3.10 or later is recommended. The notebook runs on CPU; CUDA is optional. The expected runtime is approximately 20–25 minutes on CPU, but it depends on the machine.

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## Run the notebook

From the repository root, make sure `data/Split_smol/train/` and `data/Split_smol/val/` exist locally, then open and run the notebook from top to bottom:

```bash
jupyter notebook CNN_en_Skin_Dataset.ipynb
```

Keep the notebook outputs when saving. The submitted analysis should match the outputs and figures from the run. Do not change the split seed. Document and justify any other changes to the configuration.

## Submission and reproducibility

Do not commit the dataset, checkpoints, or trained model files. Include the executed notebook with its outputs, this README, and `requirements.txt`. The notebook includes an AI-use disclosure; review it and make sure it accurately describes the help used and what you verified or edited yourself.
