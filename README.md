# 🏡 House Price Classifier: Expensive or Not?

This project builds an end-to-end machine learning pipeline to classify houses in Ames, Iowa, as **"expensive"** or **"not expensive"** based on 80+ features from the housing dataset. It's part of my final project for a machine learning course and demonstrates real-world model development, preprocessing, evaluation, and optimization.

---

## ✨ Overview

* 📂 Dataset: Ames Housing Dataset (81 features)
* 🎓 Goal: Classify whether a house is "expensive" using numerical, ordinal, and categorical features
* 🚀 Techniques: Preprocessing pipelines, feature engineering, grid search, model comparison
* 🔧 Tools: Scikit-learn, KNN, Random Forest, SVC, pandas, NumPy, matplotlib, seaborn

---

## 📆 Project Structure

```
├── data/                # housing dataset
├── notebooks/           # Colab notebooks
│   └── final_model.ipynb
├── images/              # Plots and visualizations
├── README.md            # Project documentation (this file)
├── requirements.txt     # List of dependencies
└── LICENSE              # MIT License
```

---

## 📊 Features & Preprocessing

* **Numerical**: Scaled using `StandardScaler`
* **Categorical**: One-hot encoded
* **Ordinal**: Custom mappings (e.g., Quality: Po < Fa < TA < Gd < Ex)
* **Missing values**: Imputed using `SimpleImputer`
* **Feature selection**: Low-variance and irrelevant features dropped

---

## 🤖 Models Evaluated

| Model         | Accuracy                   | Precision | Recall | F1 Score | Kappa |
| ------------- | -------------------------- | --------- | ------ | -------- | ----- |
| SVC           | ✔ Best Overall             | 	0.9	     |0.857143|	0.878049 | 0.858142
| Random Forest | Good balance               |  0.941176 |0.761905| 0.842105 |0.818784
| KNN           | Performs well with scaling |  0.853659 |0.833333| 0.843373 | 0.81743 

> SVC achieved the **best overall performance** across all metrics.

---

## 🔢 Metrics Used

* Accuracy, Precision, Recall, F1 Score
* Specificity & Balanced Accuracy
* Cohen's Kappa

---

## ⚖️ Why Not Just Use Price?

* Price alone isn't enough: it depends on **lot size, location, quality, finishes, and more**.
* Classification allows targeting for decision-making (e.g. "worth investing in?").

---

## 🔍 Key Insights

* Feature preprocessing was **crucial** due to mixed data types (ordinal, nominal, numeric)
* Some models like GaussianNB performed well on recall but poorly on precision
* Grid search improved DecisionTree and XGBoost significantly
* Feature importance from tree-based models helped refine the pipeline

---

## 🚧 Limitations & Ideas

* Current features **lack semantics**: we ignore **text descriptions, images, or location proximity**
* **Genre/culture equivalents in housing** like neighborhood prestige aren't fully captured
* Could enhance with **clustering** or **NLP on descriptions** in future work

---

## 🚀 Run the Notebook

Open [`notebooks/final_model.ipynb`](/Copetition_pipeline_for_multiple_models.ipynb) to walk through the full pipeline:

* Preprocessing
* Model training & tuning
* Evaluation

---

## ✍️ License

This project is licensed under the **MIT License**.

---

## 🚀 Author

**Hassan Merai(Fred)**
Data scientist passionate about real-world ML and automation. Connect with me:

* [LinkedIn](https://www.linkedin.com/in/Hassan-Merai-nickname-Fred)
* [Medium](https://medium.com/@hassanmerai79)
* [GitHub](https://github.com/Hassan-Merai)

---

*"Teaching machines to spot an expensive house isn't just about numbers — it's about mimicking human judgment."*
