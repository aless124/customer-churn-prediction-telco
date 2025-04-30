# 📊 Customer Churn Prediction - Telco Dataset

Prédiction du churn client (résiliation de contrat) à partir de données d’une entreprise de télécommunications. Ce projet met en œuvre un pipeline complet de machine learning : exploration, préparation des données, modélisation, interprétation, et recommandations business.

---

## 🧠 Objectif

Identifier les clients susceptibles de quitter l’entreprise et comprendre les facteurs influents, afin d’optimiser la rétention.

---

## 📁 Structure du projet

```
customer-churn-prediction-telco/
├── data/
│   ├── raw/                      # Données brutes
│   └── processed/                # Données nettoyées
│
├── notebooks/
│   ├── 01_Exploration.ipynb      # Analyse exploratoire (EDA)
│   ├── 02_Preprocessing.ipynb    # Préparation des données
│   ├── 03_Modeling.ipynb         # Entraînement des modèles
│   ├── 04_Evaluation.ipynb       # Évaluation des modèles
│   └── 05_Interpretation.ipynb   # Interprétation avec SHAP
│
├── src/
│   ├── data_preprocessing.py     # Fonctions de nettoyage
│   ├── modeling.py               # Fonctions de modélisation
│   └── utils.py                  # Outils divers
│
├── outputs/
│   ├── figures/                  # Graphiques générés
│   └── models/                   # Modèles sauvegardés
│
├── requirements.txt              # Dépendances
├── churn_prediction.py           # Script principal (optionnel)
├── README.md                     # Ce fichier
└── .gitignore                    # Fichiers à ignorer par Git

```

---

## 📦 Données

- **Source** : [Telco Customer Churn Dataset (Kaggle)](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Contenu** : Données clients (contrats, services souscrits, données démographiques, usage, paiement...)

---

## 🛠️ Méthodologie

1. **Exploration des données**
   - Analyse statistique
   - Visualisations (distribution des variables, corrélations)

2. **Préparation des données**
   - Traitement des valeurs manquantes
   - Encodage des variables catégorielles
   - Feature engineering

3. **Modélisation**
   - Modèles testés : Logistic Regression, Random Forest, XGBoost
   - Validation croisée, tuning d’hyperparamètres
   - Évaluation : Accuracy, AUC, matrice de confusion

4. **Interprétation**
   - Importance des variables
   - Analyse SHAP pour interprétabilité locale et globale

5. **Recommandations**
   - Stratégies de rétention pour les segments à risque

---

## 📊 Résultats

- **Modèle retenu** : XGBoost
- **AUC** : 0.85
- **Principaux facteurs de churn** : contrat mensuel, absence d'engagement, montant élevé des charges mensuelles

---

## 🧰 Librairies utilisées

- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `scikit-learn`
- `xgboost`
- `shap`
- `jupyter`

---

## 🚀 Lancer le projet

```bash
# Créer un environnement virtuel
python -m venv venv
source venv/bin/activate  # ou venv\Scripts\activate sur Windows

# Installer les dépendances
pip install -r requirements.txt

# Lancer Jupyter
jupyter notebook