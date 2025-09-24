IMDb Sentiment Classification

This project performs sentiment analysis on the IMDb Movie Review Dataset. The dataset consists of 50,000 reviews labeled as positive or negative. The task is a binary text classification problem.

📂 Dataset

File: IMDB Dataset.csv

Columns:

review → Movie review text (string)

sentiment → Label (positive / negative)

For faster training, we use a 10,000-sample subset of the dataset in this notebook.

⚙️ Approach

Data Preprocessing

Encoded labels (positive → 1, negative → 0)

Text vectorized using TF-IDF (max 5000 features, English stopwords removed).

Train-test split: 80% training / 20% testing

Models Trained

Logistic Regression

LinearSVC (fast Support Vector Machine)

Random Forest (50 trees)

Evaluation Metrics

Accuracy

Precision

Recall

F1-score

Confusion Matrix

📊 Results

(Sample results, actual may vary slightly depending on random splits)

Model	Accuracy	Precision	Recall	F1-score
Logistic Regression	~0.87	~0.87	~0.87	~0.87
LinearSVC	~0.86	~0.86	~0.86	~0.86
Random Forest	~0.82	~0.82	~0.82	~0.82

Logistic Regression gave the best performance overall.

LinearSVC also performed strongly but slightly slower.

Random Forest was less effective, likely due to text data being better suited to linear models.

📈 Visualizations

Confusion matrices for each model.

Bar plot comparing performance metrics across models.

▶️ How to Run

Open the notebook in Google Colab.

Upload IMDB Dataset.csv when prompted.

Run all cells sequentially.

At the end, you will see performance metrics and plots for comparison.

📝 Conclusion

Logistic Regression was the best model for this task, balancing accuracy and efficiency.

SVM (LinearSVC) also achieved high performance but is slower.

Random Forest worked but lagged behind the linear models, showing that tree-based methods are less effective on high-dimensional sparse text data.
