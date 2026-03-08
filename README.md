
# 🏏 IPL Match Winning Probability Prediction

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-yellow)
![Sports Analytics](https://img.shields.io/badge/Domain-Sports%20Analytics-green)
![License](https://img.shields.io/badge/License-MIT-brightgreen)

A machine learning project that predicts the **winning probability of an IPL cricket match** during the second innings using match statistics such as runs required, wickets remaining, overs left, and run rate.

The model is trained using **historical IPL match data** and provides real-time probability predictions for the chasing team.

---

# 📌 Project Overview

Cricket analytics has become an important part of modern sports analysis. During a match, fans and analysts often want to know:

> *“What are the chances of the chasing team winning from the current match situation?”*

This project uses **machine learning techniques** to estimate the **win probability of the batting team during the chase**.

The model analyzes historical IPL match data and learns relationships between **match conditions and outcomes**.

---

# 🏗 Project Workflow

```text
Historical IPL Data
        │
        ▼
Data Cleaning
        │
        ▼
Feature Engineering
        │
        ▼
Model Training
(Logistic Regression)
        │
        ▼
Model Evaluation
        │
        ▼
Winning Probability Prediction
```

---

# 📊 Dataset

The project uses **historical IPL datasets**:

### 1️⃣ matches.csv

Contains match-level information.

| Feature     | Description       |
| ----------- | ----------------- |
| season      | IPL season year   |
| team1       | first team        |
| team2       | second team       |
| toss_winner | toss winning team |
| winner      | match winner      |
| venue       | match location    |

---

### 2️⃣ deliveries.csv

Contains **ball-by-ball match data**.

| Feature      | Description        |
| ------------ | ------------------ |
| match_id     | match identifier   |
| batting_team | batting team       |
| bowling_team | bowling team       |
| over         | over number        |
| ball         | ball number        |
| total_runs   | runs scored        |
| is_wicket    | wicket information |

This dataset is used to compute **dynamic match features**.

---

# ⚙️ Features Used for Prediction

The model uses features representing the **current state of the match**.

| Feature           | Description           |
| ----------------- | --------------------- |
| runs_left         | runs required to win  |
| balls_left        | balls remaining       |
| wickets_left      | wickets remaining     |
| target            | target score          |
| current_run_rate  | current scoring rate  |
| required_run_rate | required scoring rate |

Example match situation:

```
Runs Left: 60
Balls Left: 30
Wickets Left: 5
Required Run Rate: 12
```

These features help the model estimate the **probability of winning**.

---

# ⚙️ Technologies Used

| Technology       | Purpose                 |
| ---------------- | ----------------------- |
| Python           | Programming language    |
| Pandas           | Data processing         |
| NumPy            | Numerical operations    |
| Matplotlib       | Data visualization      |
| Scikit-Learn     | Machine learning model  |
| Jupyter Notebook | Development environment |

---

# 📂 Project Structure

```
IPL-WINNING-PREDICTION
│
├── IPL_WINNING_PREDICTION.ipynb
├── matches.csv
├── deliveries.csv
└── README.md
```

---

# 🔬 Implementation

## 1️⃣ Data Loading

The IPL datasets are loaded using Pandas.

```python
import pandas as pd

matches = pd.read_csv("matches.csv")
deliveries = pd.read_csv("deliveries.csv")
```

---

# 2️⃣ Data Cleaning

Data preprocessing steps include:

* removing unnecessary columns
* handling missing values
* filtering relevant matches

---

# 3️⃣ Feature Engineering

New match-state features are created.

```python
runs_left
balls_left
wickets_left
current_run_rate
required_run_rate
```

These features describe the **current match situation**.

---

# 4️⃣ Model Training

The project uses **Logistic Regression** for probability prediction.

```python
from sklearn.linear_model import LogisticRegression

model = LogisticRegression()
model.fit(X_train, y_train)
```

Logistic regression is suitable because it predicts **probabilities between 0 and 1**.

---

# 📊 Model Evaluation

The model is evaluated using the test dataset.

Example:

```python
model.score(X_test, y_test)
```

This measures how accurately the model predicts match outcomes.

---

# 🔮 Example Prediction

Example match situation:

```
Batting Team: CSK
Bowling Team: MI
Runs Left: 50
Balls Left: 30
Wickets Left: 6
Target: 180
```

Model output:

```
Winning Probability

CSK → 65%
MI → 35%
```

---

# 📈 Applications

This model can be used for:

* Sports analytics platforms
* Live match prediction systems
* Cricket broadcasting analysis
* Betting probability estimation
* Data-driven sports insights

---

# 📚 Learning Outcomes

Through this project:

* Learned **sports analytics using machine learning**
* Performed **feature engineering on time-series sports data**
* Built a **probability prediction model**
* Implemented **logistic regression for classification**
* Analyzed match statistics to derive insights

---

# 🔮 Future Improvements

Possible enhancements:

* Use advanced models like **Random Forest or XGBoost**
* Build a **real-time match prediction dashboard**
* Deploy the model using **Flask or Streamlit**
* Integrate live match APIs
* Add visualization of win probability over time

---

# 🤝 Contributing

Contributions are welcome.

Steps:

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Submit a pull request

---


If you want, I can also show you **how to organize these 4 projects so your GitHub profile looks like a strong Machine Learning portfolio for internships and research positions.**
