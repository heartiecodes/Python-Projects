# Student Exam Success Prediction

## Overview
This project predicts whether students will pass their final examination using machine learning. It demonstrates a complete **end-to-end data science workflow**, from data cleaning and exploratory analysis to model training and evaluation. The analysis explores how academic behaviors, lifestyle factors, and demographic variables influence student performance.

## Dataset
The dataset contains **1200 student records** with features reflecting academic, behavioral, and lifestyle characteristics, including:

- `StudyHoursPerWeek` – Number of hours spent studying weekly  
- `AttendanceRate` – Percentage of classes attended  
- `SleepHours` – Average hours of sleep per night  
- `PreviousGrade` – Last academic grade  
- `StressLevel` – Self-reported stress level (1–10)  
- `PartTimeJob` – Whether the student has a part-time job  
- `InternetAccess` – Availability of internet at home  
- `SocialMediaHoursPerDay` – Daily social media usage  
- `AssignmentsCompleted` – Number of assignments completed  
- `ClassParticipationScore` – Participation in class activities  
- `ExtracurricularActivities` – Number of extracurricular activities participated in  

The **target variable** is `PassFinalExam`:

- `1` = Student passes  
- `0` = Student fails

## Methodology
The project follows a structured data science workflow:

1. **Data Cleaning**  
   - Handle missing values  
   - Standardize inconsistent categorical labels  
   - Detect and remove extreme outliers  

2. **Exploratory Data Analysis (EDA)**  
   - Visualize distributions and relationships  
   - Identify key patterns influencing exam success  

3. **Feature Engineering**  
   - `StudyEfficiency = PreviousGrade / StudyHoursPerWeek`  
   - `LifestyleScore = SleepHours - StressLevel`  

4. **Machine Learning Modeling**  
   - Split data into training (80%) and testing (20%) sets  
   - Train a **Random Forest Classifier**  

5. **Model Evaluation**  
   - Accuracy, Confusion Matrix, Precision, Recall, F1-score  
   - Feature importance analysis  

## Key Insights
From EDA and feature importance analysis:

- Higher **attendance** increases the likelihood of passing  
- Strong **previous grades** correlate with success  
- More **study hours** generally improve outcomes  
- Higher **stress levels** and insufficient **sleep** reduce chances of passing  
- Both **academic and lifestyle factors** are critical for success  

## Results
The Random Forest model successfully identified patterns and achieved reliable predictions on the test set. Feature importance revealed that the top predictors were:

1. `AttendanceRate`  
2. `PreviousGrade`  
3. `StudyHoursPerWeek`  
4. `StressLevel`  
5. `SleepHours`  

## Tools and Technologies
- **Programming Language:** Python  
- **Data Analysis:** Pandas, NumPy  
- **Visualization:** Matplotlib, Seaborn  
- **Machine Learning:** Scikit-learn  
- **Environment:** Google Colab  

## Repository Structure
```text
student-exam-success-prediction/
│
├── notebook/
│   └── student_exam_prediction.ipynb
├── data/
│   └── student_exam_success_unclean_dataset.csv
├── images/
│   ├── ConfusionMatrix.png
│   ├── FeatureCorrelationMatrix.png
│   ├── FeatureImportance.png
│   ├── MissingDataVisualization.png
│   └── StudyHoursPerWeek.png

```
## Conclusion

This project demonstrates how data science techniques can be applied to educational data to predict student success. Key factors such as attendance, study habits, sleep, stress, and previous academic performance strongly influence outcomes. Future improvements could include testing additional machine learning models, hyperparameter tuning, and analyzing real-world datasets for more actionable insights.
