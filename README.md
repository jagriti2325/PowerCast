# PowerCast: Power Consumption Prediction

## Overview

**PowerCast** is an advanced machine learning project designed to accurately predict electricity power consumption using multiple predictive models and interactive Power BI visualizations. The project combines data science, statistical analysis, and business intelligence to provide actionable insights into power consumption patterns and trends.

This repository contains both the analytical notebook (PowerCast.ipynb) for exploratory data analysis and a production-ready Power BI dashboard for stakeholder reporting and decision-making.

---

## Project Objectives

- **Predict Power Consumption**: Build and compare multiple ML models to accurately forecast electricity consumption
- **Model Optimization**: Evaluate and rank different algorithms to identify the best-performing model
- **Data Insights**: Uncover patterns, trends, and anomalies in power consumption data
- **Interactive Reporting**: Provide intuitive visualizations and dashboards for business stakeholders
- **Decision Support**: Enable data-driven decision-making for energy management and optimization

---

## Key Results & Findings

### 🏆 Model Performance Comparison

Our comprehensive analysis evaluated three state-of-the-art machine learning models:

| Model | MAE | Performance | Recommendation |
|-------|-----|-------------|-----------------|
| **XGBoost** | **241.15** | ⭐⭐⭐⭐⭐ Excellent | **Primary Model** |
| Random Forest | 247.89 | ⭐⭐⭐⭐ Good | Alternative/Ensemble |
| LSTM | 337.69 | ⭐⭐⭐ Fair | Not Recommended |

### 📊 Performance Metrics

- **Best Performing Model**: XGBoost
- **Lowest Mean Absolute Error (MAE)**: 241.15
- **Error Improvement**: 2.75% better than Random Forest, 28.4% better than LSTM
- **Model Accuracy**: XGBoost provides optimal balance between accuracy and computational efficiency

### 💡 Key Insights

1. **XGBoost Superiority**: XGBoost consistently outperforms both Random Forest and LSTM models with the lowest prediction error
2. **Gradient Boosting Advantage**: Tree-based ensemble methods prove more effective than deep learning (LSTM) for this time-series dataset
3. **Model Stability**: Random Forest offers a robust alternative with comparable performance (only 2.75% higher error)
4. **Sequential Model Limitations**: LSTM's higher error suggests that the power consumption patterns are better captured by feature-based models rather than pure sequential learning
5. **Prediction Reliability**: XGBoost's MAE of 241.15 indicates highly reliable predictions for practical deployment

### 📈 Data Characteristics

- **Dataset**: powerconsumption.csv
- **Temporal Coverage**: Multi-month electricity consumption records
- **Granularity**: Time-series data with regular intervals
- **Key Variables**: Timestamp, consumption values across different zones
- **Data Quality**: Cleaned and validated for model training

---

## Dashboard Features

### 📱 Power BI Interactive Dashboard

**File**: \Power_Consumption Prediction.pbix
The professional Power BI dashboard provides real-time insights and comprehensive model performance visualization.

#### Dashboard Components

1. **KPI Cards** (Top Section)
   - Best Model: XGBoost
   - Lowest MAE: 241.15
   - XGB MAE: 241.15
   - RF MAE: 247.89
   - LSTM MAE: 337.69

2. **Power Consumption Prediction Comparison**
   - Time-series visualization showing actual vs. predicted values
   - Identifies prediction accuracy across the timeline
   - Reveals consumption patterns and seasonal variations

3. **Model Accuracy Comparison**
   - Visual comparison of the three models
   - Color-coded for easy identification (XGBoost in red, RF in blue, LSTM in mint)
   - Quick visual assessment of relative performance

4. **Model Error Distribution (MAE)**
   - Pie chart showing error distribution across models
   - Percentage breakdown of total prediction error
   - Identifies which model contributes most effectively

5. **Model Error Reduction Analysis**
   - Horizontal bar chart showing error metrics
   - Progressive improvement visualization
   - Highlights ranking and comparative performance

