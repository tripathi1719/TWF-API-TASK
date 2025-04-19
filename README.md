# TWF-API-TASK
# Delivery Cost API

This is a simple REST API built using FastAPI that calculates the minimum cost to deliver an order to a given location (L1) using one delivery vehicle from one of three centers (C1, C2, or C3).

## 📦 Request Format
Send a POST request to `/calculate-cost` with the following JSON body:
```json
{
  "A": 1,
  "B": 1,
  "C": 1,
  "D": 0,
  "E": 0,
  "F": 0,
  "G": 1,
  "H": 1,
  "I": 3
}
```

## ✅ Response
```json
{
  "cost": 86
}

```

## 🚀 Running Locally
1. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # or venv\Scripts\activate on Windows
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the app:
   ```bash
   uvicorn main:app --reload
   ```

## 🌐 Deploying on Render
1. Push this code to a public GitHub repository.
2. Go to [https://render.com](https://render.com) > New > Web Service.
3. Connect your GitHub, select repo.
4. Set the following:
   - **Environment**: Python
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `uvicorn main:app --host 0.0.0.0 --port 10000`
   - **Port**: 10000
