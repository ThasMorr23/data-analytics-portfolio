# Sentiment Analysis of Amazon Product Reviews

##  Overview
This project builds a machine learning model to classify Amazon product reviews as **positive or negative** using natural language processing (NLP) and a neural network implemented in TensorFlow/Keras.

The project demonstrates an end-to-end workflow including data cleaning, text preprocessing, model development, evaluation, and a simulated real-world deployment scenario.

---

##  Objective
Customer reviews contain valuable insights, but analyzing them at scale is challenging. The goal of this project is to develop a model that can automatically classify review sentiment, enabling businesses to monitor customer feedback and make data-driven decisions.

---

##  Tools & Technologies
- Python
- Pandas, NumPy
- TensorFlow / Keras
- Scikit-learn
- Matplotlib

---

##  Dataset
The dataset consists of labeled product reviews, where each review is classified as either positive or negative. Multiple datasets were combined into a single dataset for analysis.

---

##  Methodology

### Data Preparation
- Removed duplicates and missing values  
- Normalized text (lowercasing, removing punctuation and extra spaces)  
- Tokenized text into numerical sequences  
- Applied sequence padding to standardize input length  

### Model Development
- Neural network with:
  - Embedding layer for text representation  
  - Global average pooling  
  - Dense hidden layer with ReLU activation  
  - Batch normalization and dropout for regularization  
  - Sigmoid output for binary classification  

### Training
- Train/test split with stratification  
- Early stopping to prevent overfitting  
- Model evaluated on unseen test data  

---

##  Results
- **Test Accuracy: ~78%**

The model successfully captures sentiment patterns in review text. While slightly lower than earlier experimental results (~81%), this version was selected because it balances performance with a clean, reproducible, and interpretable pipeline suitable for real-world use.

---

##  Simulated Real-World Deployment

To demonstrate how this model would function in production, a simulated pipeline was created:

1. New customer reviews are processed by the model  
2. Each review is classified as positive or negative  
3. Predictions are aggregated to calculate sentiment distribution  
4. Results are visualized to identify trends  

This reflects how companies monitor customer sentiment at scale.

---

##  Business Applications

This model can be used to:

- Monitor customer sentiment in real time  
- Identify trends in product satisfaction  
- Detect spikes in negative feedback  
- Support product, marketing, and customer experience decisions  

---

##  Future Improvements

- Tune hyperparameters to improve accuracy  
- Compare with baseline models (e.g., logistic regression)  
- Implement more advanced architectures (LSTM, GRU, transformers)  
- Expand dataset for better generalization  
- Deploy as an automated pipeline connected to a live data source  

---

## 📁 Project Structure

