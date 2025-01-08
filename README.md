# Emotion Detection Using BiLSTM

## Overview
This project implements an emotion detection system using a Bi-directional LSTM (BiLSTM) model. The goal is to classify text into six predefined emotion categories (“joy”, “sadness”, “fear”, “anger”, “surprise”, and “neutral”). The pipeline includes data preprocessing, model training, evaluation, and result visualization.

## Features
- Preprocessing of textual data with cleaning and tokenization.
- Class imbalance handling through upsampling techniques.
- BiLSTM-based model for improved context understanding.
- Hyperparameter tuning for optimized performance.
- Checkpointing and early stopping to prevent overfitting.

## Dataset
The dataset used contains labeled text data for six emotion categories. Preprocessing steps ensured:
- Handling of missing data, slang, and special characters.
- Balanced class distribution.
- Feature extraction including text length, polarity, and subjectivity.

## Preprocessing Steps
1. Cleaned text to remove unwanted characters and stopwords.
2. Handled special cases such as emojis and slang.
3. Tokenized and padded sequences to a uniform length (150 tokens).
4. Encoded emotion labels using one-hot encoding.

## Model
- **BiLSTM Architecture**:
  - Embedding layer initialized with GloVe pre-trained embeddings.
  - Bi-directional LSTM layers for capturing context in both directions.
  - Dense layers with dropout for classification.

## Training
- Early stopping and checkpointing to optimize training time.
- Batch size: 16-32 (adjusted for system limitations).
- Learning rate: 1e-4 with Adam optimizer.
- Trained for up to 50 epochs with early stopping.

## Evaluation Metrics
- Accuracy
- Precision, Recall, F1-Score
- Confusion matrix visualization

## Results
The BiLSTM model achieved:
- Test Accuracy: ~75%
- Consistent performance across all emotion classes.

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your_username/Emotion_Classification_Using_BiLSTM.git
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Download the dataset.

## Future Work
- Experiment with hybrid models combining CNNs and BiLSTMs.
- Extend the dataset to include multi-label emotions.
- Deploy the model using Flask or FastAPI.

## Contributing
Contributions are welcome! Open issues or submit pull requests for suggestions or improvements.

## License
This project is licensed under the MIT License. See the `LICENSE` file for more details.

