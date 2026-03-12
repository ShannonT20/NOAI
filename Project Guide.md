## NOAI Demo — Round 3: Data Analysis Exam

Welcome. This is the practical exam from the 3rd round of last year’s edition, used as part of the selection process for IOAI 2025. It contains a single data analysis task, evaluated using the F-score. This version is provided as a demo of the EduSpace platform for those interested in joining the EduSpace–IOAI initiative, which aims to universalize access to basic AI knowledge and digital literacy.

### 1) Exam Task Overview
You are given a tabular dataset from a 2060 health monitoring system. Your goal is to predict the disease stage for each patient using the provided features.

### 2) Files in This Folder
- Train.csv — training data with the target label
- Test.csv — test data without the target label
- SampleSubmission.csv — required submission format
- Starter Notebook.ipynb — baseline workflow
- VariableDefinitions.xlsx — feature descriptions

### 3) Dataset Features
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

### 4) Evaluation Metric
Your score is **Macro F1**. This metric treats each class equally, which is important for imbalanced datasets.

### 5) What You Must Do
1. **Load and inspect the data**
   - Check column names and shapes
   - Identify missing values
2. **Prepare the data**
   - Handle missing values
   - Decide whether scaling is needed
3. **Train a model**
   - Start with Logistic Regression as a baseline
   - Try at least one additional model
4. **Evaluate**
   - Use a train/validation split
   - Report Macro F1 on the validation split
5. **Generate predictions**
   - Train a final model on all training data
   - Predict DiseaseStage for Test.csv
   - Save predictions using the required submission format

### 6) Submission Format
Your submission file must contain exactly:
- PatientID
- DiseaseStage

Example:
```
PatientID,DiseaseStage
P000001,0
P000002,1
```

### 7) Deliverables
Submit:
- Your executed notebook with all code and outputs
- Your final submission CSV
- A brief report describing your approach and results
If you need clarification or encounter issues, notify the examiner before submitting.

### 8) Academic Integrity
- Do your own work
- Cite any external sources
