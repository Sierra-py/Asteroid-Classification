# NASA's Near Earth Asteroid (NEAs) classification of Potentially Hazardous Asteroid (pha).

### What is pha?
Potentially Hazarous asteroids are near-Earth objects that are large enough and have orbits that can bring them close to Earth, posing a risk of significant damage if they were to collide with our planet.

### How does NASA classifies them?
They are conventionally defined as having a minimum orbit intersection distance with Earth of less than 0.05 astronomical units and an absolute magnitude of 22 or brighter, the latter of which roughly corresponds to a size larger than 140 meters.

### Data Source
Kaggle Dataset - [NASA Near-Earth Asteroids & Close Approaches](https://www.kaggle.com/datasets/darkmatternet/nasa-near-earth-asteroids-and-close-approaches)

### Models Trained 
1. Logistics Regression
2. Random Forest 

### Key Findings
Most of the features of the dataset does not contribute in determining the threat level of an asteroid. H and moid does the most of the heavy lifting in determing the pha. The model does not find any new patterns of determining pha but fits the NASA's definition of deining pha.

### Library Used:
* pandas
* numpy
* matplotlib
* sklearn
 