# 🧠 Self-Analysis Mental Health Prediction Model

## **Objective**
This project develops a **Self-Analysis Mental Health Model** that predicts possible mental health conditions based on user-provided symptoms. The model is designed for **seamless integration** into a chatbot or application, focusing on:
- **Accuracy**
- **Interpretability**
- **Efficiency**

Additionally, a **basic UI or CLI script** is provided for testing and interaction.

---

## **📂 Project Structure**
```
📦 ArogoAI_Mental_Health_Prediction
│
├── 📂 datasets/                      # Datasets used for training and evaluation
│   ├── 📂 datasets_original/          # Raw datasets
│   │   ├── depression_anxiety_data.csv
│   │   ├── survey.csv (Not Used)
│   │
│   ├── 📂 datasets_preprocessed/      # Processed datasets
│   │   ├── preprocessed_depression_anxiety_data.csv
│   │   ├── preprocessed_survey.csv (Not Used)
│   │
│   ├── 📂 datasets_pickle/            # Saved datasets in pickle format
│   │   ├── depression_anxiety_data.csv_pickle/
│   │       ├── X_train.pkl
│
├── 📂 code/                           # Python scripts for training and inference
│   ├── training.ipynb                 # Model training notebook
│   ├── sample.py                      # Sample script (remove if unused)
│   ├── predict_mental_health.py        # CLI script for inference
│
├── 📂 models/                         # Trained models
│   ├── 📂 depression_anxiety_data.csv_models/
│   │   ├── random_forest_model.pkl
│   │   ├── xgboost_model.pkl
│   │
│   ├── 📂 (NOT USED)survey.csv_models/  # Unused models
│   │   ├── xgboost_expanded_model.pkl
│
├── 📂 encoders/                        # Encoders for categorical variables
│   ├── 📂 depression_anxiety_data.csv_encoders/
│   │   ├── label_encoders.pkl
│   │   ├── target_encoder.pkl
│
├── .gitignore                          # Ignore unnecessary files
├── requirements.txt                     # Python dependencies
├── mental_health_report.pdf             # Documentation report
└── README.md                            # This file
```

---

## **📊 Dataset & Preprocessing**
We use **publicly available mental health datasets**, including:
- **Depression and Anxiety Symptoms Dataset**
- **Mental Health in Tech Survey** (not used)

### **Preprocessing Steps**
1. **Data Cleaning** – Remove inconsistencies and missing values.
2. **Normalization** – Process text for better analysis.
3. **Exploratory Data Analysis (EDA)** – Identify relationships between symptoms and conditions.
4. **Feature Engineering** – Encode symptoms and mental health conditions as features and labels.
5. **Feature Selection** – Choose the most impactful features.

Preprocessed datasets are saved as:
```
📂 datasets_preprocessed/      # Processed datasets
│   │   ├── preprocessed_depression_anxiety_data.csv
│   │   ├── preprocessed_survey.csv (Not Used)
```
The code for preprocessing is present in [training.ipynb](code/training.ipynb). The encoders that are used in this preprocessing are stored as .pkl files in the [encoders](encoders/depression_anxiety_data.csv_encoders) folder.

---

## **🛠 Model Development**

We trained and compared the following models:

1. Random Forest
2. XGBoost

The best-performing model is stored in:
```
📂 models/depression_anxiety_data.csv_models/
├── random_forest_model.pkl
├── xgboost_model.pkl
```
---

## **Evaluation Metrics**

1. Accuracy
2. Precision

To train models:
```
python code/training.ipynb
```
---

## **🔍 Model Inference**

We provide a command-line script to test the trained model:
```
python code/predict_mental_health.py
```
---

## **🧠 LLM Experimentation**

We used LLM (Google Gemini) to:

1. Explain the predicted mental health condition in natural language.
2. Suggest coping mechanisms based on symptoms.

Results are documented in [mental_health_report.pdf](mental_health_report.pdf).(This file is an example output file).

---

## **📈 SHAP/LIME Analysis**

To interpret model predictions, we used:

LIME (Local Interpretable Model-Agnostic Explanations)

---

## **📦 Installation & Dependencies**

1. Clone the Repository
```
git clone https://github.com/your_username/ArogoAI_Mental_Health_Prediction.git
cd ArogoAI_Mental_Health_Prediction
```
2. Install Dependencies

Create a virtual environment and install required packages:
```
python -m venv venv
source venv/bin/activate  # On macOS/Linux
venv\Scripts\activate  # On Windows
pip install -r requirements.txt
```

3. Run the Model

```
python code/predict_mental_health.py
```
