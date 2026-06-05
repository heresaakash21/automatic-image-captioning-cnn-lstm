AUTOMATIC IMAGE CAPTIONING USING CNN-LSTM ARCHITECTURE

Project Overview

This project implements an end-to-end Image Captioning system capable of automatically generating natural language descriptions for images. The system combines Computer Vision and Natural Language Processing techniques by using a pre-trained InceptionV3 convolutional neural network for image feature extraction and a Long Short-Term Memory (LSTM) network for caption generation.

The objective of the project is to bridge the gap between visual understanding and language generation by enabling machines to describe image content in human-readable sentences.

Dataset

The project uses the Flickr8k Dataset, a widely used benchmark dataset for image captioning tasks.

Dataset Details:

* Total Images: 8,091
* Total Captions: 40,455
* Captions per Image: 5
* Dataset Size: Approximately 1 GB

Each image is associated with five human-written captions that describe the scene, objects, actions, and context present in the image.

Methodology

1. Caption Preprocessing

   * Captions are converted to lowercase.
   * Punctuation is removed.
   * Start and end sequence tokens are added.
   * Tokenization is performed to convert words into numerical sequences.

2. Image Feature Extraction

   * A pre-trained InceptionV3 model is used as the encoder.
   * The final classification layer is removed.
   * A 2048-dimensional feature vector is extracted for every image.

3. Caption Generation

   * Image features are combined with textual sequences.
   * An LSTM-based decoder predicts one word at a time.
   * Captions are generated sequentially until an end token is produced.

4. Evaluation

   * Generated captions are compared against human-written captions.
   * BLEU metrics are used to evaluate caption quality.

Model Architecture

Encoder:

* InceptionV3 (Pre-trained on ImageNet)
* Feature Vector Size: 2048

Decoder:

* Embedding Layer
* Dropout Layers
* LSTM Layer
* Dense Layers
* Softmax Output Layer

Workflow

Input Image
↓
InceptionV3 Feature Extraction
↓
2048-Dimensional Feature Vector
↓
LSTM Decoder
↓
Generated Caption

Technologies Used

* Python
* TensorFlow
* Keras
* InceptionV3
* LSTM Networks
* NumPy
* Matplotlib
* NLTK
* Kaggle Notebooks

Evaluation Metrics

BLEU (Bilingual Evaluation Understudy) metrics were used to evaluate generated captions against reference captions.

Sample Results:

* BLEU-1: 0.38
* BLEU-4: 0.11

Sample Prediction

Input Image: Dog running through a grassy field

Generated Caption:
"brown dog is running through the grass"

The model successfully identifies primary objects, scene context, and actions occurring within the image.

Project Highlights

* End-to-end Image Captioning Pipeline
* CNN-LSTM Deep Learning Architecture
* InceptionV3-based Feature Extraction
* Caption Tokenization and Sequence Modeling
* BLEU Score Evaluation
* Qualitative and Quantitative Analysis
* Real-world Image Understanding and Language Generation

Future Improvements

* Incorporate Attention Mechanisms
* Implement Transformer-based Decoders
* Use Beam Search for Improved Caption Generation
* Train on Larger Datasets such as MS COCO
* Deploy as a Web Application using Flask or Streamlit
* Improve Caption Diversity and Semantic Accuracy

Author

Aakash Yericharla

Repository

GitHub Repository:
https://github.com/heresaakash21/automatic-image-captioning-cnn-lstm
