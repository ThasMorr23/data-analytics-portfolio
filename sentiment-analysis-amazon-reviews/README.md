# Amazon Review Sentiment Analysis (RNN)

## Overview
This project uses natural language processing (NLP) and a recurrent neural network (RNN) to classify Amazon product reviews as positive or negative. The goal was to determine whether customer sentiment can be accurately predicted from review text.

---

## Objective
- Classify customer reviews as positive or negative  
- Build and train a neural network model for text classification  
- Evaluate model performance on unseen data  

---

## Tools & Technologies
- Python  
- TensorFlow / Keras  
- Pandas, NumPy  
- scikit-learn  

---

## Dataset

The dataset consists of Amazon product reviews labeled as:

- **1 = Positive sentiment**  
- **0 = Negative sentiment**  

Example:
  "Great product!" → 1
  "Waste of money." → 0


The model was trained on **2,731 labeled reviews**. :contentReference[oaicite:1]{index=1}  

---

## Data Preparation

- Removed special characters and noise  
- Removed stop words  
- Tokenized text into sequences  
- Converted words into numerical representations  
- Applied padding to standardize input length  
- Split data into training (80%) and testing (20%) sets  

---

## Model Architecture

The neural network includes:

- Embedding layer (text representation)  
- MaxPooling layer  
- Dense layers  
- Dropout layer (to reduce overfitting)  
- Sigmoid output layer for binary classification  

Total parameters: ~1.6 million :contentReference[oaicite:2]{index=2}  

---

## Model Performance

- **Training Accuracy:** 99.86%  
- **Test Accuracy:** 81.72%  
- **Loss (test):** 0.5324  

:contentReference[oaicite:3]{index=3}  

---

## Key Insights

- The model successfully learns patterns in customer sentiment  
- Strong training accuracy indicates effective learning  
- Lower test accuracy suggests some overfitting  
- The model generalizes reasonably well to new data  

---

## Business Relevance

Sentiment analysis can help organizations:

- Understand customer satisfaction at scale  
- Identify negative feedback trends quickly  
- Improve products based on user sentiment  
- Enhance customer experience  

---

## Limitations

- Model shows signs of overfitting (train vs test gap)  
- Dataset size is relatively small  
- Limited vocabulary may restrict performance  

:contentReference[oaicite:4]{index=4}  

---

## Future Improvements

- Increase dataset size for better generalization  
- Tune hyperparameters (epochs, dropout, layers)  
- Explore advanced models (LSTM, transformers)  
- Improve text preprocessing and feature engineering  

---

## Project Files

- `sentiment-analysis.ipynb` → Full code and modeling workflow  
- `project-summary.docx` → Detailed written analysis  
- `data/` → Raw and prepared datasets  
- `images/` → Training and evaluation visuals  

---

Notebook

The full analysis is available in:

- `sentiment-analysis.ipynb`

This notebook includes:
- Data preprocessing and cleaning  
- Tokenization and sequence preparation  
- Neural network model construction  
- Training and evaluation  

The project is fully reproducible using the provided dataset.

---

## Key Takeaway

This project demonstrates how deep learning and NLP techniques can be used to extract meaningful insights from unstructured text data, enabling scalable analysis of customer sentiment.
