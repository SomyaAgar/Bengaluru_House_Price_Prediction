# Bengaluru House Price Prediction

This project is a **regression-based machine learning model** that predicts housing prices in **Bengaluru** using real-world data. The project also features a **fully functional web application** built using the **Flask** framework, allowing users to interact with the model through a web interface.

---
## Features

- Data preprocessing and feature engineering
- Regression model training and evaluation
- Web interface for real-time house price prediction
- Clean and responsive UI using HTML, Bootstrap, and JavaScript

---
## Tech Stack

### Backend
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Flask

### Frontend
- HTML
- CSS (Bootstrap)
- Basic JavaScript

### Environment
- Jupyter Notebook (for model development and analysis)

---
## Dataset

The dataset used is obtained from Kaggle (https://www.kaggle.com/datasets/amitabhajoy/bengaluru-house-price-data), **Bengaluru House Data**, which contains  9 features :

Area Type 
Availability
Location
Size
Society 
Total sqft
bath
balcony
price

---
## Project Workflow

1. **Import necessary libraries**  
   Load Python libraries including Pandas, NumPy, Matplotlib, Seaborn, and Scikit-learn modules.

2. **Load and inspect dataset**  
   Read the Bengaluru housing dataset and inspect its structure and basic statistics.

3. **Perform EDA and feature engineering**  
   Key observations and actions:
   - Found large number of null values in `society` and `balcony` columns.
   - `location` has only one missing value, handled with imputation.
   - Dropped non-essential columns: `area_type`, `availability`, `society`, and `balcony`.
   - Standardized `size` column values (e.g., unified formats like "2 BHK" and extracted numeric parts).
   - Identified and handled outliers, especially in `total_sqft` (e.g., entries like `1133 - 1384`).
   - Created a new feature: `price_per_sqft`.
   - Grouped low-frequency locations (less than 10 occurrences) into an `other` category.
   - Removed unrealistic entries (e.g., properties with < 300 sqft per BHK).

4. **Export cleaned data**  
   Saved the cleaned and transformed dataset to a new CSV file for modeling.

5. **Model building and evaluation**  
   - Imported libraries: `train_test_split`, `LinearRegression`, `Lasso`, `Ridge`, `StandardScaler`, `OneHotEncoder`, and `r2_score`.
   - Applied transformations and tested various regression algorithms.
   - Compared models based on `R² Score`.
   - Selected and saved the best-performing model (**Ridge Regression**) using Python's `pickle` module.

6. **Create frontend**  
   - Designed a simple user interface using HTML, Bootstrap, and JavaScript.
   - Input form accepts location, square footage, BHK, and number of bathrooms.

7. **Backend integration using Flask**  
   - Created a Flask app that loads the trained model.
   - Accepts user input from the frontend and returns predicted house price.
  
---
## UI Overview:
![image](https://github.com/user-attachments/assets/d6fdda76-5fb9-4124-9aa3-0fc836b0efdb)

---
