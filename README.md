# Human Activity Recognition from Sensor Data

This project is part of a research challenge to classify **human physical activities** (walking, running, etc.) using accelerometer data from sensors placed on the **lower back** and **right thigh**.

## Highlights
- Sensors: accelerometer data (`back_x,y,z`, `thigh_x,y,z`)
- Task: 8-class classification problem
- Evaluation metric: **Macro F1-score**
- Final validation performance: **0.782 macro-F1**

## Dataset
- `train.csv`: includes sensor data with activity labels  
- `test.csv`: includes sensor data without labels (to predict)  

## Methodology
1. Data preprocessing & handling missing values  
2. Sliding window segmentation (200 samples, stride 50)  
3. Feature extraction (mean, std, min, max, energy per window)  
4. Model training with **Random Forest (balanced class weights)**  
5. Prediction on test set  
6. Export results to `submission.csv`  

## Results
- Validation macro-F1: **0.782**  
- Predictions generated for full test set  

## How to Run
```bash
git clone <repo-url>
cd project
pip install -r requirements.txt
jupyter notebook
```
## Future Work

- Explore deep learning approaches (CNN/LSTM)

- More advanced feature engineering

- Hyperparameter tuning