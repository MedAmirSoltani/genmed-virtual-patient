# 🧬 GenMed — Virtual Patient Generator

> Prototype de génération de données médicales synthétiques multimodales  
## 📌 Contexte

Dans le domaine médical, les données patients sont rares et confidentielles.  
Ce projet propose un pipeline de génération de **patients virtuels complets** —  
des faux patients médicalement cohérents qui n'existent pas, utilisables pour  
entraîner des modèles d'IA sans compromettre la confidentialité.

## 🏗️ Architecture

Le pipeline génère 3 outputs cohérents pour chaque patient virtuel :

| Module | Output | Technologie |
|--------|--------|-------------|
| Module 1 | ECG synthétique | GAN (PyTorch) |
| Module 2 | Données cliniques | Règles statistiques médicales |
| Module 3 | Note clinique | LLM (Groq / LLaMA 3.3 70B) |

## 📊 Dataset

- **MIT-BIH Arrhythmia Database** (PhysioNet/Kaggle)
- 10 000 beats normaux (Classe 0) utilisés pour l'entraînement
- 187 points par beat à 360Hz

## 🚀 Résultats

- GAN convergé en 1500 epochs sur CPU
- ECG synthétiques avec morphologie PQRST réaliste
- Patients virtuels exportés en JSON structuré

## 📁 Structure
