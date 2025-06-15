# 📁 Insurance Fraud Detection Project

## 📝 Introduction

Insurance fraud poses a significant financial burden to the industry, costing billions annually. Detecting fraudulent claims early is critical for insurers to minimize losses, improve claim processing efficiency, and maintain trust with legitimate customers.

This project aims to build an end-to-end fraud detection pipeline using a real-world insurance claims dataset. The workflow is divided into three structured phases:

---

## 🔍 Project Objectives:

1. **Phase 1: Fraud Classification (Supervised Learning)**
   - Predict whether a claim is fraudulent (`isFraud`: Yes/No)
   - Train machine learning models (Random Forest, Logistic Regression) on engineered features
   - Optimize performance using SMOTE for class imbalance and evaluate using F1-score and Recall

2. **Phase 2: Geospatial Risk Mapping**
   - Identify high-risk regions (states and cities) with elevated fraud rates
   - Visualize patterns using bar charts and interactive choropleth maps
   - Inform fraud investigation priorities through geographic insights

3. **Phase 3: Anomaly Detection (Unsupervised Learning)**
   - Detect unusual claim patterns using Isolation Forest
   - Flag claims with outlier behavior (e.g., extreme claim ratios or timing)
   - Enhance fraud monitoring even in the absence of labeled data

---

## 📦 Tools & Libraries Used:
- Python (Pandas, Scikit-learn, Seaborn, Matplotlib)
- `plotly.express` for interactive maps
- `imblearn` for SMOTE
- `IsolationForest` for unsupervised detection

---

This project offers a **comprehensive fraud detection strategy**, combining both supervised and unsupervised techniques, with actionable geospatial insights for operational teams.


 Link: [Work Report](/code_analysis/fraud_analyst.ipynb)

 ## 🧾 Background

Fraudulent insurance claims are a growing concern in the financial services industry. Whether it's exaggerated car repairs, staged accidents, or fake medical expenses, fraudulent activity inflates overall claim costs, burdens investigation teams, and negatively impacts honest policyholders through rising premiums.

Traditional fraud detection often relies on **manual audits** and **rule-based systems**, which are:
- Time-consuming
- Limited in adaptability
- Prone to missing complex fraud patterns

To overcome these limitations, this project explores the use of **machine learning and data science techniques** to detect and prevent fraudulent claims more efficiently and accurately.

We treat this as a **real-world classification and anomaly detection problem**, where the goal is not only to predict fraud but also to understand patterns geographically and behaviorally.

This project is structured in **three phases**:
1. **Supervised Fraud Classification** (to learn from labeled fraud)
2. **Geospatial Risk Mapping** (to locate fraud clusters)
3. **Unsupervised Anomaly Detection** (to catch hidden fraud)

Together, these approaches provide a comprehensive solution to enhancing fraud detection pipelines in insurance.


## 🛠️ Tools & Libraries Used

This project was developed using a suite of open-source Python tools for data manipulation, machine learning, and visualization:

---

### 📚 **Data Handling & Processing**
- **`pandas`**: For data cleaning, aggregation, and transformation
- **`numpy`**: For efficient numerical computations
- **`imblearn` (SMOTE)**: To address class imbalance in supervised learning

---

### 🤖 **Machine Learning**
- **`scikit-learn`**:
  - `LogisticRegression` and `RandomForestClassifier` for supervised classification
  - `train_test_split`, `classification_report`, `confusion_matrix` for model evaluation
  - `IsolationForest` for unsupervised anomaly detection

---

### 📊 **Data Visualization**
- **`matplotlib`** & **`seaborn`**: For static data visualization (bar plots, histograms, confusion matrices)
- **`plotly.express`**: For interactive geospatial visualizations (choropleth maps)

---

### 💻 **Environment**
- **Python 3.x**
- Developed using **VS Code**
- Optional use of **Jupyter Notebook** for interactive exploration

---

These tools enabled the full fraud detection pipeline — from raw data cleaning to interactive map generation and anomaly detection.


## 📈 Analysis Summary

