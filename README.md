# NASA Near-Earth Asteroid Classification: Potentially Hazardous Asteroids (PHA)

Binary classification model to identify potentially hazardous asteroids from NASA's Near-Earth Object dataset.

## Problem Statement

Potentially Hazardous Asteroids are near-Earth objects large enough and close enough to pose collision risk. NASA defines PHAs as objects with:
- Minimum Orbit Intersection Distance (MOID) < 0.05 AU from Earth
- Absolute magnitude H < 22 (diameter roughly >140m)

## Dataset

**Source:** [NASA Near-Earth Asteroids & Close Approaches](https://www.kaggle.com/datasets/darkmatternet/nasa-near-earth-asteroids-and-close-approaches) (Kaggle)

**Size:** 41,281 asteroids  
**Class Distribution:** 94% non-hazardous, 6% potentially hazardous

## Approach

- **Exploratory Analysis:** Examined 15+ orbital and physical features
- **Class Imbalance Handling:** Stratified train/test split, balanced class weights
- **Models:** Logistic Regression (baseline), Random Forest Classifier

## Results

**Random Forest Classifier Performance:**
- Precision: 99%
- Recall: 99%
- ROC-AUC: 0.996

**Feature Importance:**
1. H (absolute magnitude): 59%
2. MOID (minimum orbit intersection distance): 29%
3. q (perihelion distance): 7%

The model successfully learns NASA's existing classification criteria, with H and MOID as primary discriminators.

## Key Insights

- Most orbital elements (eccentricity, semi-major axis, inclination) show minimal separation between hazardous and non-hazardous classes
- Classification boundary is fundamentally simple: large objects (low H) with close approaches (low MOID)
- Identified and removed data leakage from observation arc length, which correlated with hazard status due to tracking prioritization

## Libraries

pandas | numpy | matplotlib | scikit-learn

## Files

- `asteroid_analysis.ipynb` - Full analysis and model training
- `README.md` - Project overview