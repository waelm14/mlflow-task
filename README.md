# MLOps Task: ML Experiment Tracking with MLflow

## 1. Description
This project demonstrates experiment tracking using MLflow for a House Price Prediction model. Multiple runs with different hyperparameters are logged and compared, and the best model is selected based on RMSE.

## 2. How to Run

1. **Create and activate a virtual environment:**
```bash
   python3 -m venv mlops-env
   source mlops-env/bin/activate
```
   On Windows:
```bash
   mlops-env\Scripts\activate
```

2. **Install dependencies:**
```bash
   pip install -r requirements.txt
```

3. **Start the MLflow UI server:**
```bash
   mlflow ui
```

4. **Run the training script (in a separate terminal with the environment activated):**
```bash
   python train.py
```

5. **View the results:** Open `http://127.0.0.1:5000` in your web browser.

## 3. Experiment Comparison Table

| Run Name | Max Depth | Learning Rate | RMSE | MAE | R² |
|----------|-----------|---------------|------|------|------|
| Run 1 | 3 | 0.1 | 0.54 | 0.37 | 0.78 |
| **Run 2 (Best)** | **5** | **0.05** | **0.52** | **0.36** | **0.79** |
| Run 3 | 7 | 0.01 | 0.70 | 0.53 | 0.63 |

## 4. Selected Best Model

- **Selected Model:** Run 2
- **Why?** Run 2 achieved the lowest **RMSE (0.52)** and the highest **R² (0.79)** among all runs. Since RMSE is the primary metric for model selection in this task, Run 2 provides the best predictive performance and generalization balance on the validation dataset.

## 5. MLflow UI Screenshots

![MLflow Runs List](screenshots/runs.png)
![MLflow Run Comparison](screenshots/comparison.png)