6. **Model Rankings Table**
   - Ranked comparison table with Model, MAE, and Rank columns
   - Detailed metrics for documentation and reporting
   - Easy reference for stakeholders

#### Interactive Features

- **Drill-through capabilities** for deeper analysis
- **Cross-report filtering** for focused investigation
- **Dynamic insights** powered by AI
- **Professional formatting** suitable for executive presentations
- **Export capabilities** for reports and presentations

#### Dashboard Screenshot

![Power Consumption Prediction Dashboard](assets/dashboard-screenshot.png)

*The comprehensive Power BI dashboard showcasing all model performance metrics, visualizations, and key insights at a glance.*
<img width="663" height="624" alt="Screenshot (224)" src="https://github.com/user-attachments/assets/c90504d9-5a21-42b5-a794-c669289bfd1e" />


---

## Technical Architecture

### Models Implemented

#### 1. XGBoost (Recommended)
- **Algorithm**: Extreme Gradient Boosting (tree ensemble)
- **Strengths**: High accuracy, handles non-linear relationships, robust to outliers
- **Performance**: MAE of 241.15 (BEST)
- **Use Case**: Production deployment, real-time predictions

#### 2. Random Forest
- **Algorithm**: Ensemble of decision trees
- **Strengths**: Stable, interpretable, resistant to overfitting
- **Performance**: MAE of 247.89 (GOOD - 2.75% higher than XGBoost)
- **Use Case**: Ensemble voting, baseline comparison

#### 3. LSTM (Long Short-Term Memory)
- **Algorithm**: Recurrent Neural Network
- **Strengths**: Captures sequential dependencies, handles long-term patterns
- **Performance**: MAE of 337.69 (FAIR - 28.4% higher than XGBoost)
- **Use Case**: Educational reference, potential future optimization

---

## Project Structure

\PowerCast/
├── PowerCast.ipynb                    # Main analysis & modeling notebook
├── Power_Consumption Prediction.pbix  # Interactive Power BI dashboard
├── powerconsumption.csv              # Dataset
├── README.md                         # Project documentation
└── requirements.txt                  # Python dependencies
\
---

## Getting Started

### Prerequisites

- **Python 3.7+** (for notebook execution)
- **Jupyter Lab/Notebook** (for running the notebook)
- **Power BI Desktop** (free version available) - for dashboard
- **Required Libraries**: pandas, numpy, matplotlib, seaborn, scikit-learn, xgboost

### Installation

1. **Clone the repository**:
   \\ash
   git clone https://github.com/jagriti2325/PowerCast.git
   cd PowerCast
   \
2. **Create a virtual environment** (recommended):
   \\ash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   \
3. **Install dependencies**:
   \\ash
   pip install pandas numpy matplotlib seaborn scikit-learn xgboost
   \
### Usage

#### Running the Notebook

1. Open PowerCast.ipynb in Jupyter Lab or VS Code:
   \\ash
   jupyter lab PowerCast.ipynb
   \
2. Execute cells sequentially to:
   - Load and explore the dataset
   - Perform data cleaning and preprocessing
   - Train all three models (XGBoost, Random Forest, LSTM)
   - Evaluate model performance
   - Generate visualizations

#### Accessing the Dashboard

1. **Download Power BI Desktop** (free):
   - Visit: https://powerbi.microsoft.com/desktop/

2. **Open the dashboard**:
   - Launch Power BI Desktop
   - Open \Power_Consumption Prediction.pbix   - Connect to data sources if prompted

3. **Interact with visualizations**:
   - Use filters and slicers for dynamic analysis
   - Click on charts for drill-through options
   - Export insights for reports

---

## Data Analysis & Methodology

### Data Preprocessing
- ✅ Timestamp validation and format conversion
- ✅ Missing value detection and handling
- ✅ Outlier identification and treatment
- ✅ Feature engineering and normalization
- ✅ Train-test split (typically 80-20)

### Model Training
- ✅ Hyperparameter tuning for each model
- ✅ Cross-validation for robustness
- ✅ Performance metrics calculation
- ✅ Comparative analysis

