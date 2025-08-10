# Sleep Health & Lifestyle – Stress Level Prediction

## Overview

This project analyzes and processes a **Sleep Health and Lifestyle dataset** to explore the relationship between sleep habits, lifestyle factors and stress levels.
It applies **data preprocessing, visualization, and machine learning models** to predict a person’s stress level based on various health and lifestyle indicators.

The project uses **Random Forest, Logistic Regression, and Decision Tree** classifiers to compare performance and identify the most effective prediction model.

---

## Dataset

The dataset contains the following columns:

| Feature                 | Description                           |
| ----------------------- | ------------------------------------- |
| Person ID               | Unique identifier for each individual |
| Gender                  | Male / Female                         |
| Age                     | Age in years                          |
| Occupation              | Profession of the individual          |
| Sleep Duration          | Average sleep hours per day           |
| Quality of Sleep        | Rating from 1–10                      |
| Physical Activity Level | Activity score (1–10)                 |
| Stress Level            | Target variable (1–10)                |
| BMI Category            | Normal / Overweight / Obese           |
| Blood Pressure          | Recorded in mmHg (e.g., 120/80)       |
| Heart Rate              | Resting heart rate (bpm)              |
| Daily Steps             | Average steps per day                 |
| Sleep Disorder          | Sleep Apnea / Insomnia / None         |

---

## Technologies Used

* **Programming Language:** Python 
* **Libraries:**

  * `pandas`, `numpy` – Data handling
  * `matplotlib`, `seaborn` – Data visualization
  * `scikit-learn` – Machine learning models & evaluation
* **Models Used:**

  * Random Forest Classifier
  * Logistic Regression
  * Decision Tree Classifier

---

## Project Workflow

### Data Preprocessing

* Removed irrelevant columns (`Person ID`, `Sleep Disorder`)
* Encoded categorical variables:

  * Gender → 0: Male, 1: Female
  * BMI Category → 0: Normal, 1: Overweight, 2: Obese
  * Occupation → Encoded to numerical values
  * Blood Pressure → Categorized into Low, Normal, High
* Handled duplicate and inconsistent values
* Removed outliers using quantile thresholds
* Standardized feature scaling for models requiring it

---

### Data Visualization

* Histograms & boxplots for all features (before & after processing)
* Distribution checks for each feature
* Outlier detection through visual plots

---

### Model Training & Evaluation

* **Split:** 80% training, 20% testing (stratified)
* **Evaluation Metrics:** Accuracy, Precision, Recall, F1-score, Confusion Matrix, ROC Curve, AUC Score
* **Model Performance:**

  * Random Forest: Highest accuracy among tested models
  * Logistic Regression & Decision Tree also evaluated for comparison
* Plotted comparison charts for **Accuracy, Precision, Recall, F1-score** across models

---

### User Input Prediction

The program allows a user to input:

* Gender, Age, Occupation, Sleep Duration, Sleep Quality, Physical Activity Level, BMI, Blood Pressure, Heart Rate, Daily Steps
  ➡ Predicts **Stress Level** instantly using the trained Random Forest model.

---

## Example Visuals

* Histogram plots of features
* Boxplots before & after processing
* ROC Curves for each class
* Model comparison bar charts

---

## Installation & Usage

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/sleep-health-stress-prediction.git
   ```
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Place the dataset in the project directory and name it:

   ```
   SleepHealthAndLifestyleDATASET_NotProcessed.csv
   ```
4. Run the project:

   ```bash
   python sleep_health_analysis.py
   ```

---

## License

This project is licensed under the [Apache-2.0 license](https://www.apache.org/licenses/).

---

## Contributing

Contributions are welcome!

* Fork the repo
* Create a feature branch
* Submit a pull request
