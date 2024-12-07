# Image Captioning with DarkNetLM and DarkNetVG2

## Table of Contents
- [Image Captioning with DarkNetLM and DarkNetVG2](#image-captioning-with-darknetlm-and-darknetvg2)
  - [Table of Contents](#table-of-contents)
  - [Overview](#overview)
  - [Models](#models)
    - [DarkNetLM](#darknetlm)
    - [DarkNetVG2](#darknetvg2)
  - [Installation](#installation)
  - [Usage](#usage)
    - [DarkNetLM](#darknetlm-1)
    - [DarkNetVG2](#darknetvg2-1)
  - [Results](#results)
  - [Contributing](#contributing)
  - [License](#license)
  - [Acknowledgments](#acknowledgments)
- [Data Lake for Image Captioning model](#data-lake-for-image-captioning-model)
- [Mobile Application](#mobile-application)


## Overview

This project focuses on image captioning, utilizing two primary models: **DarkNetLM** and **DarkNetVG2**. Both models leverage the CSP DarkNet53 architecture as the backbone of YOLOv8 for feature extraction from images, but they differ in their approaches to generating captions.

## Models

### DarkNetLM

- **Architecture**: DarkNetLM employs the CSP DarkNet53 architecture within YOLOv8 for image feature extraction.
- **Components**:
  - **Bert-Tokenizer**: Utilized for tokenizing input text, allowing the model to understand and process natural language effectively.
  - **LSTM**: Long Short-Term Memory networks are used to generate sequential captions based on the extracted image features.

### DarkNetVG2

- **Architecture**: Similar to DarkNetLM, DarkNetVG2 also uses the CSP DarkNet53 architecture in YOLOv8 for image feature extraction.
- **Components**:
  - **GPT-2**: This model employs the GPT-2 architecture for generating captions, leveraging its powerful language generation capabilities to produce coherent and contextually relevant descriptions.

## Installation

To set up the project, clone the repository and install the required dependencies:
```
git clone https://github.com/yourusername/Image-Captioning.git
cd Image-Captioning
pip install -r requirements.txt
```

## Usage

To run the models, use the following commands:

### DarkNetLM
```
python Test_model/test-model-bert-lstm-8ep.ipynb
```

### DarkNetVG2
```
python Test_model/test-model-gpt2-8ep.ipynb --> update continue...
```

## Results

The models are evaluated based on their ability to generate accurate and descriptive captions for a variety of images. Performance metrics and sample outputs will be provided in the results section of the documentation.

## Contributing

Contributions are welcome! Please submit a pull request or open an issue for any suggestions or improvements.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

## Acknowledgments

- YOLOv8 for its powerful object detection capabilities.
- The creators of the CSP DarkNet53 architecture.
- The developers of BERT and GPT-2 for their contributions to natural language processing.

## Data Lake for Image Captioning model
This system involved the development and implementation of a Data Lake architecture to support an AI model capable of generating image captions. The architecture was designed to efficiently ingest, process, and centralized store large volumes of image and text data. View more details at this [repo](https://github.com/Narius2030/DataLake-Solution-IMCP.git)

![image](https://github.com/user-attachments/assets/1f37671e-7be2-45cc-8a6b-ee926171ead8)

## Mobile Application
This mobile application uses the camera to capture images and sends them to a microservice for image captioning. Powered by a machine learning model, the app generates descriptive captions for each photo, providing visually impaired users with a detailed understanding of their surroundings through auditory feedback. View more detailes at this [repo](https://github.com/Narius2030/IMCP-Mobile-App.git)

