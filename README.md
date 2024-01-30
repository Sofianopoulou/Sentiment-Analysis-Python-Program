# Sentiment Analysis Python Program

This Python program performs sentiment analysis on movie reviews using the `polarity_dataset_v2.0`. The dataset consists of text files categorized as either positive or negative reviews. The sentiment analysis is carried out using a text classification approach, specifically with Multinomial Naive Bayes and Bernoulli Naive Bayes classifiers.

## Setup

### Dependencies
- Python
- NLTK (Natural Language Toolkit)
- Scikit-learn

### Installation
1. Ensure you have Python installed.
2. Install the required dependencies using the following commands:
    ```bash
    pip install nltk scikit-learn
    ```
3. Download NLTK resources (uncomment these lines of code):
    ```python
    import nltk
    nltk.download('punkt')
    nltk.download('stopwords')
    nltk.download('wordnet')
    ```

## Usage

1. **Download Dataset:**
   The program assumes that the `review_polarity.tar.gz` file is located in the project folder. If not, provide the correct file path in the `tar_gz_file_path` variable.

2. **Run the Program:**
   Execute the program by running the Python script. It will extract the dataset and prompt you to choose a classifier:
   - Enter `1` for Multinomial Naive Bayes
   - Enter `2` for Bernoulli Naive Bayes
   - Enter `exit` to end the program.

3. **View Results:**
   The program will display results for the chosen classifier, including accuracy, precision, recall, and a confusion matrix.

## Preprocessing

The program employs a preprocessing pipeline that includes:
- Text lowercasing
- Tokenization
- Stopword removal
- Lemmatization
- Stemming
- N-gram generation (optional)

These preprocessing steps enhance the quality of the text data for classification.

## Data Loading

The text files are loaded from the `pos` and `neg` folders. The content of each file is preprocessed, and the corresponding labels (positive or negative) are assigned.

## Classification

The program allows you to choose between Multinomial Naive Bayes and Bernoulli Naive Bayes classifiers. It leverages the Scikit-learn library for building the classification pipeline, vectorizing the text data, and evaluating the model using 5-fold cross-validation.

## Acknowledgments

This sentiment analysis program was developed for educational purposes. It uses the NLTK library for natural language processing tasks and Scikit-learn for machine learning. Special thanks to the dataset contributors.

Feel free to contribute or provide feedback to enhance this sentiment analysis tool.