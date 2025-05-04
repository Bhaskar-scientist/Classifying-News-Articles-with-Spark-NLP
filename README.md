# Classifying-News-Articles-with-Spark-NLP
📰 Classifying News Articles with Spark NLP
Built a scalable text classification model using Spark NLP, PySpark ML, and John Snow Labs' pre-trained models. The project processes and classifies 2,225 BBC News articles into five categories: business, entertainment, politics, sport, and tech.

📌 Project Highlights
📄 Dataset: 2,225 labeled BBC news articles

🧠 Goal: Accurately classify each article into one of the five categories

⚙️ Tech Stack: PySpark, Spark NLP, Spark MLlib, Pandas, John Snow Labs NLP models

🛠 Pipeline Includes:

Data ingestion and cleaning

Text preprocessing (tokenization, lemmatization, stopwords removal)

Feature extraction (TF-IDF, CountVectorizer)

Model training using Spark ML algorithms

Evaluation using accuracy, F1-score, and precision/recall

☁️ Scalable GCP-Based Architecture (Suggested for Production)
While the current implementation runs locally, the project is designed to be production-ready and can be deployed using the following Google Cloud Platform architecture:

pgsql
Copy
Edit
              +-----------------------------+
              |   Google Cloud Storage (GCS)|
              |   (Raw Data Input)          |
              +-------------+---------------+
                            |
                            v
           +-------------------------------+
           |  Dataproc Cluster (PySpark Job)|
           |  - Spark NLP Pipeline          |
           |  - Model Training & Inference  |
           +-------------------------------+
                            |
                            v
              +-----------------------------+
              |  BigQuery (Model Outputs)   |
              +-----------------------------+
                            |
                            v
            +--------------------------------+
            |  Streamlit / Flask Web App     |
            |  (For real-time predictions)   |
            +--------------------------------+
⚙️ Future enhancement: Export the trained model and deploy it as a Cloud Function or REST API with real-time input and output handling.

🧪 Tools & Libraries Used
Apache Spark & PySpark – Distributed processing

Spark NLP (John Snow Labs) – Efficient NLP on Spark

Spark MLlib – Machine learning on large datasets

Jupyter Notebook – Interactive development

📁 Repository Structure
vbnet
Copy
Edit
📦 Classifying-News-Articles-with-Spark-NLP
 ┣ 📓 Spark NLP & ML for Text Classification.ipynb
 ┣ 📜 README.md
📈 Results
The trained model demonstrated robust accuracy across all five news categories. PySpark's distributed architecture and Spark NLP's optimized components ensured efficient handling of structured and unstructured text data at scale.

🚀 Getting Started
1. Clone the Repo
bash
Copy
Edit
git clone https://github.com/Bhaskar-scientist/Classifying-News-Articles-with-Spark-NLP.git
cd Classifying-News-Articles-with-Spark-NLP
2. Install Dependencies
bash
Copy
Edit
pip install pyspark spark-nlp pandas
3. Launch Jupyter Notebook
bash
Copy
Edit
jupyter notebook
Open and run:
📓 Spark NLP & ML for Text Classification.ipynb

🔮 Future Improvements
Deploy classifier via Streamlit or Flask UI

Integrate the pipeline with Google Cloud Platform

Serve predictions via REST API (e.g., FastAPI + Cloud Run)

Visualize key insights: class distribution, confusion matrix, keyword clouds

Experiment with transformer-based models (e.g., BERT) using Spark NLP

👨‍💻 Author
Bhaskar Reddy
Data Scientist | NLP & ML Enthusiast
🔗 LinkedIn | 🛠 Portfolio (Coming soon)

⭐️ If you found this helpful...
Give the repository a star ⭐️, fork it, or share with fellow developers working on NLP, PySpark, or cloud-native data engineering!
