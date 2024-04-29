**House Recommendations Random Forest**

**Description:**
This repository contains a FastAPI application that serves as a machine learning prediction service. The service exposes an endpoint `/predict` which accepts POST requests containing data to be predicted. Upon receiving a request, the service uses a pre-trained machine learning model to make predictions on the provided data and returns the predictions to the client.

**Features:**
- Exposes a RESTful API endpoint `/predict` for making predictions.
- Supports POST requests with JSON payloads containing input data.
- Handles data preprocessing and prediction using a pre-trained machine learning model.
- Returns prediction results in JSON format.

**Installation:**
1. Clone the repository:
   ```
   git clone https://github.com/tinapyp/HouseRecommendation-Random-Forest.git
   ```
2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

**Usage:**
1. Ensure that the pre-trained machine learning model file (`model.pkl`) is placed in the `models` directory.
2. Start the FastAPI server by running the `app.py` script:
   ```
   uvicorn app:app --host 127.0.0.1 --port 8000
   ```
3. Send POST requests to the `/predict` endpoint with input data in JSON format. For example:
   ```
   POST http://127.0.0.1:8000/predict
   {
       "Usia": 35,
       "Status Pernikahan": "Married",
       "Jumlah Anak": 2,
       "Pendapatan/Bulan": "High",
       "Fasilitas Yang Diinginkan": "Garden Lounge, Masjid",
       "Preferensi Lingkungan": "Dekat Dengan Tempat Ibadah, Dekat Dengan Sarana Perbelanjaan"
   }
   ```
   Replace the input data with your own values.
   
4. The server will respond with the predicted results in JSON format.