### Validation Strategy
- ✅ Multiple evaluation metrics (MAE, RMSE, R²)
- ✅ Temporal validation (time-series specific)
- ✅ Visual inspection of predictions
- ✅ Error distribution analysis

---

## Results Interpretation

### Why XGBoost Wins

1. **Superior Predictive Power**: 241.15 MAE represents the most accurate predictions
2. **Computational Efficiency**: Faster training and inference compared to LSTM
3. **Interpretability**: Feature importance can be extracted for business insights
4. **Robustness**: Handles non-linear relationships and interactions effectively
5. **Scalability**: Suitable for production environments and real-time predictions

### Random Forest as Backup

- Competitive performance with only 2.75% higher error
- Better interpretability than XGBoost
- Recommended for ensemble approaches combining both models

### LSTM Limitations

- Higher error suggests temporal patterns alone don't capture consumption variations
- May benefit from:
  - Architecture improvements (attention mechanisms)
  - Feature engineering enhancements
  - Hyperparameter optimization
  - Longer training sequences

---

## Applications & Use Cases

### 📌 Energy Management
- Real-time power consumption forecasting
- Peak demand prediction for grid management
- Resource allocation optimization

### 💼 Business Intelligence
- Cost prediction and budgeting
- Anomaly detection in consumption patterns
- Zone-wise consumption analysis

### 🔧 Operational Optimization
- Equipment maintenance scheduling
- Load balancing decisions
- Energy efficiency recommendations

---

## Performance Metrics Explained

### Mean Absolute Error (MAE)
- **Definition**: Average of absolute differences between predicted and actual values
- **Unit**: Same as the target variable (power units)
- **Lower is Better**: Indicates more accurate predictions
- **XGBoost MAE**: 241.15 (Excellent)

### Why MAE matters
- Easy to interpret and communicate to stakeholders
- Less sensitive to outliers than RMSE
- Directly represents average prediction error in real units

---

## Future Enhancements

- [ ] Implement ensemble voting combining XGBoost and Random Forest
- [ ] Explore hybrid models (XGBoost + LSTM)
- [ ] Add external features (weather, holidays, day type)
- [ ] Develop real-time prediction API
- [ ] Implement automated retraining pipeline
- [ ] Create zone-wise sub-models for granular predictions
- [ ] Add confidence intervals to predictions
- [ ] Deploy to cloud (Azure, AWS, GCP)

---

## Requirements

### Python Libraries
\pandas>=1.0.0
numpy>=1.18.0
matplotlib>=3.1.0
seaborn>=0.10.0
scikit-learn>=0.22.0
xgboost>=1.3.0
\
### System Requirements
- **For Notebook**: 4GB RAM minimum, 2GB disk space
- **For Power BI**: Windows 10/11 or Power BI Online access

---

## Notes & Best Practices

✅ **Data Preparation**
- Ensure \powerconsumption.csv\ is in the same directory as the notebook
- Validate data integrity before running models
- Check for seasonal patterns in your data

✅ **Model Deployment**
- Retrain models quarterly with new data for optimal performance
- Monitor prediction accuracy in production
- Set up alerts for sudden accuracy drops

✅ **Dashboard Usage**
- Refresh Power BI data connections regularly
- Use the dashboard for executive reporting and KPI tracking
- Customize visuals for specific business requirements

---

## Contributing

Contributions are welcome! Feel free to:
- Report issues and bugs
- Suggest improvements or new features
- Submit pull requests with enhancements
- Share insights and use cases

---

## License

[Add appropriate license information here]

---

## Contact & Support

**Project Owner**: Jagriti Arora  
**Repository**: https://github.com/jagriti2325/PowerCast  
**Last Updated**: March 2026

For questions, issues, or collaboration opportunities, please open an issue on GitHub.

---

## Acknowledgments

- PowerCast leverages industry-standard ML libraries and best practices
- Dashboard built with Microsoft Power BI for professional reporting
- Data-driven insights powered by advanced statistical analysis

---

**PowerCast** - Making Power Consumption Predictions Simple, Accurate, and Actionable. 🚀
