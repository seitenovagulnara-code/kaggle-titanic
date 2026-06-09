# Kaggle Titanic — Machine Learning from Disaster

## Username
seitenovagulnara-code | gyesserg01EDU Astana_06_2026

## Project Description
Predicting Titanic survival using Machine Learning.
Binary classification task: predict whether a passenger
survived (1) or not (0).

## Feature Engineering
The following features were created or transformed:

- **Title** — extracted from passenger Name
  (Mr, Mrs, Miss, Master, Rare)
- **FamilySize** — SibSp + Parch + 1
- **IsAlone** — 1 if passenger travelled alone
- **Has_Cabin** — 1 if cabin number exists
- **Deck** — extracted first letter from Cabin

Key insights:
- Sex, Title and Fare are the strongest predictors
- Children (Age < 10) had higher survival rate
- Passengers travelling alone survived less
- Cabin presence indicates higher class passenger

## Model
- Algorithm: Random Forest Classifier
- Hyperparameter tuning: GridSearchCV (cv=5)
- Best parameters:
  - max_depth: 6
  - max_features: sqrt
  - min_samples_leaf: 2
  - n_estimators: 300

## Results
- CV Score (GridSearchCV): 82.6%
- Kaggle Leaderboard Score: TBD

## How to Run

### Step 1 — Create virtual environment:
```bash
python3 -m venv titanic_env
```

### Step 2 — Activate:
```bash
source titanic_env/bin/activate
```

### Step 3 — Install dependencies:
```bash
pip install -r requirements.txt
```

### Step 4 — Launch Jupyter Lab:
```bash
jupyter lab
```

### Step 5 — Open and run:

git remote add github https://github.com/seitenovagulnara-code/kaggle-titanic.git

git push github main
