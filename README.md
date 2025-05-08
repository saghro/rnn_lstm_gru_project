# rnn_lstm_gru_project
Documentation pour le projet GitHub : RNN-LSTM-GRU Financial Time Series Analysis
Voici un fichier README.md complet pour votre dépôt GitHub qui documente votre projet d'analyse de séries temporelles financières avec RNN, LSTM et GRU.
# Analyse de Séries Temporelles Financières avec RNN, LSTM et GRU

Ce projet implémente et compare trois architectures de réseaux neuronaux récurrents (RNN, LSTM et GRU) pour la prédiction de séries temporelles financières. L'objectif est d'analyser les performances relatives de ces différentes architectures pour la prédiction des prix d'actions.

## 📋 Table des matières
- [Objectifs](#objectifs)
- [Technologies utilisées](#technologies-utilisées)
- [Structure du projet](#structure-du-projet)
- [Modèles implémentés](#modèles-implémentés)
- [Installation](#installation)
- [Utilisation](#utilisation)
- [Résultats](#résultats)
- [Références](#références)

## 🎯 Objectifs

- Comparer les performances des architectures RNN, LSTM et GRU
- Prédire l'évolution des prix des actions (Apple/AAPL)
- Analyser les différences fondamentales entre ces architectures
- Démontrer l'utilité des réseaux récurrents pour l'analyse de séries temporelles

## 🛠️ Technologies utilisées

- **Python 3.13** : Langage de programmation principal
- **PyTorch** : Framework d'apprentissage profond
- **pandas** : Manipulation et analyse de données
- **numpy** : Calcul numérique
- **matplotlib** : Visualisation de données
- **scikit-learn** : Prétraitement et évaluation des modèles
- **yfinance** : Téléchargement de données financières
- **Jupyter Notebook** : Environnement de développement interactif

## 📂 Structure du projet
rnn_project/
│
├── data/                  # Dossier contenant les données boursières
│   └── AAPL_data.csv      # Données historiques d'Apple
│
├── models/                # Dossier contenant les modèles entraînés
│   ├── rnn_model.pth      # Modèle RNN entraîné
│   ├── lstm_model.pth     # Modèle LSTM entraîné
│   └── gru_model.pth      # Modèle GRU entraîné
│
├── results/               # Dossier contenant les résultats et visualisations
│   ├── metrics_comparison.csv           # Métriques d'évaluation des modèles
│   ├── training_losses.png              # Courbes des pertes d'entraînement
│   ├── predictions_comparison.png       # Comparaison des prédictions
│   └── actual_prices_predictions.png    # Prédictions sur les prix réels
│
├── src/                   # Code source du projet
│   ├── config.py          # Configuration du projet
│   ├── data_preparation.py # Préparation des données
│   ├── models.py          # Définition des architectures des modèles
│   ├── training.py        # Fonctions d'entraînement et d'évaluation
│   └── main.py            # Script principal
│
├── RNN_LSTM_GRU_Analysis.ipynb  # Notebook Jupyter pour l'analyse interactive
│
├── requirements.txt       # Dépendances du projet
└── README.md              # Documentation du projet
## 🧠 Modèles implémentés

### RNN (Simple Recurrent Neural Network)
- Architecture de base pour le traitement de séquences
- Adapté pour les dépendances à court terme
- Souffre du problème de disparition du gradient pour les séquences longues

### LSTM (Long Short-Term Memory)
- Conçu pour résoudre le problème de la disparition du gradient
- Utilise des portes d'entrée, de sortie et d'oubli
- Capable de capturer des dépendances à long terme
- Plus de paramètres que le RNN simple

### GRU (Gated Recurrent Unit)
- Version simplifiée du LSTM
- Utilise des portes de mise à jour et de réinitialisation
- Bon compromis entre performances et complexité
- Généralement plus rapide à entraîner que le LSTM

## 🚀 Installation

1. Cloner le dépôt:
```bash
git clone https://github.com/votre-username/rnn-lstm-gru-analysis.git
cd rnn-lstm-gru-analysis
```
2. Créer un environnement virtuel:
```bash

python -m venv rnn_env
source rnn_env/bin/activate  # Sur Windows: rnn_env\Scripts\activate
```
3. Installer les dépendances:
```bash
pip install -r requirements.txt
```
4. Configurer Jupyter pour utiliser l'environnement:
```bash
pip install ipykernel
python -m ipykernel install --user --name=rnn_env --display-name="Python (rnn_env)"
```
📊 Utilisation
Exécution du script principal
```bash
cd src
python main.py
```
Utilisation du notebook Jupyter

1. Lancer Jupyter Notebook:
```bash
 jupyter notebook
```
2. Ouvrir le fichier RNN_LSTM_GRU_Analysis.ipynb
3. Sélectionner le noyau "Python (rnn_env)"
4. Exécuter les cellules une par une

📈 Résultats
Le projet génère plusieurs résultats et visualisations:

Comparaison des métriques: MSE, RMSE, MAE et R² pour chaque modèle
Courbes d'apprentissage: Évolution des pertes pendant l'entraînement
Comparaison des prédictions: Visualisation des prédictions vs. valeurs réelles
Analyse des performances: Comparaison détaillée des trois architectures

📚 Références

Understanding LSTM Networks
PyTorch Documentation
Empirical Evaluation of Gated Recurrent Neural Networks on Sequence Modeling
Financial Time Series Forecasting with Deep Learning

## Fichier requirements.txt

Voici également le contenu du fichier `requirements.txt` à inclure dans votre dépôt:
torch==2.7.0
numpy==2.2.5
pandas==2.2.3
matplotlib==3.10.1
yfinance==0.2.58
scikit-learn==1.6.1
jupyter==1.0.0
ipykernel==6.29.0
## Comment ajouter ces fichiers à GitHub

1. **Créer un nouveau dépôt GitHub** via l'interface web GitHub

2. **Initialiser Git dans votre dossier local**:
```bash
cd rnn_project
git init
```
3. Créer les fichiers README.md et requirements.txt avec le contenu fourni ci-dessus
4. Ajouter tous les fichiers au suivi Git:
```bash
git add .
```
5. Effectuer votre premier commit:
```bash
   git commit -m "Premier commit: implémentation des modèles RNN, LSTM et GRU"
```
6. Lier votre dépôt local au dépôt GitHub:
```bash
  git remote add origin https://github.com/votre-username/rnn-lstm-gru-analysis.git

```
7. Pousser vos modifications:
```bash
git push -u origin main
```