This project uncovered several meaningful insights through each phase of fraud detection:

---

### 🔹 **Phase 1: Fraud Classification**
- The initial model achieved 73% accuracy, but recall was very low due to class imbalance.
- After applying **SMOTE**, recall improved from **10% to 22%**, and precision from **33% to 52%**.
- Key features influencing fraud detection included:
  - `incident_severity_Minor Damage`, `vehicle_claim`, `total_claim_amount`
  - Engineered features like `injury_to_total_ratio` and `tenure_group` also proved valuable.

  ![Model Training](/assets/1st%20Model%20Training.png)
  ![Model Training + SMOTE](/assets/Model%20Training%20+%20SMOTE.png)

---

### 🔹 **Phase 2: Geospatial Risk Mapping**
- **Ohio (OH)** was identified as the most fraud-prone state.
- **Columbus** emerged as the highest-risk city.
- Choropleth map and bar charts clearly showed fraud clustering in certain regions.

![Geospatial Risk Map](/assets/choropleth%20map.jpg)


---

### 🔹 **Phase 3: Anomaly Detection**
- Using **Isolation Forest**, 50 out of 1000 claims were flagged as anomalies.
- These claims showed outlier behavior in total amount, claim ratios, and customer tenure.
- The model added another layer of fraud detection without relying on labeled data.
![Anomaly Detection](/assets/anomaly%20score%20dist.png)

---

Overall, the combination of supervised learning, geospatial analysis, and unsupervised methods provided a **robust, multi-angle approach** to insurance fraud detection.

## 🎓 What I Learned

Working on this insurance fraud detection project helped reinforce and deepen my skills across multiple domains in data science and machine learning:

---

### ✅ **Technical Skills**
- **Data Cleaning & Preprocessing**:
  - Handling missing values, label encoding, and one-hot encoding
  - Feature engineering like claim ratios and customer tenure grouping

- **Machine Learning**:
  - Built and evaluated classification models using `Logistic Regression` and `Random Forest`
  - Applied **SMOTE** to resolve class imbalance, improving model recall and precision
  - Used **Isolation Forest** to perform unsupervised anomaly detection

- **Geospatial Analysis**:
  - Aggregated fraud data by state and city
  - Built bar charts and an interactive **choropleth map** to identify high-risk regions

---

### 🧠 **Analytical Thinking**
- Learned how to interpret model results beyond accuracy (e.g., precision, recall, F1-score)
- Understood the importance of **feature importance** and how engineered features can influence predictions
- Recognized how **fraud is often localized** and can be caught through multiple techniques

---

### 💡 **Real-World Relevance**
- Fraud detection requires a mix of **predictive models and investigative insight**
- Class imbalance is common in real-world problems — solving it requires thoughtful techniques
- Unsupervised learning adds great value when labels are limited or noisy

---

This project gave me practical experience in designing a full fraud detection pipeline and strengthened my confidence in handling real-world classification and anomaly detection problems.


## 🧾 Conclusions

This project successfully demonstrated how machine learning can enhance insurance fraud detection through a multi-phase analytical approach:

---

### 🔍 Key Takeaways:

1. **Supervised models** like Random Forest can effectively predict fraud when supported by good feature engineering and class balancing techniques (e.g., SMOTE).
2. **Geospatial risk mapping** revealed that fraud is not randomly distributed — certain cities and states show significantly higher fraud rates.
3. **Unsupervised anomaly detection** (via Isolation Forest) provided a valuable layer of fraud discovery, capable of flagging suspicious claims that might not yet be labeled.

---

### 🎯 Overall Outcome:
- Built a full fraud detection pipeline from raw data to model evaluation.
- Combined classification, geospatial analysis, and anomaly detection.
- Delivered both actionable insights and operational tools (e.g., maps, metrics, flagged claims).

This end-to-end project provides a strong foundation for deploying real-world fraud analytics and could be extended with:
- Real-time scoring of incoming claims
- Deep learning-based anomaly detection
- Integration into insurer claim workflows



