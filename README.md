# Diagnosis_of_COVID_19

# 📊 Analyse Exploratoire des Données (Exploratory Data Analysis)

## 🎯 Objectif

- Mieux comprendre la structure et le contenu de notre jeu de données.
  > _"Un petit pas en avant vaut mieux qu’un grand pas en arrière."_
- Élaborer une première stratégie de modélisation.

---

## ✅ Checklist Initiale

### 🔹 Analyse de Forme

- **Variable cible :** `SARS-Cov-2 exam result`
- **Dimensions du jeu de données :** 5644 lignes × 111 colonnes
- **Types de variables :**

  - **Qualitatives :** 70
  - **Quantitatives :** 41
    - `object` : 37
    - `int64` : 4

- **Analyse des valeurs manquantes :**
  - De nombreuses valeurs manquantes
  - Plus de 50 % des variables contiennent plus de 90 % de valeurs manquantes
  - On distingue deux groupes :
    - ~76 % de valeurs manquantes dans les **tests viraux**
    - ~89 % dans les **taux sanguins**

---

### 🔹 Analyse de Fond

#### 🎯 Visualisation de la variable cible

- Environ **10 % de cas positifs** au test SARS-Cov-2

#### 📌 Compréhension des variables

- **Variables continues :**
  - Standardisées
  - Distribution asymétrique (skewed)
  - Majoritairement issues d’**analyses sanguines**
- **Âge (quantile) :**

  - Donnée difficile à interpréter
  - Il pourrait s'agir de tranches d’âge (ex. : 0-5), ou d'une transformation mathématique inconnue
  - Le jeu de données ne précise pas la signification exacte
  - Toutefois, ce n’est pas un élément bloquant à ce stade

- **Variables qualitatives :**
  - Principalement **binaires** (0 ou 1)
  - Exemple notable : **Rhinovirus** semble très fréquent

---

### 🔍 Relations entre Variables et la Cible (`target`)

- **Target vs. Tests sanguins :**

  - Certaines variables comme **Monocytes**, **Plaquettes**, et **Leucocytes** montrent un lien possible avec le COVID-19  
    → **Hypothèse à tester**

- **Target vs. Âge :**

  - Les individus jeunes semblent moins affectés
  - ⚠️ L’âge réel n’est pas connu, ni la période de collecte des données
  - Si les individus jeunes sont des enfants, cela pourrait contredire certaines observations scientifiques actuelles
  - → À surveiller : variable potentiellement utile **en combinaison** avec les résultats des tests sanguins

- **Target vs. Tests viraux :**
  - Les cas de **co-infection virale** sont rares
  - Exemple : patients **positifs au Rhinovirus/Enterovirus** sont souvent **négatifs au COVID-19**  
    → Hypothèse à approfondir (peut-être une épidémie régionale concomitante ?)
  - Attention : la co-infection par plusieurs virus est tout à fait possible
  - **Conclusion :** Ces observations ne permettent pas à elles seules de conclure à une relation directe avec le COVID-19

---

## 🧠 Remarques Générales

- De nombreuses hypothèses émergent de cette première analyse.
- La qualité et la clarté des métadonnées du dataset sont limitées.
- Des tests statistiques et une modélisation sont nécessaires pour confirmer ou infirmer les corrélations suspectées.

---
