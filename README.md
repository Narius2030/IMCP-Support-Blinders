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
