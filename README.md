# 🚦 Vietnamese Traffic Image Captioning Dataset & System

## 📑 Table of Contents
- [🚦 Vietnamese Traffic Image Captioning Dataset \& System](#-vietnamese-traffic-image-captioning-dataset--system)
  - [📑 Table of Contents](#-table-of-contents)
  - [📝 Overview](#-overview)
  - [📁 Folder Structure](#-folder-structure)
  - [🔗 Pipeline](#-pipeline)
  - [🤖 Models](#-models)
  - [🚀 Usage](#-usage)
    - [1. Environment Setup](#1-environment-setup)
    - [2. Run the Pipeline Steps](#2-run-the-pipeline-steps)
  - [📊 Results](#-results)
  - [🤝 Contributing](#-contributing)
  - [🪪 License](#-license)
  - [🙏 Acknowledgments](#-acknowledgments)
  - [💁‍♂️ Author](#️-author)

## 📝 Overview

This project provides a full pipeline for building a Vietnamese traffic image captioning dataset and system, supporting both computer vision research and accessibility for the visually impaired. The pipeline includes data crawling, cleaning, caption generation, and image augmentation.

## 📁 Folder Structure

```
IMCP-Support-Blinders/
├── README.md
├── Data/
│   ├── dashboard.dio
│   ├── image.png
│   ├── README_en.md
│   ├── README_vn.md
│   ├── README.md
│   ├── 1.crawl_data/
│   │   ├── env_crawl_data.yaml
│   │   ├── output/
│   │   │   ├── metadata.json
│   │   │   ├── traffic_images_dataset_v1.csv
│   │   │   ├── traffic_images_dataset_v2.csv
│   │   │   └── traffic_images_dataset_v3.csv
│   │   └── python/
│   │       └── traffic_raw.py
│   ├── 2.data_preprocessing/
│   │   ├── jupyter/
│   │   │   └── data_preprocessing.ipynb
│   │   └── output/
│   ├── 3.labels_short_captions/
│   │   ├── output/
│   │   │   └── csv_with_captions/
│   │   └── python/
│   └── 4.Image_data_augument/
│       ├── output/
│       └── python/
├── Model/
│   ├── DarkNetLM/
│   └── DarkNetVG2/
```

- **Data/**: Main pipeline and dataset scripts, including crawling, preprocessing, captioning, and augmentation.<br>
  👉 For more details, see the [Germini-Captioning-Dataset-2025 repo](https://github.com/TrieuPhi/Germini-Captioning-Dataset-2025)
- **Model/**: Model code and experiments (details to be updated).

## 🔗 Pipeline

1. **Crawl Data**  
   Collect traffic images from Google Images via SerpApi, save metadata and images locally.

2. **Data Preprocessing**  
   Clean data: remove broken URLs, handle nulls, standardize fields.

3. **Labels Short Captions**  
   Use Gemini 2.0 Flash API to generate concise (10-15 words) captions for each image.

4. **Image Augmentation**  
   Augment data using modern image transformation techniques with [Albumentations](https://albumentations.ai/).

## 🤖 Models

**To be updated.**

## 🚀 Usage

### 1. Environment Setup

```bash
cd Data/1.crawl_data/
conda env create -f env_crawl_data.yaml
conda activate crawl_data
pip install -r ../3.labels_short_captions/python/requirements.txt
pip install -r ../4.Image_data_augument/python/requirements.txt
```

### 2. Run the Pipeline Steps

**Step 1: Crawl data**
```bash
python 1.crawl_data/python/traffic_raw.py
```

**Step 2: Data cleaning**
- Use the notebook or script in `2.data_preprocessing/jupyter/`

**Step 3: Caption generation**
```bash
python 3.labels_short_captions/python/label_short_captions.py
```

**Step 4: Augmentation**
```bash
python 4.Image_data_augument/python/data_augument.py
```

## 📊 Results

- Augmented images and captions are stored in `Data/4.Image_data_augument/output/` and `augmented/`.
- Cleaned CSVs and intermediate results are in the corresponding `output/` folders.

## 🤝 Contributing

Contributions are welcome! Please submit a pull request or open an issue for any suggestions or improvements.

## 🪪 License

This project is licensed under the MIT License. See the LICENSE file for more details.

## 🙏 Acknowledgments

- BERT, GPT-2, and Albumentations authors.
  
## 💁‍♂️ Author

- [Narius2030](https://github.com/Narius2030) 🦉
- [HTN-DT-Beo](https://github.com/HTN-DT-Beo) 🐻
- [TrieuPhi](https://github.com/TrieuPhi) 🚀
