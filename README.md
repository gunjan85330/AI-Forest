# AI-FOREST: A Generative AI-Powered Wildfire Prediction, Simulation, and Risk Assessment System

## Project Overview
Wildfires cause devastating ecological and economic losses worldwide. Traditional fire prediction methods (like physics-based models) often fail to adapt in real time.  
**AI-FOREST** is a Generative AI-driven system that:
- Predicts wildfire occurrence using machine learning models.
- Simulates fire spread under different conditions.
- Generates synthetic data for improved training.
- Visualizes fire risk maps for disaster management teams.

This repository contains the **data preprocessing, grid creation, weather data integration, and machine learning pipeline** for wildfire prediction in **Uttarakhand, India**.

## Repository Structure
AI-FOREST/
│── data/ # raw datasets (NASA FIRMS, weather, etc.)
│── notebooks/ # Jupyter notebooks (preprocessing, grid, weather fetching, modeling)
│── src/ # Python scripts (helper functions, reusable code)
│── outputs/ # cleaned datasets, processed files, prediction results
│── README.md # project overview (this file)
│── requirements.txt # dependencies



## Dataset Sources
- **NASA FIRMS (Fire Information for Resource Management System)**  
  Provides satellite-detected fire locations, brightness, and timing.  
  [Link](https://earthdata.nasa.gov/firms)

- **Open-Meteo ERA5 Reanalysis Data**  
  Historical weather data: temperature, precipitation, humidity, windspeed.  
  [Link](https://open-meteo.com/)


## Methodology (What We Did)
1. **Data Collection & Cleaning**: Downloaded FIRMS fire data + ERA5 weather data and removed inconsistencies.  
2. **Grid Creation**: Divided Uttarakhand into 10 km × 10 km grid cells.  
3. **Weather Data Fetching**: Mapped daily weather to each grid cell.  
4. **Fire Aggregation**: Labeled whether a fire occurred in each cell on each day.  
5. **Dataset Preparation**: Structured data so that yesterday’s weather predicts today’s fire.  
6. **Model Training**: Trained Logistic Regression and Random Forest classifiers.  
7. **Balancing**: Used oversampling (ROS/SMOTE) to handle class imbalance.  
8. **Prediction & Visualization**: Generated fire risk maps with Plotly.

---

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/AI-FOREST.git
   cd AI-FOREST

2. Install dependencies:
   pip install -r requirements.txt

3. Open Jupyter Notebook:
   jupyter notebook

4. Run notebooks in /notebooks to preprocess data, train models, and generate maps

Example Output

Heatmaps showing wildfire risk zones in Uttarakhand.

Model metrics (ROC-AUC, Precision, Recall).

Predictions saved in /outputs/predictions.csv.

Team Members

Gunjan Singh

Harshvardhan Singh 

Muskan Khandelwal 

Bhupendra Singh 

Mentor

Mr. Shubham Singhal


