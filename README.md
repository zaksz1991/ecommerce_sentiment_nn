# Neural Network Sentiment Analysis – E-Commerce Review Classification

## Project Overview

This project applies Natural Language Processing and Deep Learning techniques to classify customer reviews as Positive or Negative using TensorFlow and Keras.

The solution follows the Discovery-to-Action (DTA) framework to transform customer feedback into actionable business insights.

## Discovery Phase

### Data Preparation

* Loaded a sentiment review dataset
* Explored review and label distributions
* Checked for missing values
* Converted sentiment labels into binary classes
* Prepared text data for vectorization

### Text Standardization Strategy

* Lowercasing handled by TextVectorization
* Vocabulary limited to 10,000 words
* Reviews converted into integer sequences
* Sequence length fixed at 200 tokens

## Technical Phase

### Text Vectorization

Keras TextVectorization was used to:

* Build a vocabulary from training data
* Convert text into numerical sequences
* Standardize inputs for neural network training

### Neural Network Architecture

Model Architecture:

1. Embedding Layer (32 dimensions)
2. GlobalAveragePooling1D
3. Dense Hidden Layer (16 neurons, ReLU)
4. Output Layer (1 neuron, Sigmoid)

### Compilation

* Optimizer: Adam
* Loss Function: Binary Crossentropy
* Metric: Binary Accuracy

### Training

The model was trained for 5 epochs while monitoring validation accuracy to evaluate generalization performance and detect overfitting.

## Evaluation Results

The trained model achieved strong validation performance and successfully classified positive and negative review sentiment.

### Test Review

Input:

"The product arrived broken and I am very unhappy"

Output:

Negative Sentiment

The confidence score was low, indicating a negative customer experience.

## Action Phase

### Confidence-Based Review Routing

| Confidence Score | Action                                         |
| ---------------- | ---------------------------------------------- |
| < 0.20           | Automatically flag for urgent customer support |
| 0.20 – 0.50      | Send for manual review                         |
| > 0.50           | No intervention required                       |

### Business Workflow

1. Customer submits review.
2. Model predicts sentiment.
3. Confidence score is generated.
4. Negative reviews below threshold are routed automatically to customer support.
5. Support team receives alert and contacts customer.
6. Positive reviews remain in standard feedback storage.

## Reliability Considerations

Confidence scores help automate decision-making but should not be treated as absolute certainty.

Human review remains valuable for:

* Ambiguous reviews
* Mixed sentiment
* Domain-specific terminology
* Edge cases

## Limitations

* Sarcasm is difficult to detect.
* Long contextual relationships may be missed.
* Unknown vocabulary can reduce accuracy.
* Predictions depend on training data quality.

## Future Improvements

* LSTM-based architectures
* Bidirectional LSTM
* Transformer models
* BERT fine-tuning
* Real-time API deployment
* Continuous model retraining

## Conclusion

The project successfully demonstrates how neural networks can classify customer sentiment and support automated customer-service workflows using confidence-driven business rules.
