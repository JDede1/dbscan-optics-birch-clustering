# Assignment 6: DBSCAN, OPTICS, BIRCH Clustering

## Overview
This project builds **unsupervised clustering models** using:
- DBSCAN (Density-Based Spatial Clustering of Applications with Noise)  
- OPTICS (Ordering Points To Identify the Clustering Structure)  
- BIRCH (Balanced Iterative Reducing and Clustering using Hierarchies)  

The models are applied to the **Fatal Police Shootings dataset** to discover hidden patterns and segment victims into clusters.  
We compare clustering methods, visualize results, and interpret findings.

Notebook: 📓 `DBSCAN_OPTICS_BIRCH_Clustering.ipynb`

---

## Dataset
`fatal-police-shootings-data.csv`

### Columns
1. `id` – unique identifier  
2. `name` – victim name  
3. `date` – shooting date  
4. `manner_of_death` – Shot / Shot and Tasered  
5. `armed` – weapon info (undetermined, unknown, unarmed)  
6. `age` – victim age  
7. `gender` – M/F/None  
8. `race` – W, B, A, N, H, O, None  
9. `city` – location  
10. `state` – state code  
11. `signs_of_mental_illness` – True/False  
12. `threat_level` – attack / other / undetermined  
13. `flee` – Foot / Car / Not fleeing  
14. `body_camera` – True/False  

---

## Objectives
- Preprocess and encode categorical variables  
- Apply **DBSCAN** clustering (tune `eps` and `min_samples`)  
- Apply **OPTICS** clustering (compare results to DBSCAN)  
- Apply **BIRCH** clustering with fixed clusters  
- Visualize cluster distributions with seaborn count plots  
- Interpret cluster structures  

---

## Steps to Run

```bash
# Clone repo
git clone git@github.com:JDede1/dbscan-optics-birch-clustering.git
cd dbscan-optics-birch-clustering

# Create virtual environment
python -m venv .venv
.venv\Scripts\Activate   # Windows PowerShell
# OR
source .venv/bin/activate   # Linux/Mac

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook
````

Open `DBSCAN_OPTICS_BIRCH_Clustering.ipynb` and run all cells.

---

## Tools & Libraries

* Python 3
* pandas, numpy
* scikit-learn (DBSCAN, OPTICS, BIRCH)
* matplotlib, seaborn
* Jupyter Notebook

---

## Results

* **DBSCAN** formed density-based clusters with noise points identified.
* **OPTICS** produced similar clusters to DBSCAN but with a better hierarchical view of density reachability.
* **BIRCH** provided centroid-based clusters with reduced complexity.

Visualization of cluster distributions confirmed the cluster assignments, and interpretations revealed unique subgroup patterns.

```

---