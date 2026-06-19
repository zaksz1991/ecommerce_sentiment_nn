# Neural Network Sentiment Analysis – E-Commerce Review Classification

## Overview

This project builds a deep learning sentiment classifier using TensorFlow and Keras. Customer reviews are converted into numerical representations using TextVectorization and classified as Positive or Negative using an embedding-based neural network.

## Dataset

TensorFlow IMDb Dataset

- Positive Reviews = 1
- Negative Reviews = 0
- Vocabulary Size = 10,000

## Model Architecture

1. TextVectorization
2. Embedding Layer (16 dimensions)
3. GlobalAveragePooling1D
4. Dense Layer (16 ReLU units)
5. Sigmoid Output Layer

## Results

Test Accuracy: XX%

Example Review:

"The product arrived broken and I am very unhappy"

Predicted Score: XX

Classification: Negative

## Threshold Recommendation

- <0.20 = Urgent Negative
- 0.20–0.50 = Review Required
- >0.50 = Positive

## Discovery-to-Action Framework

### Discovery

- Data inspection
- Text preprocessing
- Vocabulary generation

### Technical

- TextVectorization
- Embedding Neural Network
- Model training and evaluation

### Action

- Automated routing of negative reviews
- Support ticket creation
- Customer experience monitoring

## Limitations

- Sarcasm detection
- Long-context reviews
- Rare vocabulary
- Domain-specific terminology

## Future Improvements

- LSTM architecture
- Transformer models
- Larger datasets
- Real-time deployment