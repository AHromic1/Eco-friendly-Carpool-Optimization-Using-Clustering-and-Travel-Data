# Eco-friendly Carpool Optimization Using Clustering and Travel Data

## Introduction

This project aims to design and implement a data-driven system for optimizing carpool groups to reduce both travel costs and CO₂ emissions. Using simulated mobility data inspired by university staff trips, the project applies machine learning clustering algorithms (KMeans and AGNES) with a custom Gower distance metric to group travelers based on route, timing, and vehicle attributes. After clustering, an optimization phase matches users into carpool groups considering vehicle capacities and travel schedules, including substituting car trips with train journeys when beneficial. 

## Methodologies

- **Data simulation:** Synthetic datasets modeled after real university travel data containing missions, passengers, and vehicle CO₂ emission rates.
- **Data preprocessing:** OneHotEncoding of categorical features, scaling and standardization of numerical variables.
- **Clustering:** Application of KMeans and AGNES clustering with Gower distance to handle mixed data types.
- **Optimization:** Formation of carpool groups within clusters based on route, temporal proximity, and vehicle capacity, with travel mode switching for efficiency.
- **Evaluation:** Use of silhouette scores, PCA visualization, and comparative analysis against a greedy baseline.

## Conclusion

The project successfully demonstrated the potential of clustering-based carpool optimization to reduce emissions and costs, with AGNES clustering (n=30) achieving up to 61% reduction in CO₂ emissions and 62.5% cost savings compared to a greedy baseline. The approach balances environmental sustainability and economic feasibility, while also identifying trade-offs in group coverage. The scalable architecture supports future work on real-world data and user-facing applications.

## Authors

- Nerma Kadrić  
- Azra Žunić  
- Nadina Miralem  
- Amina Hromić  

## Mentorship

- Professor Philippe Canalda  
- Anna Joliot

## Affiliated Universities

- University of Marie and Louise Pasteur  
- University of Sarajevo


## Repository Contents

## Repository Contents

- `Dataset/` — All input data used in clustering and optimization 
- `Images/` — Screenshots of PCA plots, silhouette visualizations, and evaluation charts
- `Results/` — Optimized outputs saved as CSV files for each experiment
- `Eco_friendly_Carpool_Optimization_Using_Clustering_and_Travel_Data.ipynb` — Main notebook implementing preprocessing, clustering, optimization, and evaluation  
- `Simulating_data.ipynb` — Notebook for generating synthetic datasets  
- `Developer's guide.pdf` — Short guide explaining how to use the notebooks and replicate the results  
- `README.md` — This documentation file

- `Eco_friendly_Carpool_Optimization_Using_Clustering_and_Travel_Data.ipynb` — main notebook implementing preprocessing, clustering, optimization, and evaluation  
- `Simulating_data.ipynb` — notebook for generating synthetic datasets  
- `Developer's guide` — a short guide explaining how to use the two Colabs in order to replicate the obtained results.  
- `requirements.txt` — List of required Python packages  

## Getting Started
Clone this repository:

```bash
git clone https://github.com/ahromic1/Eco-friendly-Carpool-Optimization-Using-Clustering-and-Travel-Data.git
cd Eco-friendly-Carpool-Optimization-Using-Clustering-and-Travel-Data
```
use the CSV files provided in the Dataset/ folder: allmissions.csv, personsnew.csv, co22.csv.

Note: If you do not have the datasets, they can be generated using the Simulating_data.ipynb notebook included in this repository.

Open Eco_friendly_Carpool_Optimization_Using_Clustering_and_Travel_Data.ipynb in Google Colab or Jupyter Notebook. This notebook contains the main implementation of the clustering and optimization pipeline.

Run the notebook cells sequentially to perform data preprocessing, clustering, optimization, and results visualization.

For more detailed instructions on usage, environment setup, and data requirements, please refer to the Developer's Guide included in the project.

### Prerequisites

- Python 3.8 or higher  
- Required Python libraries:
  pandas, numpy, scikit-learn (specifically StandardScaler, OneHotEncoder, silhouette_score, PCA, KMeans, AgglomerativeClustering), matplotlib, seaborn, scipy, warnings (built-in), os (built-in), datetime (built-in).
- To install the rewuired libraries:  
  ```bash
  pip install pandas numpy scikit-learn matplotlib seaborn scipy gower


