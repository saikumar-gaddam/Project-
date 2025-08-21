# AI-Driven Climate Change Model

## Overview
This Jupyter Notebook performs an analysis of global land average temperature data from 1900 onwards, sourced from the "Climate Change: Earth Surface Temperature Data" dataset (likely from Kaggle). The analysis includes:

- Data ingestion and preprocessing (loading CSV, cleaning, filtering to reliable years, and visualization of trends).
- Exploratory Data Analysis (EDA) with visualizations.
- Model performance comparison using metrics like MAE (Mean Absolute Error) and RMSE (Root Mean Squared Error) for various forecasting models:
  - Linear Regression
  - ARIMA
  - Prophet
  - LSTM (Long Short-Term Memory neural network)
  - Random Forest (referencing Wang et al.)
  - BPNN (Backpropagation Neural Network, referencing Vidal et al.)

The notebook culminates in a bar chart comparing MAE values across these models to benchmark against recent literature.

The goal is to explore temperature trends and evaluate predictive models for climate forecasting.

## Dataset
- Source: `/kaggle/input/climate-change-earth-surface-temperature-data/GlobalTemperatures.csv` (assumed to be from Kaggle or similar).
- Key columns used: `dt` (date) and `LandAverageTemperature`.
- Data filtered to years >= 1900 for reliability.
- Preprocessing: Date conversion, sorting, handling missing values.

## Requirements
The notebook relies on the following Python libraries (install via `pip` if needed):

- pandas (>=2.0)
- numpy (>=1.20)
- matplotlib (>=3.5)
- scikit-learn (>=1.0) – for metrics like MAE, RMSE, and models like LinearRegression
- tensorflow (>=2.0) – for LSTM model
- statsmodels – implied for ARIMA (though not explicitly imported in visible code)
- prophet – for Prophet model (install via `pip install prophet`)
- warnings (standard library)

Full import list from the notebook:
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.metrics import mean_absolute_error, mean_squared_error, confusion_matrix, roc_curve, auc
from sklearn.preprocessing import MinMaxScaler
import tensorflow as tf
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import LSTM, Dense, Dropout
import warnings
from sklearn.linear_model import LinearRegression
import seaborn as sns
```

**Environment Notes:**
- Python 3.12+ (as per execution metadata).
- Tested on Kaggle (with GPU accelerator enabled).
- No additional package installations are performed in the notebook (assumes pre-installed in environment like Kaggle).

## How to Run
1. **Download the Notebook:** Save the provided `.ipynb` file.
2. **Dataset Setup:** Ensure the dataset CSV is available at the path `/kaggle/input/climate-change-earth-surface-temperature-data/GlobalTemperatures.csv`. If running locally, adjust the path in the notebook.
3. **Install Dependencies:** Run `pip install -r requirements.txt` (create one based on the list above if needed).
4. **Open in Jupyter:** Use Jupyter Notebook or JupyterLab:
   ```
   jupyter notebook saikumar-new-climateanalysis.ipynb
   ```
5. **Execute Cells:** Run cells sequentially (Shift+Enter). The notebook is stateful, so order matters.
6. **Outputs:** Expect plots (e.g., temperature trends and MAE comparison bar chart) and printed data summaries.

**Notes on Execution:**
- The notebook sets a random seed (`np.random.seed(42)`) for reproducibility.
- Suppresses warnings with `warnings.filterwarnings("ignore")`.
- If running on Kaggle, enable internet and GPU for TensorFlow.

## Results
- **Temperature Trend Visualization:** A line plot showing monthly global land average temperatures from 1900.
- **Model Comparison:** Bar chart of MAE values:
  - LinearReg: 3.76
  - ARIMA: 0.29
  - Prophet: 0.23
  - LSTM: 0.52
  - Random Forest (Wang et al.): 0.018
  - BPNN (Vidal et al.): 0.0033
- RMSE values are partially provided (e.g., missing for Random Forest).
- Lower MAE/RMSE indicates better performance; literature models (e.g., BPNN) outperform some implemented ones.

## Limitations
- The notebook appears truncated in the provided content (e.g., full model implementations for ARIMA, Prophet, etc., may not be visible).
- Assumes access to Kaggle dataset; local runs require manual data download.
- No hyperparameter tuning or full cross-validation shown in visible cells.
- Comparisons reference external papers (Wang et al., Vidal et al.) – verify citations for context.

## Contributing
This is a standalone analysis notebook. Fork and modify as needed. For issues, check library versions or dataset integrity.

## License
MIT License (assumed; adjust as per original author). Dataset may have its own terms (e.g., public domain via Kaggle).

*Last Updated: August 21, 2025*

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

