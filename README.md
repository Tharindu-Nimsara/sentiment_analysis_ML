# Sentiment Analysis and Review Summarization System  

## 📌 Introduction  
The rapid growth of user-generated content on platforms such as social media, online reviews, and e-commerce websites has created an urgent need for automated sentiment analysis systems. Businesses and researchers rely on these systems to understand customer opinions, improve services, and make data-driven decisions.  

This project implements a **machine learning-based sentiment analysis system** capable of classifying user reviews into **positive** or **negative** sentiments. Alongside classification, it also features a **summarization tool** powered by **OpenAI’s GPT-4o**, which generates concise summaries of multiple reviews.  

The system is designed with a user-friendly **web interface**, making it accessible for real-time analysis and suitable for practical business applications.  

---

## 🎯 Problem Statement  
E-commerce platforms generate massive volumes of reviews, which are challenging to analyze manually due to:  
- Fake and biased reviews  
- High data volume  
- Lack of trust and transparency  
- Time-consuming and error-prone manual analysis  

Existing solutions often struggle with **scalability** and **usability**. This project addresses these challenges with an **intelligent sentiment classification and summarization system**.  

---

## ⚙️ Features  
- **Binary Sentiment Classification**: Classifies text as *Positive* or *Negative*.  
- **Summarization Tool**: Summarizes user reviews using **GPT-4o API** (requires at least 5 reviews).  
- **Machine Learning Models Tested**: Logistic Regression, Naive Bayes, Decision Tree, Random Forest, Support Vector Machine.  
- **Best Performing Model**: Logistic Regression with **88.2% accuracy** and an **F1-score of 0.88**.  
- **Web Interface**: Built with HTML, CSS, Python (Flask), and JavaScript for interactive user experience.  

---

## 📊 Development Workflow  
1. **Project Setup**  
   - Repository initialized on GitHub  
   - Virtual environment created (`virtualenv`)  
   - Installed dependencies: `numpy`, `pandas`, `matplotlib`, `scikit-learn`, `jupyter`  

2. **Dataset Acquisition**  
   - Dataset sourced from Kaggle using API key  
   - Preprocessing applied:  
     - Case normalization  
     - Link, punctuation, and number removal  
     - Stop word removal  
     - Stemming  
     - Vectorization  

3. **Model Training & Evaluation**  
   - Tested 5 ML models with hyperparameter tuning  
   - Evaluated using **accuracy, precision, recall, F1-score**  
   - Used **5-fold cross-validation** to ensure generalization  
   - Selected **Logistic Regression** as the best-performing model  

4. **Web Application**  
   - Sentiment analysis deployed with Flask (`app.py`)  
   - Frontend: `index.html`, CSS, JavaScript  
   - Integrated GPT-4o API for summarization  

---

## 📈 Experimental Results  
| Model               | Accuracy | Precision | Recall | F1-score |
|---------------------|----------|-----------|--------|----------|
| Logistic Regression | **88.2%** | 0.89      | 0.87   | **0.88** |
| Random Forest       | 85.7%    | 0.86      | 0.85   | 0.85     |
| Support Vector Machine | 87.1% | 0.88      | 0.86   | 0.87     |
| Naive Bayes         | 83.4%    | 0.84      | 0.83   | 0.83     |
| Decision Tree       | 79.8%    | 0.80      | 0.79   | 0.79     |

---

## 🧪 Evaluation Metrics  
- **Accuracy** – Overall correct predictions  
- **Precision** – Reliability of positive predictions  
- **Recall** – Ability to capture true positives  
- **F1-score** – Balance between precision & recall  

Additionally, summarization performance was evaluated through response time, relevance, and human judgment.  

---

## 🚀 Limitations & Future Work  
- Dataset bias (limited domain coverage)  
- Difficulty handling sarcasm/irony  
- Binary classification only (no neutral/multi-class sentiments)  
- Dependent on GPT-4o API limits & costs  
- English-only support  

**Future Improvements**:  
- Multi-class classification (positive, negative, neutral)  
- Advanced deep learning models (e.g., LSTMs, Transformers)  
- Multilingual support  
- Feature-based sentiment analysis  

---

## 👨‍💻 Contributions  
- **Anushka** – Group Leader, ML Model Evaluation, Documentation  
- **Tharindu** – ML Model Development, Backend Development  
- **Lisara** – ML Model Evaluation, Frontend Development, Documentation  

---

## 🛠️ Installation & Usage  

### Prerequisites  
- Python 3.8+  
- Virtualenv  
- Kaggle account & API key  
- OpenAI API key  

### Setup  
```bash
# Clone repository
git clone https://github.com/your-repo-link.git
cd sentiment-analysis-system

# Create and activate virtual environment
pip install virtualenv
virtualenv venv
source venv/bin/activate   # for Linux/Mac
venv\Scripts\activate      # for Windows

# Install dependencies
pip install -r requirements.txt
```

### Running the Application

# Start Flask app
python app.py

Then open http://127.0.0.1:5000/ in your browser.
