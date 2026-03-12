## AI for Disease Detection (2060 Challenge) — Student Project Guide

### 1) Story Context
In 2060, a global health network deploys portable diagnostic sensors in remote regions. Each sensor collects biological signals and environmental factors. Your task is to build a model that predicts disease stage for each patient using tabular data.

### 2) Learning Goals
By completing this project, you will learn to:
- Explore and clean tabular health data
- Handle missing values and outliers responsibly
- Discover correlations and multicollinearity
- Train and compare multiple models
- Evaluate performance with Macro F1
- Produce a clean, reproducible workflow

### 3) Files in This Folder
- Train.csv — training data with the target label
- Test.csv — test data without the target label
- SampleSubmission.csv — required submission format
- Starter Notebook.ipynb — baseline workflow

### 4) Dataset Features
**Input features**
- Age
- BodyTemp
- HeartRate
- OxygenLevel
- ImmuneMarkerA
- ImmuneMarkerB
- BloodSugar
- SleepHours
- StressLevel
- PollutionExposure
- GeneticRiskScore
- PhysicalActivity
- NutritionScore

**Target**
- DiseaseStage
  - 0 = Healthy
  - 1 = Early Stage Disease
  - 2 = Severe Disease

### 5) Evaluation Metric
You will be scored with **Macro F1**, which treats each class equally and is a strong metric for imbalanced classes. Your goal is to improve Macro F1 on a validation split without overfitting.

### 6) Project Tasks (Step-by-Step)
1. **Load the data**
   - Open Starter Notebook.ipynb
   - Read Train.csv, Test.csv, SampleSubmission.csv
2. **Explore the data**
   - Inspect column types and missing values
   - Visualize class distribution of DiseaseStage
   - Create a correlation heatmap
3. **Handle missing data**
   - Choose a strategy (median imputation is a strong baseline)
   - Keep the same imputation strategy for train and test
4. **Build a baseline model**
   - Start with Logistic Regression
   - Use scaling if needed
   - Measure Macro F1 on a validation split
5. **Try additional models**
   - Decision Tree
   - Random Forest
   - KNN
   - Compare Macro F1 results
6. **Avoid overfitting**
   - Use a train/validation split
   - Track performance changes
   - Keep features consistent between train and test
7. **Generate predictions for Test**
   - Train the final model on full Train.csv
   - Predict DiseaseStage for all rows in Test.csv
   - Save predictions using SampleSubmission.csv format

### 7) Baseline Checklist
- Data loaded correctly
- Missing values handled
- Feature correlations explored
- Baseline model trained
- Macro F1 reported
- Submission file generated

### 8) Submission Format
Your submission file must contain exactly:
- PatientID
- DiseaseStage

Example:
```
PatientID,DiseaseStage
P000001,0
P000002,1
```

### 9) Suggested Extensions (Optional)
- Feature engineering: ratios or interactions between vitals
- Try different imputation strategies
- Hyperparameter tuning
- Cross-validation

### 10) Academic Integrity
- Do your own analysis
- Cite any external sources
- Focus on clear reasoning and reproducibility

### 11) Deliverables
Submit:
- Your final submission CSV
- A short report explaining your model choices
- A brief summary of what you tried and what worked best
