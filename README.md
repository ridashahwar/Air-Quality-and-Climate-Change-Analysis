# Air Quality and Climate Change Analysis Pipelines

This repository contains two robust data pipelines designed for distinct datasets and purposes:

1. **Structured Data Pipeline**: Processes air quality data for predictive modeling.
2. **Unstructured Data Pipeline**: Analyzes Reddit discussions related to climate change using natural language processing (NLP).

---

## Project Overview

### Structured Data Pipeline
This pipeline prepares structured air quality data from OpenAQ for machine learning applications, focusing on predictive modeling of pollutant levels. Key features include:

- **Data Source**: OpenAQ air quality dataset.
- **Objectives**:
  - Ensure data integrity through cleaning and transformation.
  - Engineer meaningful features for model training.

### Unstructured Data Pipeline
This pipeline processes unstructured text data from Reddit discussions to perform sentiment analysis and topic modeling, offering insights into public discourse on climate change.

- **Data Source**: Reddit comments from climate-related subreddits.
- **Objectives**:
  - Extract and normalize text data.
  - Identify sentiment and key discussion topics.

---

## Pipeline Details

### 1. Structured Data Pipeline

#### Steps:
1. **Data Ingestion**
   - Load raw data and inspect for missing values, distributions, and potential quality issues.
   - Key columns: `location`, `parameter` (pollutant type), `value`, and `datetime`.

2. **Data Cleaning and Transformation**
   - Handle missing values and normalize datetime fields.
   - Encode categorical features like `location` and `parameter`.

3. **Feature Engineering**
   - Aggregate daily pollutant levels.
   - Add statistical (e.g., mean, standard deviation) and temporal features (e.g., day-of-week).

4. **Data Splitting**
   - Split into training and testing sets (80/20 split).

5. **Model Evaluation Preparation**
   - Incorporate metrics like R² score and Mean Squared Error.
   - Enable cross-validation for robust model performance.

#### Results:
- Enhanced dataset integrity with added predictive features.
- Initial modeling demonstrates strong performance with significant R² scores.

### 2. Unstructured Data Pipeline

#### Steps:
1. **Data Ingestion and Exploration**
   - Load Reddit comments into a DataFrame and inspect shape and quality.
   - Key columns: `self_text`, `subreddit`, `author_name`, `created_time`, and `score`.

2. **Data Cleaning and Transformation**
   - Normalize text: convert to lowercase, remove punctuation, tokenize, and lemmatize.
   - Remove stop words and irrelevant data.

3. **Feature Engineering**
   - Perform sentiment analysis using the VADER analyzer.
   - Generate n-grams and perform topic modeling with Latent Dirichlet Allocation (LDA).

4. **Data Splitting**
   - Split into training and testing sets (80/20 split).

5. **Model Evaluation**
   - Train logistic regression for sentiment classification.
   - Evaluate with metrics like accuracy, precision, recall, and F1-score.

#### Results:
- **Sentiment Analysis**:
  - Sentiment distribution: 65% neutral, 25% positive, 10% negative.
- **Topic Modeling**:
  - Identified key themes: climate policy, energy alternatives, public skepticism.
- **Model Performance**:
  - Achieved 99% accuracy with high precision and recall.
