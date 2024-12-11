# BookRecommender
Book Recommender: Find the Book that Fits You

## Author
Developed by Sunwoo Baek, Hangoo Kang, Supia Park, Esther Hwang

---


## Introduction
This project processes tweets and book datasets to:
- Impute missing categories for books using zero-shot classification.
- Preprocess tweet content by removing links, mentions, and emojis.
- Classify user tweets into predefined book categories.
- Recommend books to users based on tweet analysis.

The script uses `tweepy`, `transformers`, and `scikit-learn`, among other libraries. It leverages Kaggle datasets and provides outputs in CSV files.

---

## Requirements
### Tools and Libraries
- Python 3.8+
- Kaggle API configured with your account
- Libraries: `tweepy`, `torch`, `transformers`, `kagglehub`, `sklearn`, `pandas`, `csv`, `os`, `re`

---

## Setup Instructions

### 1. Install Python and Required Libraries
Ensure Python is installed on your machine. Install the necessary libraries by running:
```bash
pip install tweepy torch transformers kagglehub scikit-learn pandas
```

### 2. Download the Dataset from Kaggle or from Zip.file
This script requires tweet and book datasets from Kaggle. You must have Kaggle CLI configured on your system. 
Or, you can directly load datasets included in the Zip.file.

**Steps to Download the Dataset:**
1. Install Kaggle CLI:
   ```bash
   pip install kaggle
   ```
2. Download the datasets by running the following in the terminal:
   ```bash
   kaggle datasets download mmmarchetti/tweets-dataset
   ```
   The dataset will be downloaded as a ZIP file.

3. Extract the ZIP file:
   ```bash
   unzip tweets-dataset.zip -d tweets_dataset
   ```
or

1. Load `books.csv` and `tweets.csv` from the Zip.file.

---

## How to Run

### Step 1: Setup Environment
Ensure all required libraries are installed and datasets are unzipped and placed in the correct directories.

### Step 2: Execute the Script
Run the script using Python:
```bash
python analysis_script.py
```

### Step 3: Outputs
1. **Books with Imputed Categories:**
   - Saved as `books_with_imputed_categories.csv`.
   - Contains missing book categories imputed using zero-shot classification.

2. **Preprocessed Tweets:**
   - Saved as `tweets_with_imputed_categories.csv`.
   - Contains tweets with links, mentions, and emojis removed.

3. **User Classification and Recommendations:**
   - Saved as `author_classification_results.csv`.
   - Contains the predicted top category for each author and the top 5 recommended books.

---

## File Structure
```plaintext
project/
├── books.csv                         # Dataset with book information
├── tweets.csv                        # Dataset with Tweets
├── books_with_imputed_categories.csv # Output with imputed book categories
├── tweets_with_imputed_categories.csv# Preprocessed tweet data
├── author_classification_results.csv # User classification results
├── CS410_Project_BookRecommender.ipynb           # Main Project Jupyter Notebook
```

---

## Notes
- For failed classifications or missing data, a fallback category (e.g., `Fiction`) is used.
- Use the Kaggle API token in your system to download datasets programmatically or use datasets that are included in the zip file.

---

## Troubleshooting
1. **Missing Datasets:**
   - Ensure the datasets are downloaded and unzipped in the correct directory.
2. **Dependency Errors:**
   - Check Python version and installed libraries.

---

## License
This project is for educational purposes only. Use of datasets and models must comply with their respective licenses.

---

