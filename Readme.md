# AI-Driven Climate Change Model

A master's research project developed under the University of Hertfordshire's School of Physics, Engineering and Computer Science for module 7COM1039.

This project leverages Artificial Intelligence (AI) to forecast temperature trends, classify climate risks, and provide explainable insights using SHAP and LIME.

## Project Overview

Climate change is one of the most urgent global challenges. This project builds an AI-powered climate model to:
- Predict temperature changes
- Classify risk levels (Low, Moderate, High, Extreme)
- Explain model behavior using SHAP and LIME
- Simulate future climate risk under different CO₂ emission scenarios

## Objectives

- Build regression models to predict average temperature
- Train classifiers to categorize climate risk
- Use SHAP and LIME for model explainability
- Perform scenario-based forecasting
- Provide reproducible results via Google Colab

## Research Questions

1. How effectively can AI models (Random Forest, LSTM, Transformer) predict temperature based on climate indicators?
2. What are the most influential features driving climate predictions?
3. How can explainable AI techniques improve transparency in climate modeling?

## Dataset Details

Dataset Source: Kaggle Climate Change Dataset by Bhadra Mohit  
Total Samples: 1,000 rows × 10 columns  
License: Public domain

Selected Features:
- CO₂ Emissions (Tons/Capita)
- Sea Level Rise (mm)
- Rainfall (mm)
- Population
- Renewable Energy (%)
- Severe Meteorological Events
- Forest Area (%)

Target Variables:
- Average Temperature (°C) — for regression
- Risk Category (Low–Extreme) — for classification

## Tools and Libraries

| Purpose            | Tools Used                                      |
|--------------------|-------------------------------------------------|
| Data Handling      | pandas, numpy                                   |
| ML Models          | RandomForest, GradientBoosting, XGBoost         |
| Deep Learning      | LSTM, Transformer (via TensorFlow/Keras)        |
| Explainability     | SHAP, LIME                                      |
| Visualization      | matplotlib, seaborn, plotly                     |
| IDE                | Google Colab (Primary Notebook)                 |

## Key Outcomes

- Regression model with high R² score for temperature prediction
- Classifier to label regions by climate risk
- SHAP and LIME visualizations for feature influence
- Scenario-based insights for climate forecasting
- Reproducible Colab Notebook

## Project Structure


## References

- Agrawal (2023). Organizational sustainability of generative AI-Driven optimization intelligence. https://doi.org/10.1080/08874417.2023.2286540  
- Amiri et al. (2024). Comprehensive survey of AI for climate change mitigation. https://doi.org/10.1016/j.energy.2024.132827  
- Chakraborty et al. (2021). XAI for energy modeling. https://doi.org/10.1016/j.apenergy.2021.116807  
- Cavus et al. (2025). AI in predictive maintenance for EVs. https://doi.org/10.3390/en18051041  
- Chang & Kidman (2023). Ethics of AI in environmental education. https://doi.org/10.1080/10382046.2023.2194036

## Acknowledgements

- Supervisor: (Add your supervisor's name)  
- University of Hertfordshire  
- Kaggle for dataset provisioning

## Contact

Author: Sai kumar Gaddam 
Email: saikumargaddam949@gmail.com
Student ID: 23100456  
