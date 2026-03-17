# Project AAS — Analysis of Anabolic Steroids Content

This repository contains notebooks and tools for collecting, preprocessing, and analyzing YouTube content about anabolic steroid use. Notebooks cover transcription, summarization, topic modeling, face analysis, and model training (multi-label classification).

Contents

- Notebooks:
  - `data_prep.ipynb` — data preparation
  - `characterization.ipynb` — dataset characterization
  - `transcription.ipynb` — audio transcription
  - `summarization.ipynb` — transcript summarization (uses OpenAI) — prompt preserved
  - `language_detection.ipynb` — language detection
  - `frame_collection.ipynb` — frame extraction and face processing
  - `face_analysis.ipynb` — face embeddings and clustering
  - `topic_analysis.ipynb` — topic modeling (BERTopic) and demographic profiling
  - `temporal_analysis.ipynb` — temporal exploratory analysis
  - `data_treatment.ipynb` — cleaning scripts
  - `data_annotation.ipynb` — annotation utilities
  - `Training and Validation MultiLABEL.ipynb` — multi-label training with LoRA + 4-bit quant

How to run

1. Create a Python environment and install requirements (examples):

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Requirements (high level)

- Python 3.10+
- numpy, pandas, torch, transformers, sentence-transformers, bertopic, umap-learn, hdbscan, scikit-learn, bitsandbytes, peft, tqdm, nltk, spacy, matplotlib, seaborn

Dataset

- Due to data sharing restrictions, this repository does not include the original videos or full datasets. The only dataset file provided in this repo is a list of video IDs (`video_ids/video_ids.csv`). With these IDs you can re-download the videos and metadata to reproduce analyses locally.
