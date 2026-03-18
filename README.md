# Project AAS — Analysis of Anabolic Steroids Content

This repository contains a comprehensive pipeline for collecting, preprocessing, and analyzing YouTube content related to anabolic steroid use. The project uses Natural Language Processing (NLP) and Computer Vision (CV) to characterize the discourse and demographics of the community.

## Pipeline Overview

The analysis is divided into several stages, each handled by specific notebooks:

### 1. Data Collection & Preparation
- `data_prep.ipynb`: Initial data loading, keyword filtering, and basic statistics.
- `transcription.ipynb`: Automates audio download (yt-dlp) and transcription using OpenAI's Whisper model.
- `language_detection.ipynb`: Filters content to ensure only Portuguese-language videos are analyzed (using XLM-RoBERTa).
- `data_treatment.ipynb`: Data cleaning, deduplication, and validation of the comments dataset.

### 2. Content Analysis
- `summarization.ipynb`: Uses GPT models to extract structured information from video transcripts (topics, substances, side effects).
- `topic_analysis.ipynb`: Performs topic modeling using BERTopic and analyzes the prevalence of different themes.
- `characterization.ipynb`: Exploratory Data Analysis (EDA) of user behavior and term frequency (TF-IDF) analysis.
- `temporal_analysis.ipynb`: Analyzes the evolution of content and engagement over time.

### 3. Demographic & Visual Analysis
- `frame_collection.ipynb`: Extracts frames from videos and detects faces and its corresponding attributes
- `face_analysis.ipynb`: Estimates age and gender of content creators and users to build demographic profiles.

### 4. Machine Learning & Modeling
- `data_annotation.ipynb`: Utilities for sampling and preparing data for manual annotation.
- `Training and Validation MultiLABEL.ipynb`: Trains a multi-label classification model (e.g., LLaMA 3.1) using LoRA and 4-bit quantization for high-efficiency fine-tuning.

## How to run

1. Create a Python environment and install requirements:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

2. **Requirements**: Python 3.10+, PyTorch, Transformers, BERTopic, DeepFace, InsightFace, and other standard data science libraries (see `requirements.txt`).

## Dataset

Due to privacy and data sharing restrictions, this repository does not include the original video files or the full processed datasets. The provided `video_ids/video_ids.csv` contains the YouTube IDs used in this study, which can be used to re-collect the data and reproduce the results.

---
*This project is part of a research initiative at UFOP.*
