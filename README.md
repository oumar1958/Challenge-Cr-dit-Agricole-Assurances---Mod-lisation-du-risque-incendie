# Challenge Data Science - Prédiction des Risques Incendie Agricoles

## Description du Projet
Ce projet vise améliorer la modélisation du risque incendie dans les contrats Multirisque Agricole. Le but est de développer des modèles de prédiction plus performants que les GLM standards utilisés actuellement.



## Objectif
Prédire la prime pure incendie en développant deux modèles distincts :
1. Un modèle pour la Fréquence des sinistres
2. Un modèle pour le Coût moyen des sinistres

La variable cible finale (CHARGE) est calculée par : CHARGE = FREQ × CM × ANNEE_ASSURANCE

## Structure des Données
### Variables Cibles
- FREQ : Fréquence des sinistres
- CM : Coût moyen des sinistres
- CHARGE : Charge totale (variable cible finale)

### Variables Explicatives
1. **Données Géographiques**
   - Département
   - Données météorologiques

2. **Données Contractuelles**
   - Activité de l'assuré (cultivateur, polyculteur, etc.)
   - Indicateurs de souscription des garanties
   - Nombre de bâtiments
   - Nombre de salariés
   - Historique des sinistres

3. **Données de Surface**
   - Surfaces des bâtiments (anonymisées : surface1, surface2, etc.)
   - Surface d'exploitation
   - Surface d'élevage

4. **Données de Capitaux**
   - Capitaux assurés (anonymisés : capital1, capital2, etc.)
   - Options de garantie (vol, serres, etc.)

5. **Données de Prévention**
   - Équipements de sécurité (extincteurs, etc.)
   - Caractéristiques des structures (matériaux, etc.)
   - Indicateurs de prévention (anonymisés : prev1, prev2, etc.)

## Benchmark
Le benchmark utilise deux GLM standards :
1. **Fréquence**
   - Distribution : Poisson
   - Fonction de lien : Log

2. **Coût Moyen**
   - Distribution : Tweedie
   - Fonction de lien : Log

## Métrique d'Évaluation
- **RMSE (Root Mean Square Error)**
- Formule : RMSE = √(1/n * Σ(yᵢ - ŷᵢ)²)
- Où :
  - yᵢ : valeur réelle
  - ŷᵢ : valeur prédite
  - n : nombre d'observations

## Critères de Performance
1. Précision des prédictions
2. Interprétabilité des modèles
3. Efficacité computationnelle
4. Respect des contraintes métier

## Fichiers Disponibles
- x_train : Variables explicatives pour l'entraînement
- y_train : Variables cibles pour l'entraînement
- x_test : Variables explicatives pour le test
- Exemple de soumission aléatoire
- Documentation supplémentaire


## Auteur
Oumar Abdramane ALLAWAN
