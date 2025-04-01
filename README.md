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
```

---

## Unique Aspects

✅ **End-to-End ML Pipeline**  
✅ **Secure MongoDB Data Storage**  
✅ **FastAPI for Real-time Predictions**  
✅ **Scalable and Modular Codebase**  

---

## Author
Developed by **Viplove**  
📧 viplovethakran4@gmail.com  

---

This project is a powerful tool for network security monitoring and can be extended for real-world cybersecurity applications. 🚀
