

# 📈 Happy Customers: Predicting Customer Satisfaction

## 📝 Project Overview

In the competitive logistics and delivery industry, understanding the "why" behind customer happiness is as critical as the delivery itself. This project, completed as part of the **Apziva AI Residency**, focuses on predicting customer satisfaction for **ACME**, a logistics startup.

The goal was twofold:

1. **Predictive Modeling**: Develop a machine learning model to predict whether a customer is happy (1) or unhappy (0) based on survey data.
2. **Feature Optimization**: Identify which specific factors (survey questions) are the strongest drivers of satisfaction to help the business streamline operations and survey design.



## 🚀 Step-by-Step Project Flow

### 1. Data Exploration & Validation (EDA)

The dataset consists of survey responses from customers, where they rated six key aspects (X1 to X6) on a scale of 1–5.

* **X1**: Order delivered on time.
* **X2**: Contents of order were as expected.
* **X3**: I ordered everything I wanted to order.
* **X4**: I paid a good price for my order.
* **X5**: I am satisfied with my courier.
* **X6**: The app makes ordering easy.

**Findings:** I analyzed class balance (ensuring no bias toward happy/unhappy labels) and used correlation heatmaps to identify relationships between delivery speed and courier satisfaction.

### 2. Preprocessing & Feature Selection

* **Data Cleaning**: Verified there were no missing values or outliers that would skew model performance.
* **Feature Importance**: Using techniques like `ExtraTreesClassifier` and correlation analysis, I identified that not all questions were equal. Specifically, **X1 (On-time delivery)** and **X5 (Courier satisfaction)** emerged as primary drivers.
* **Dimensionality Reduction**: I tested models with a reduced feature set to simplify the survey for the client without losing predictive power.

### 3. Model Development & Comparison

I utilized **LazyPredict** to rapidly baseline several models and then fine-tuned the top performers:

* **Logistic Regression**: Used as a baseline for interpretability.
* **Random Forest / Extra Trees**: Leveraged for their ability to handle non-linear relationships in ordinal data.
* **Hyperparameter Tuning**: Applied optimization (via `Hyperopt`) to maximize the F1-score and Accuracy.

### 4. Evaluation

Models were evaluated not just on accuracy, but on **Recall** for unhappy customers. For a business, missing an "unhappy" customer (False Positive) is more costly than misidentifying a happy one.

---

## 💡 Key Insights & Business Impact

* **Operational Priority**: Delivery punctuality (X1) is the #1 predictor of happiness. ACME should prioritize logistics efficiency over app aesthetics (X6) to see the highest ROI in satisfaction.
* **Survey Streamlining**: My analysis suggests that the survey can be shortened from 6 questions to the top 3-4 most impactful ones, reducing customer friction while maintaining **~80%+ prediction accuracy**.
* **Proactive Retention**: The model can be integrated into the CRM to flag "unhappy" predictions in real-time, allowing customer success teams to reach out before a customer churns.

* As demonstrated, the model optimized with **Hyperopt** significantly outperformed the standard XGB classification model
* We identified XGBoost as the most effective model for predicting class 0 (unhappy customers), which is crucial since they represent nearly half of the customer base. After applying advanced hyperparameter optimization, the model achieved an F1 score of 0.80 and an accuracy of 0.77, making it the strongest candidate for this business focus.
* Based on the exploratory data analysis and model selection, it is clear that X5 (customer satisfaction with the courier) and X3 (ability to order everything desired) are key drivers of overall Customer Happiness. To maximize impact, special attention should be directed toward strengthening these two variables, as improvements here are likely to yield the greatest gains in customer satisfaction and loyalty.
---

## 🛠️ Tech Stack

* **Language**: Python
* **Libraries**: Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn, LazyPredict.
* **Tools**: Jupyter Notebook, GitHub.

---

## 👨‍💻 Concluding Remarks for Hiring Managers

This project demonstrates my ability to take a raw business problem and translate it into a technical pipeline that provides **actionable insights**. Beyond just "building a model," I focused on:

* **Feature Engineering**: Understanding which variables actually move the needle for the business.
* **Model Interpretability**: Providing "why" a customer is unhappy, not just "if."
* **End-to-End Ownership**: From data ingestion and cleaning to final business recommendations.

I am eager to apply this data-driven mindset to help your team solve complex problems and drive customer-centric growth.

---


*Developed by Ibrahim Chaoudi as part of the Apziva AI Residency Program.*
