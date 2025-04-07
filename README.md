# 🎧 Grammar Scoring Engine-SHL Assessment

Predict grammar proficiency scores (on a scale of 0 to 5) using machine learning techniques applied to spoken audio data. The aim is to build an intelligent scoring engine that can evaluate how grammatically accurate a spoken response is—similar to how a human evaluator would—by analyzing patterns in speech such as pronunciation, fluency, pauses, pitch, and structural coherence.

---

## 📊 Dataset Description

- `train.csv`: Contains `filename` and corresponding `label` (grammar score)
- `test.csv`: Contains `filename` of test audio samples
- `sample_submission.csv`: Template CSV for submission format
- `audios_train/`: Training audio `.wav` files
- `audios_test/`: Testing audio `.wav` files

---

## 🧪 Workflow

1. **Preprocessing & Feature Extraction**
   - Extract MFCCs, pitch, spectral features, etc. using `Librosa`
   - Save as numerical feature vectors

2. **Model Training**
   - Split into train/val
   - Use `XGBoost Regressor` for prediction
   - Evaluate with Pearson Correlation, RMSE, MAE

3. **Prediction**
   - Extract features from test audio
   - Predict scores using trained model
   - Generate `submission.csv`

---

## 📈 Evaluation Metrics

- **📌 Pearson Correlation**  
 0.6212

- **📉 Root Mean Squared Error (RMSE)**  
0.9191

- **📊 Mean Absolute Error (MAE)**  
  0.7168

---


