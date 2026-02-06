# Analyse de sentiments et de réclamations avec BERT

## Présentation du projet

Ce projet a pour objectif d’analyser et de classifier des réclamations de consommateurs à partir de leur description textuelle en utilisant le modèle **BERT (Bidirectional Encoder Representations from Transformers)**.

Les données utilisées proviennent de la **Consumer Complaint Database** du **CFPB (Consumer Financial Protection Bureau)**, une agence gouvernementale américaine chargée de la protection des consommateurs contre les pratiques financières déloyales.

L’objectif final est de prédire automatiquement le **type de problème (Issue)** associé à une réclamation à partir du texte libre **Consumer complaint narrative**.

---

## Contexte

Chaque semaine, le CFPB collecte des milliers de réclamations déposées par des consommateurs à l’encontre d’institutions financières.  
Ces réclamations sont ensuite transmises aux entreprises concernées afin d’obtenir une réponse.

La base de données contient :
- des informations catégorielles (produit, entreprise, État, etc.)
- des descriptions textuelles libres des problèmes rencontrés par les consommateurs

L’analyse automatique de ces textes permet :
- d’identifier rapidement les problèmes récurrents
- d’améliorer la réactivité du service client
- de faciliter la prise de décision pour les institutions financières

---

## Objectifs du projet

- Explorer et comprendre la structure de la base de données
- Nettoyer et préparer les données textuelles
- Analyser la répartition des types de réclamations
- Mettre en place un modèle de **classification de texte avec BERT**
- Prédire le problème associé à une réclamation à partir de sa description

---

## Données

- **Source** : Consumer Complaint Database (CFPB)
- **Nombre d’observations** : 89 793
- **Nombre de variables** : 18

### Variables principales utilisées

| Variable | Description |
|--------|-------------|
| Consumer complaint narrative | Description textuelle de la réclamation (entrée du modèle) |
| Issue | Type de problème associé à la réclamation (label) |

---

## Démarche méthodologique

### 1. Manipulation et exploration des données
- Importation des données depuis Google Drive
- Analyse des dimensions du dataset
- Vérification des types de variables
- Analyse des valeurs manquantes
- Étude de la distribution de la variable cible (*Issue*)

### 2. Prétraitement des données textuelles
- Conversion en minuscules
- Suppression des caractères spéciaux et ponctuations
- Suppression des mots vides (*stopwords*)
- Nettoyage appliqué uniquement aux variables utiles au modèle

### 3. Analyse exploratoire
- Analyse de la fréquence des différents types de réclamations
- Visualisation de la distribution des catégories
- Sélection d’un sous-échantillon pour l’entraînement du modèle

### 4. Modélisation avec BERT
- Utilisation de BERT pour la classification de texte
- Encodage des textes avec un tokenizer BERT
- Entraînement du modèle sur les réclamations
- Évaluation des performances

---

## Technologies utilisées

- **Python**
- **Pandas / NumPy** : manipulation des données
- **Matplotlib / Seaborn** : visualisation
- **NLTK** : prétraitement du texte
- **Transformers (Hugging Face)** : modèle BERT
- **PyTorch** : entraînement du modèle
- **Google Colab** : environnement d’exécution

---

## Résultats attendus

- Un modèle capable de prédire automatiquement le type de problème d’une réclamation
- Une meilleure compréhension des réclamations les plus fréquentes
- Une base solide pour une application de NLP dans le domaine financier

---

## Améliorations possibles

- Utilisation de modèles BERT spécialisés (FinBERT)
- Gestion du déséquilibre des classes
- Ajout d’une étape de lemmatisation
- Déploiement du modèle via une API
- Analyse temporelle des réclamations

---

## Auteur

**TIMITE Abdoul – EQUADE**

Projet réalisé dans le cadre d’une étude en **Data Science / NLP**.
