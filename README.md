# Vietnamese Image Captioning with Attention Mechanism

## Overview

This project involves developing an image captioning model that generates descriptive captions for images using Vietnamese text. This is a EncoderDecoder model utilizes a combination of Convolutional Neural Networks (CNN) and Long Short-Term Memory (LSTM) networks with an Bahdanau attention mechanism. The project is built using PyTorch and leverages pre-trained ResNet-50 for feature extraction.

## Project Components

1. **Data Preparation**:
   - **Dataset**: The project uses the Flickr 8k dataset with Vietnamese translation of images and corresponding Vietnamese captions. Captions are stored in a CSV file.
   - **Vocabulary Building**: A custom vocabulary is built from the dataset to map words to indices.
   - **DataLoader**: A PyTorch `DataLoader` is used to efficiently handle and preprocess the dataset.

2. **Model Architecture**:
   - **EncoderCNN**: Uses ResNet-50 to extract feature maps from images.
   - **Attention Mechanism**: Implements Bahdanau attention to focus on relevant parts of the image while generating captions.
   - **DecoderRNN**: An LSTM-based decoder generates captions based on the image features and attention context.
   - **EncoderDecoder**: Combines the encoder and decoder into a single model for training and inference.

3. **Training**:
   - The model is trained using cross-entropy loss and the Adam optimizer.
   - Training involves saving the model’s state periodically for later use.

4. **Inference**:
   - The model generates captions for new images and visualizes the attention weights to understand which parts of the image are being focused on.

5. **Visualization**:
   - Attention maps are visualized to show the regions of the image that influence the generated captions.


