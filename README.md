# Delivery Time Estimation App 🚴

A **Streamlit-based web application** to estimate delivery time for orders using delivery person information, vehicle details, order characteristics, and environmental factors. The app can be extended to integrate a trained ML model for precise predictions.

---

## Table of Contents

1. [Project Overview](#project-overview)  
2. [Features](#features)  
3. [Architecture](#architecture)  
4. [Dataset](#dataset)  
5. [Folder Structure](#folder-structure)  
6. [Usage](#usage)  
7. [Future Enhancements](#future-enhancements)  

---

## Project Overview

Delivery time estimation is crucial for food delivery, e-commerce, and logistics platforms. This project provides a **user-friendly interface** where a delivery operator or manager can input:

- Delivery person details (age, ratings, vehicle type, and condition)  
- Order details (type, order time, pick-up time)  
- Restaurant & delivery location coordinates  
- Environmental factors (weather, traffic density)

The app then outputs an **estimated delivery time**. Currently, it uses a placeholder random value, but it is designed to easily integrate a trained machine learning model.

---

## Features

- **Delivery Person Info:** Age, ratings, vehicle type, and vehicle condition.  
- **Order Info:** Type of order, order time, and pick-up time.  
- **Location Info:** Restaurant and delivery latitude/longitude.  
- **Environmental Info:** Weather conditions and traffic density.  
- **Predict Delivery Time:** Calculates estimated delivery time.  
- **Input Summary:** Displays all entered inputs in a structured table for verification.  
- **Unique Widget Keys:** Avoids Streamlit duplicate element ID errors.

---

## Architecture
User Inputs → Streamlit Widgets → Data Collection → (ML Model) → Delivery Time Prediction → Output


- **Frontend:** Streamlit app (`app.py`) for interactive user interface.  
- **Backend/ML:** Optional Python script (`model.py`) for prediction logic.  
- **Data:** Can be from CSV, database, or API. Input is collected directly via widgets.  

---

## Dataset (Optional)

If using a machine learning model:

- **Typical features:**
  - `delivery_person_age`
  - `delivery_person_ratings`
  - `vehicle_condition`
  - `type_of_vehicle`
  - `restaurant_latitude`, `restaurant_longitude`
  - `delivery_latitude`, `delivery_longitude`
  - `order_date`, `time_ordered`, `time_order_picked`
  - `type_of_order`
  - `weather_conditions`, `road_traffic_density`

- **Target:** `delivery_time` (in minutes)  

> You can train a regression model (Random Forest, XGBoost, or Linear Regression) with this dataset.

---

## Folder Structure
project_folder
- app.py # Main Streamlit application
- model.py # Optional: ML model loading/prediction functions
- requirements.txt # Python dependencies
- data/ 
- README.md # Project documentation

## Usage

- Run the app: streamlit run app.py.
- Enter delivery person, order, location, and environmental details.
- Click Predict Delivery Time.
- View the predicted delivery time and input summary.


## Future Enhancements

- Integrate Google Maps API to calculate distance and route.
- Add real-time traffic and weather data for better predictions.
- Store historical predictions for analytics.
- Deploy to Streamlit Cloud or Heroku.

