Predictive Analysis for Manufacturing Operations API
 ## Objective
 This API predicts machine downtime or production defects using manufacturing data. It includes
 endpoints for uploading data, training a model, and making predictions.
 ## Setup Instructions
 ### Prerequisites- Python 3.8+- Pip (Python package installer)
 ### Installation
 1. Clone the repository:
 ```
 git clone https://github.com/yourusername/manufacturing-predictive-api.git
 cd manufacturing-predictive-api
 ```
 2. Create a virtual environment (optional):
 ```
 python -m venv venv
 source venv/bin/activate  # On Windows use `venv\Scripts\activate`
 ```
 3. Install the dependencies:
 ```
 pip install -r requirements.txt
 Page 1
```
 Predictive Analysis for Manufacturing Operations API
 ### Configuration- Update the `.env` file with necessary configurations if applicable.
 ## Running the API
 1. Start the API server:
 ```
 python app.py
 ```
 2. The API will be accessible at `http://localhost:8000`.
 ## Example API Requests and Responses
 ### 1. Upload Data
 **Endpoint:** `POST /upload`  
**Description:** Upload a CSV file containing manufacturing data.
 **Request:**
 ```
 curl -X POST -F "file=@data.csv" http://localhost:8000/upload
 ```
 **Response:**
 ```
 {
 Page 2
Predictive Analysis for Manufacturing Operations API
    "message": "File uploaded successfully.",
    "data_summary": {
        "rows": 100,
        "columns": 3
    }
 }
 ```
 ### 2. Train Model
 **Endpoint:** `POST /train`  
**Description:** Train the model on the uploaded dataset.
 **Request:**
 ```
 curl -X POST http://localhost:8000/train
 ```
 **Response:**
 ```
 {
 }
 ```
    "message": "Model trained successfully.",
    "accuracy": 0.95,
    "f1_score": 0.92
 Page 3
### 3. Predict
 Predictive Analysis for Manufacturing Operations API
 **Endpoint:** `POST /predict`  
**Description:** Predict machine downtime based on input parameters.
 **Request:**
 ```
 curl -X POST -H "Content-Type: application/json" \-d '{"Temperature": 80, "Run_Time": 120}' \
 http://localhost:8000/predict
 ```
 **Response:**
 ```
 {
 }
 ```
    "Downtime": "Yes",
    "Confidence": 0.85

