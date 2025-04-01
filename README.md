# Network Security Detection System

## Overview

The **Network Security Detection System** is a machine learning-based solution designed to analyze and detect security threats in network traffic or web URLs. This project integrates **FastAPI**, **MongoDB**, and **Machine Learning Pipelines** to process and classify network activity efficiently.

## Key Features

- **Machine Learning for Security Threats**: Uses a trained model to classify network activity.
- **FastAPI Integration**: Provides a REST API for seamless interaction.
- **MongoDB for Data Storage**: Stores network security-related data for model training.
- **Automated Data Processing**: Ingests, validates, and transforms network data.
- **Custom Logging and Exception Handling**: Enhances debugging and tracking.

---

## Installation and Setup

### Prerequisites
Ensure you have Python installed (>=3.8). Install dependencies using:

```bash
pip install -r requirements.txt
```

### Environment Setup
Create a `.env` file and define your MongoDB URL:
```env
MONGO_DB_URL=mongodb+srv://your_username:your_password@cluster.mongodb.net
```

---

## Project Structure

```
Network_Security/
│── networksecurity/           # Core package
│   ├── components/            # ML Pipeline components
│   ├── logging/               # Logging system
│   ├── exception/             # Custom exception handling
│   ├── pipeline/              # Training pipeline
│   ├── utils/                 # Helper utilities
│── data_schema/               # Data structure definitions
│── app.py                     # FastAPI application
│── main.py                    # Runs the training pipeline
│── push_data.py                # Uploads data to MongoDB
│── requirements.txt            # Dependencies
│── setup.py                    # Installation script
│── test_mongodb.py             # MongoDB connection test
```

---

## How It Works

### 1. **Data Ingestion**
- Defined in `networksecurity.components.data_ingestion`
- Reads raw network data and stores it in MongoDB.

### 2. **Data Validation**
- Ensures the schema matches (`data_schema/schema.yaml`).

### 3. **Data Transformation**
- Converts and cleans data for training.

### 4. **Model Training**
- Implemented in `networksecurity.components.model_trainer`
- Uses `scikit-learn` to build a predictive model.

### 5. **API Service**
- `app.py` runs a FastAPI server for predictions.

---

## Running the Project

### Train the Model
```bash
python main.py
```

### Start the API Server
```bash
uvicorn app:app --reload
``![Screenshot (72)](https://github.com/user-attachments/assets/9d35d418-afb7-4e58-8b00-4aab852df6c7)![Screenshot (71)](https://github.com/user-attachments/assets/797354a6-16d2-4921-a704-b8b36a21c752)

`

---

## Unique Aspects

✅ **End-to-End ML Pipeline**  
✅ **Secure MongoDB Data Storage**  
✅ **FastAPI for Real-time Predictions**  
✅ **Scalable and Modular Codebase**  


---

## MLflow & DagsHub Integration

### Why Use MLflow?
MLflow helps in:
- Tracking experiments, parameters, and metrics.
- Managing and storing multiple model versions.
- Reproducing results efficiently.

### Why Use DagsHub?
DagsHub provides:
- A remote repository to store MLflow experiments.
- A web interface to compare model versions.
- Easy collaboration on ML projects.

### Setting Up MLflow with DagsHub

1. **Install MLflow**:
   ```bash
   pip install mlflow
   ```

2. **Configure MLflow to Use DagsHub**:
   ```python
   import mlflow

   mlflow.set_tracking_uri("https://dagshub.com/YOUR_USERNAME/YOUR_PROJECT.mlflow")
   mlflow.start_run()

   mlflow.log_param("learning_rate", 0.01)
   mlflow.log_metric("accuracy", 0.92)
   mlflow.end_run()
   ```

3. **View Experiments in DagsHub**:
   - Go to **your DagsHub project URL**.
   -

https://github.com/user-attachments/assets/1cff81b4-2f0b-46a3-876b-5754d25d9063

 Check the **MLflow UI** for logged runs.

### MLflow & DagsHub Architecture
![MLflow DagsHub Integration](A_conceptual_diagram_showing_MLflow_and_DagsHub_in.png)

---

## Running the Project

### Train the Model
```bash
python main.py
```

---

## Author
Developed by **Viplove**  
📧 viplovethakran4@gmail.com  

---

This project is a powerful tool for network security monitoring and can be extended for real-world cybersecurity applications. 🚀
