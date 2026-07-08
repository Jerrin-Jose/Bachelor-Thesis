# Vorhersage von Verletzungsrisiken im Profifußball auf Basis von Spielerleistungs- und Belastungsdaten — Eine ML-basierte Analyse

**Bachelor Thesis — Jerrin Jose**  
Westfälische Hochschule Gelsenkirchen | B.Sc. Informatik  
Supervisor: Prof. Sebastian Büttner

---

## Research Question
Which player, performance and load characteristics are 
associated with injury risk in professional football — 
and how accurately can this risk be predicted using ML?

---

## Dataset
- Kaggle injury dataset (kolambekalpesh) — 1,301 player-season records
- Transfermarkt appearances (dcaribou) — CC0 license
- Combined: 1,301 rows × 40 features, 604 players, Premier League 2016–2020

---

## Methods
- Logistic Regression (baseline)
- Random Forest
- XGBoost
- SMOTE for class imbalance (training only)
- TreeSHAP for explainability
- 5-fold stratified cross-validation

---

## Results

| Model | ROC-AUC | F1 | Recall | Precision |
|---|---|---|---|---|
| Logistic Regression | 0.694 ± 0.018 | 0.736 | 0.673 | 0.817 |
| Random Forest | 0.699 ± 0.012 | 0.814 | 0.852 | 0.780 |
| XGBoost | 0.687 ± 0.035 | 0.814 | 0.848 | 0.785 |

**Top SHAP Features:**
1. season_games_played
2. cumulative_days_injured
3. season_minutes_played
4. position_numeric
5. age

---

## Repository Structure
├── thesis_pipeline.ipynb  ← complete pipeline
├── dataset.csv            ← combined dataset (not tracked)
├── results/               ← plots and metrics
├── requirements.txt
└── README.md


## Viewing Results

> 💡 All results and plots are pre-rendered and visible 
> directly on GitHub by clicking thesis_pipeline.ipynb — 
> no installation required for viewing.
> Installation only needed to re-run the pipeline.

---