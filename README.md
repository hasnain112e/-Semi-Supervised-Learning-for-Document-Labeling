# -Semi-Supervised-Learning-for-Document-Labeling
📝 Semi-Supervised Learning for Document Labeling
This project implements a self-training semi-supervised learning approach to classify text documents using a small labeled dataset and a larger unlabeled dataset.
By assigning pseudo-labels to high-confidence predictions on unlabeled data, the model improves performance without requiring expensive manual labeling.

📌 Project Overview
Technique: Self-training (semi-supervised learning)

Model: Logistic Regression (can be replaced with any classifier)

Feature Extraction: TF-IDF vectorization

Goal: Improve classification accuracy by leveraging unlabeled data

Use Cases: Sentiment analysis, spam detection, topic classification

📂 Dataset Description
The dataset consists of:

Small Labeled Data: 4 sample reviews with sentiment labels (1 = positive, 0 = negative)

Large Unlabeled Data: 8 text samples without labels

Both datasets are combined for vectorization to ensure consistent feature space

🛠 Installation
bash
Copy
Edit
pip install pandas scikit-learn matplotlib seaborn
🚀 How to Run
1️⃣ Clone the Repository

bash
Copy
Edit
git clone https://github.com/YourUsername/semi-supervised-document-labeling.git
cd semi-supervised-document-labeling
2️⃣ Run the Script / Notebook

bash
Copy
Edit
python semi_supervised_document_labeling.py
or open in Google Colab / Jupyter Notebook.

🔄 Workflow
Load Data

Small labeled dataset

Larger unlabeled dataset

Vectorize Text

TF-IDF vectorization on combined labeled + unlabeled text

Train Initial Model

Logistic Regression trained only on labeled data

Generate Pseudo-Labels

Predict probabilities for unlabeled samples

Keep only high-confidence predictions (≥ 90%)

Retrain Model

Combine labeled + pseudo-labeled data for training

Evaluate & Inspect Predictions

📊 Example Output
Predicted Labels for Unlabeled Data:

arduino
Copy
Edit
                        text  pseudo_label
0         I love this phone             1
1            Not good at all             0
2  Really satisfied with ...             1
3     Horrible app experience            0
4         It works perfectly             1
5          Useless and buggy            0
6  Fantastic design and build            1
7     This was disappointing            0
📈 Benefits of This Approach
✅ Reduces labeling cost by using unlabeled data
✅ Improves performance with minimal labeled data
✅ Easy to adapt for real-world NLP problems

🔮 Future Improvements
Use transformer-based models like BERT for embeddings

Implement iterative self-training with multiple pseudo-labeling rounds

Add evaluation metrics on a test set for better performance tracking
