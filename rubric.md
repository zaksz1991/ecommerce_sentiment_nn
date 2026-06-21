# Rubric Template – Neural Network Sentiment Analysis

## 1. Data Preparation (20%)
- Loaded dataset successfully
- Cleaned missing values
- Converted labels into binary format (0/1)
- Split dataset into training and testing sets

## 2. Text Processing (20%)
- Applied TextVectorization
- Standardized text input
- Set vocabulary size to 10,000
- Fixed sequence length to 200

## 3. Model Architecture (20%)
- Embedding layer (32 dimensions)
- GlobalAveragePooling1D
- Dense layer (16 units, ReLU)
- Output layer (sigmoid)

## 4. Training Performance (15%)
- Model trained for 5 epochs
- Validation accuracy monitored
- No major overfitting observed

## 5. Evaluation (15%)
- Model evaluated on test set
- Accuracy reported successfully

## 6. Action Phase (10%)
- Confidence score generated
- Prediction used for sentiment classification
- Business rule applied for decision-making