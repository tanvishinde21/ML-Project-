📌 Sentiment Analysis on Zepto Reviews
This project performs sentiment analysis on customer reviews from Zepto using traditional machine learning models. The aim is to classify reviews into positive, neutral, or negative sentiments using text classification techniques.

🧾 Dataset
Input: Customer reviews and corresponding rating scores (1–5).

Target: Sentiment label mapped from score:

1–2 → Negative

3 → Neutral

4–5 → Positive

🔍 Preprocessing & EDA
Removed null entries

Cleaned the review text (lowercasing, removing special characters, links, extra spaces)

Created sentiment labels from review scores

WordClouds generated for each sentiment class

Visualized class distribution (before and after SMOTE)

⚙️ Feature Engineering
Used TF-IDF Vectorizer with 1000 max features

Encoded target labels using LabelEncoder

⚖️ Handling Class Imbalance
Applied SMOTE (Synthetic Minority Over-sampling Technique) on the training data

Balanced each class (positive, neutral, negative) to equal sample sizes

🤖 Models Trained
Four classifiers were trained and evaluated:

Model	Accuracy
✅ Random Forest	86.18% ,
Logistic Regression	84.93% ,
SVM (LinearSVC)	84.75% ,
Naive Bayes	81.95%

Best model: Random Forest (n_estimators=50, max_depth=15)

Metrics: Precision, Recall, F1-score, Confusion Matrix for all models

📈 Results Snapshot
Accuracy on test set: ~86%

Sentiment distribution handled effectively with SMOTE

Random Forest provided the best balance between performance and speed

Saved prediction results to CSV and exported model metrics

💾 Inference & Deployment
Trained model saved as random_forest_model.pkl

Vectorizer saved with TF-IDF features

Sample function: predict_sentiment(text, vectorizer, model) for custom review prediction


