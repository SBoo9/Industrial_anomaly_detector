# ⚙️ Industrial Anomaly Detection System

A robust machine learning-based system designed to detect anomalies in industrial engineering environments. Leveraging Isolation Forests, Autoencoders, and PCA for dimensionality reduction, this project is built to identify system failures early, ensuring safety, efficiency, and predictive maintenance.

---

## 🧠 Overview

This project applies **unsupervised anomaly detection techniques** to multivariate sensor data collected from industrial machines. It enables:
- Early detection of unusual patterns
- Failure prediction before breakdown
- Real-time integration via FastAPI

---

## 📁 Project Structure

```
industrial-anomaly-detection/
├── data/                        # Contains CSV or time-series sensor datasets
├── notebooks/                   # EDA, PCA, model exploration notebooks
├── models/                      # Saved models (Autoencoder, Isolation Forest)
├── src/
│   ├── preprocessing.py         # Data loading, scaling, and cleaning
│   ├── anomaly_isoforest.py    # Isolation Forest model logic
│   ├── anomaly_autoencoder.py  # Autoencoder model training and inference
│   ├── dimensionality.py        # PCA, SVD, UMAP utilities
│   └── api.py                   # FastAPI server
├── requirements.txt
└── README.md
```

---

## 🔍 Features

- 🧪 **Isolation Forest & Autoencoder-based anomaly detection**
- 📉 **PCA** for feature compression and visualization
- 🚀 **FastAPI-based microservice** for real-time anomaly detection
- 📊 **Visualizations** for normal vs anomalous patterns
- 🧰 Modular structure for future ML/DL algorithm integration

---

## ⚙️ Technologies Used

| Category         | Tools/Frameworks                         |
|------------------|------------------------------------------|
| ML Models        | Isolation Forest, Autoencoder            |
| Dimensionality   | PCA, SVD, UMAP                           |
| Visualization    | Matplotlib, Seaborn                      |
| API Framework    | FastAPI                                  |
| Libraries        | Scikit-learn, TensorFlow, Keras, Pandas  |

---

## 🚀 Getting Started

### 1️⃣ Clone and Install

```bash
git clone https://github.com/yourusername/industrial-anomaly-detection.git
cd industrial-anomaly-detection
pip install -r requirements.txt
```

### 2️⃣ Prepare the Data

Place your time-series CSV file into the `data/` folder. Ensure columns include timestamps and sensor readings.

### 3️⃣ Train Models

```bash
python src/anomaly_isoforest.py
python src/anomaly_autoencoder.py
```

### 4️⃣ Start FastAPI Service

```bash
uvicorn src.api:app --reload
```

Send POST requests with sensor data to `/predict` endpoint to get anomaly scores.

---

## 📊 Example Visualizations

- **PCA 2D Projection:**
  ![PCA](assets/pca_plot.png)

- **Reconstruction Error Distribution (Autoencoder):**
  ![Reconstruction](assets/reconstruction_loss.png)

---

## 🧠 Model Details

### Isolation Forest
- Tree-based model for high-dimensional anomaly detection.
- Does not require labeled data.
- Fast and scalable.

### Autoencoder
- Neural network learns to compress and reconstruct data.
- High reconstruction error indicates anomaly.

---

## 🔬 Future Enhancements

- Real-time Kafka/Socket-based streaming pipeline
- LSTM-based sequence anomaly detection
- Alerting/Notification system integration
- Grafana dashboard for live monitoring

---

## 📬 Contact

**Sujoy Banerjee**  
📧 bsujoy577@gmail.com 
