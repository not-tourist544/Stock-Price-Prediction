# 📈 Predicting Stock Prices using LSTM-CNN Model

![Project Banner](./assets/banner.jpg)

Welcome to the repository for the **Deep Learning Project** on stock price prediction using a **Feature Fusion LSTM-CNN Model**. This project is based on the research paper [*"Forecasting Stock Prices with a Feature Fusion LSTM-CNN Model Using Different Representations of the Same Data"*](#). 

---

## 🌟 Abstract

This project implements and evaluates a hybrid **LSTM-CNN model** for forecasting stock prices. By fusing **textual and numerical data**, the model captures intricate patterns in the data, leading to potentially enhanced predictive performance. The report explores the impact of different data representations on stock price forecasting accuracy.

---

## 🧐 Key Features

- **Replicated LSTM-CNN Architecture**: Adheres closely to the architecture proposed in the research paper.
- **Diverse Data Representations**: Explored the impact of stock, candlestick, line bar, and fused line bar data.
- **Comprehensive Visualizations**: Includes price trends, daily changes, volume, SMA crossovers, and candlestick charts.
- **Fusion Model Refinement**: Performance enhancements with added dense layers, adjusted learning rates, and activation functions.

---

## 🛠️ Implementation

### 🔑 Data Preparation

| Feature         | Description                     |
|------------------|---------------------------------|
| **Dataset**      | Includes `Time`, `High`, `Low`, `Open`, `Close`, `Volume`, `Count`. |
| **Data Splits**  | Training: 68,800 | Validation: 10,000 | Testing: 19,474 |
| **Preprocessing**| Standardization, Scaling, and Feature Engineering. |

### 📊 Models

#### 1. **LSTM Model**
![LSTM Architecture](./assets/lstm_model.jpg)

- **Architecture**: Single LSTM layer with 64 units followed by dense layers.
- **Evaluation Metrics**: 
  - Loss: `1.2461`
  - MAPE: `5.43%`
  - RMSE: `1.1163`

#### 2. **SC-CNN Model**
![SC-CNN Architecture](./assets/sc_cnn_model.jpg)

- **Architecture**: Conv1D layer, MaxPooling, Flatten, and Dense layers.
- **Evaluation Metrics**:
  - Loss: `0.0416`
  - MAPE: `5.44%`
  - RMSE: `0.2040`

#### 3. **Fusion Model**
![Fusion Model Architecture](./assets/fusion_model.jpg)

- **Inputs**: Stock and candlestick bar time series.
- **Challenges**: Initial loss values were high, requiring refinement.
- **Post-Refinement**: 
  - Loss reduced significantly (e.g., from `39900.3945` to `31920.3156`).

---

## 📈 Data Visualization

![Data Visualization](./assets/data_visualization.jpg)

- **Price Plot**: Historical performance of the stock.
- **Daily Change and Volume**: Market dynamics.
- **SMA Crossovers**: Technical analysis insights.
- **Candlestick Charts**: Trends and volatility.

---

## 🔍 Results

### Initial Findings:
- **LSTM Model**: Strong predictive performance with a low loss of `1.2461`.
- **SC-CNN Model**: Outperformed LSTM with a minimal loss of `0.0416`.
- **Fusion Model**: High initial loss values identified areas for refinement.

### Post-Refinement:
- Overall Fusion Model loss reduced to `31920.3156`.

---

## 🔧 Recommendations

1. Investigate and address high loss in the Fusion Model.
2. Explore alternative fusion techniques and architectures.
3. Perform additional feature engineering for enhanced predictive accuracy.

---

## 📜 Conclusion

The project successfully replicated and extended the research findings, demonstrating the potential of hybrid models for stock price forecasting. While individual models showed strong performance, ongoing refinements in the Fusion Model highlight the importance of precision and experimentation in financial data prediction.

---

## 📬 Contributors

| Name               | Contribution                                               |
|---------------------|-----------------------------------------------------------|
| **R. Sanaatan**    | Replication of research paper, individual models, data visualization, experimentation, and summary. |
| **Bodhisattwa Dhara** | Refinement, architecture evaluation, and comparative analysis. |

---

## 📂 Repository Structure

```plaintext
├── assets/                   # Images and visualizations
├── data/                     # Dataset (if applicable)
├── models/                   # Model architectures and training scripts
├── notebooks/                # Jupyter Notebooks for experiments
├── results/                  # Evaluation metrics and plots
└── README.md                 # Project Documentation
