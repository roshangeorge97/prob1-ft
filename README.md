# Problem 1: Freight Tiger Assignment

Hey! This is a simple project that predicts if your delivery will be delayed or not.

## What This Does

Built a basic ML model that looks at things like where you're shipping from/to, what kind of vehicle you're using, and weather conditions to guess if your delivery will be late.

## How I Handled the Data

Here's what I did to clean up and prepare the data:
- Did some basic EDA to find which data is missing
- Got rid of stuff we don't need (IDs and dates)
- Fixed missing vehicle types by using the most common one
- Turned text data into numbers so the model can understand it
- Added month and day info from shipping dates
- Split the data 80/20 for training and testing

## Models I Tried

I tested two different models:
- Logistic Regression (the simple one)
- Random Forest (the one that worked better)

Went with Random Forest since it did a better job predicting delays.

## About the API

Made a simple API using FastAPI. Here's how to use it:

Send a `POST` request to `/predict` with your delivery information. The API will respond with a prediction indicating whether the delivery is expected to be delayed.

### Example Request
```json
{
    "origin": "Jaipur",
    "destination": "Mumbai",
    "vehicle_type": "Truck",
    "distance": 450,
    "weather": "Clear",
    "traffic": "Normal"
}

## Getting Started

1. First, install what you need:
```bash
pip install pandas numpy scikit-learn fastapi uvicorn nest-asyncio seaborn matplotlib
```

2. Put your data file in the same folder:
- Name it: `AI ML Internship Training Data.xlsx`

3. Run it:
```bash
python main.py
```

4. Check it out at `http://localhost:8000`

## Stuff You Need to Install

- pandas
- numpy
- scikit-learn
- fastapi
- uvicorn
- nest-asyncio
- matplotlib
- seaborn
