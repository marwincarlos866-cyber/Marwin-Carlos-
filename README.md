# Skin Disease Detection using Images

An end-to-end Deep Learning system to classify skin diseases from images. 
Built with TensorFlow/Keras, FastAPI, and standard HTML/CSS/JS.

## Folder Structure

- `model/` - Contains the trained Keras `.h5` model.
- `backend/` - Contains the FastAPI backend application.
- `frontend/` - Contains the HTML, CSS, and JS for the web interface.
- `dataset/` - Directory for placing training data (folders named by class).

## How to Run

### 1. Install Dependencies
Make sure you have Python installed. Then, run:
```bash
pip install -r requirements.txt
```

### 2. Generate a Dummy Model (For immediate testing)
If you do not have a trained model yet, you can create a random dummy model so the UI and backend can be tested immediately:
```bash
python create_dummy_model.py
```
This creates `model/skin_disease_model.h5`.

*(Optional: To train a real model, place your dataset in the `dataset/` folder and run `python train_model.py`)*

### 3. Start the Backend Server
Run the FastAPI backend using `uvicorn`:
```bash
cd backend
uvicorn app:app --reload
```
The backend will start at `http://127.0.0.1:8000`.

### 4. Open the Frontend
Open the `frontend/index.html` file in your browser (just double-click it, or use a Live Server extension if you prefer).

Upload an image and test the system!
