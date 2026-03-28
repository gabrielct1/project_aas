# Analysis of Anabolic Steroid–Related Content on YouTube

This repository contains the research pipeline for a large-scale analysis of public YouTube content related to anabolic steroids. The project combines natural language processing (NLP) and visual analysis (computer vision) to characterize said discussion.

## Research Overview

The study uses a multimodal approach to:

- perform automated transcription of videos;
- run multilabel classification of comments;
- apply topic modeling to identify recurring themes;
- produce aggregated demographic characterizations from profile images and video frames.

**Status**: associated manuscript currently under submission/review at **Computers in Human Behavior**.

---

## Methodological Pipeline

The pipeline is organized as Jupyter notebooks in the `notebooks/` folder. Below is a functional summary of each notebook and its purpose.

- `transcription.ipynb`: availability checks, audio extraction, and automatic transcription of videos.
- `data_prep.ipynb`: loading, text normalization and term-based filtering.
- `language_detection.ipynb`: language detection and filtering of videos in Portuguese.
- `data_treatment.ipynb`: cleaning, date handling, missing value treatment, deduplication, and final dataset validation.
- `data_annotation.ipynb`: stratified selection and preparation of samples for manual annotation.
- `Training and Validation MultiLABEL.ipynb`: large-scale training and inference pipeline for multilabel comment classification.
- `summarization.ipynb`: structured summarization of transcriptions.
- `topic_analysis.ipynb`: topic modeling and topic-level distribution analysis.
- `temporal_analysis.ipynb`: temporal analyses of content/users engagement.
- `frame_collection.ipynb`: frame extraction and demographic inference.
- `face_analysis.ipynb`: face detection on profile images and inference of demographic attributes.

---

## Technical Components (high-level)

- Transcription pipelines: audio extraction and speech-to-text processing.
- Language detection: classifiers to filter content by the language of interest.
- Topic modeling and embeddings: text vectorization, dimensionality reduction, and clustering to identify themes.
- Multilabel classification: scalable training, validation and inference pipeline to detect categories in comments.
- Visual analyses: face detection and aggregation of demographic attributes at population level (no individual identification).

Notebook implementations rely on common Python libraries for NLP, CV and ML; dependencies and experimental parameters are documented within each notebook.

## Model and Data Availability

- Trained models and checkpoints are not included in the repository by default for privacy and size reasons.
- Essential artifacts (for example, video identifiers) are available in `video_ids/video_ids.csv` to enable reproducibility through recollection of public metadata.

---

## Data availability

Raw datasets are not publicly available due to YouTube API policies and privacy constraints. A curated list of YouTube video identifiers (video IDs) is provided in the `video_ids/` folder to enable reproducibility via the official YouTube Data API.

## Model availability

The fine-tuned Llama 3.1 8B model for identifying self-reports and symptom/side-effect discussions in Portuguese-language comments is available at [HuggingFace](https://huggingface.co/gabrielct1/llama-aas-related-classification).

## Ethics statement

This study relies exclusively on publicly available data collected through the YouTube Data API in accordance with the platform’s terms of service. No attempts were made to identify individual users.

---

## Contact

For questions or feedbacks, please contact:

Gabriel da Cunha Torres  
gabriel.ct@aluno.ufop.edu.br

---

_Research initiative at the Federal University of Ouro Preto (UFOP)._