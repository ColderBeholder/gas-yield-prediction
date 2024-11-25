# Prediction of Feed Stream Yields in a Gas Processing Plant

## Overview
![Product Name Screen Shot][product-screenshot]

This project aims to address challenges in gas processing plants related to unmetered pipelines and unreliable data by predicting feed stream yields using advanced machine learning techniques. The project compares multiple regression methods and neural networks to optimize yield prediction and improve production planning.

Code Repository: [gas-yield-prediction](https://github.com/ColderBeholder/gas-yield-prediction)

---

## Objectives
- Predict feed stream yields in gas processing plants.
- Improve accuracy over traditional methods used in the gas industry.
- Address challenges in noisy and inconsistent datasets using machine learning.

---

## Key Features
- **Model Development**: Implemented and compared regression models and neural networks.
- **Data Preprocessing**: Employed the Local Outlier Factor (LOF) algorithm for outlier detection and cleaning.
- **Evaluation Metrics**: Utilized metrics such as R², MSE, RMSE, MAE, and CMAPE to assess model performance.
- **Real-World Application**: Optimized production planning for gas plants with unmetered pipelines.

---

## Methodology
1. **Data Exploration**: Initial exploration using statistical analysis and visualization to identify relationships between inputs and outputs.
2. **Outlier Detection**: Applied LOF to handle noisy data and improve model accuracy.
3. **Modeling**: 
   - Linear regression for baseline results.
   - Decision trees, random forests, and support vector regressors for non-linear relationships.
   - Neural networks with initialized weights from linear regression for enhanced convergence.
4. **Evaluation**: Cross-validation and testing against unseen data to ensure model generalization.

---

## Results
- Linear regression models demonstrated limited accuracy due to the imposed linearity.
- Neural networks achieved superior performance with an R² score of 0.9890 and a CMAPE of 91.16%, significantly outperforming traditional methods.
- The approach demonstrated robust prediction capabilities even with limited and noisy data.

---

## Experimental Setup
- **Environment**: Python 3 with Jupyter Notebook.
- **Libraries Used**: pandas, numpy, matplotlib, scikit-learn, TensorFlow.
- **Dataset**: Daily input-output data from five gas processing plants, recorded from January 2021 to May 2024, with 1236 entries post-cleaning.

---

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/ColderBeholder/gas-yield-prediction.git
   ```
2. Navigate to the project directory:
   ```bash
   cd gas-yield-prediction
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage

This code contains functions\experiments for the following:
- To run your first experiment and obtain your first model, open main.ipynb and choose which plant to try to model (B, S, K, X, Y) and run the notebook. Then different experiments can be tested through tweaking the hyperparameters
- Visualize the data in data_exploration.ipynb through both statistical and visual approaches
- Go through previously run experiments in experiments.ipynb
- Created models are stored in the directory saved_models/
- Custom functions and model can be viewed in utils.py and model.py respectively.

---

## Dataset Description
- **Inputs**: Feed volumes from plants (e.g., Feed B, Feed K, etc.).
- **Outputs**: Product yields (e.g., C1, NGL, Sulphur, Condensate).
- Data spans 2021–2024, with varying features and scales.

---

## Limitations
- Limited dataset with only 1236 entries.
- Missing key variables like temperature and flow rate.
- Model performance might degrade when extrapolated to unseen conditions.

---

## Future Work
- Enrich the dataset with additional features and real-time variables.
- Explore advanced neural network architectures and hybrid models.
- Incorporate time-series analysis for temporal trends.

---

## Contributors
- **Ali Alhebsi**, **Omar Alawadhi**, **Rames Aljneibi**
- Affiliation: Mohamed Bin Zayed University of Artificial Intelligence, Abu Dhabi, UAE


---

## Acknowledgments
Special thanks to the gas company for providing data and domain expertise.


[product-screenshot]: images/screenshot.jpeg
