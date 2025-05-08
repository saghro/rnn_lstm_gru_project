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
1.Créer un environnement virtuel:
