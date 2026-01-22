
# Descriptive Analysis of BMW Used Car Dataset

### The Question : What exaclty are these dataset is? what is about? how we'll it is? what are different columns are about? what description are we gonna do ?

### These are the questions i tried to answer! with my data analysis skill!


## 1. Dataset Overview

This dataset contains information on **10,781 used BMW cars** with the following attributes:

- `model` – Car model (categorical)  
- `year` – Year of manufacture (numeric)  
- `price` – Price of the car (numeric)  
- `transmission` – Transmission type (categorical)  
- `mileage` – Mileage of the car (numeric)  
- `fuelType` – Fuel type (categorical)  
- `tax` – Road tax (numeric)  
- `mpg` – Miles per gallon (numeric)  
- `engineSize` – Engine size in litres (numeric)  

After cleaning, **10,664 observations** were used in the main statistical analysis.

---

## 2. Descriptive Statistics (Numerical Variables)

Summary statistics for the main numerical variables are shown below:

| Variable     | Mean      | Std Dev   | Min    | 25%      | 50% (Median) | 75%      | Max       |
|-------------|-----------|-----------|--------|----------|--------------|----------|-----------|
| Year        | 2017.06   | 2.35      | 1996   | 2016     | 2017         | 2019     | 2020      |
| Price       | 22692.89  | 11434.92  | 1200   | 14897    | 20261.5      | 27890    | 123456    |
| Mileage     | 25710.98  | 25146.63  | 1      | 5665.75  | 18783        | 38436.5  | 214000    |
| Tax         | 131.60    | 61.61     | 0      | 135      | 145          | 145      | 580       |
| MPG         | 56.48     | 31.47     | 5.5    | 45.6     | 53.3         | 62.8     | 470.8     |
| Engine Size | 2.17      | 0.55      | 0      | 2.0      | 2.0          | 2.0      | 6.6       |

Key observations:

- Price is **right-skewed** with extreme high-value outliers.
- Most cars were manufactured between **2016 and 2019**.
- Engine size is concentrated around **2.0 litres**.

---

## 3. Categorical Variable Distributions

### Fuel Type Distribution

| Fuel Type | Count |
|-----------|-------|
| Diesel    | 6988  |
| Petrol   | 3340  |
| Hybrid   | 297   |
| Electric | 36    |
| Other    | 120   |

- Diesel is the dominant fuel type.
- Electric vehicles represent a very small proportion of the dataset.

### Transmission Distribution (Proportion)

| Transmission | Proportion (%) |
|--------------|----------------|
| Semi-Auto    | 43.48          |
| Automatic    | 33.21          |
| Manual       | 23.30          |

- Semi-automatic transmission is the most common.

---

## 4. Price by Categorical Variables

### Price by Transmission (Median Price)

| Transmission | Median Price |
|--------------|-------------|
| Manual       | 13,490      |
| Automatic    | 19,299.5    |
| Semi-Auto    | 24,990      |

- Semi-automatic cars have the **highest median price**.
- Manual cars are the **cheapest on average**.

### Price by Fuel Type (Mean Price)

| Fuel Type | Mean Price |
|-----------|------------|
| Diesel    | 21,749     |
| Electric | 18,466     |
| Hybrid   | 27,155     |
| Other    | 18,194     |
| Petrol   | 24,322     |

- Hybrid cars have the **highest average price**.
- Diesel cars are cheaper on average than petrol and hybrid.

---

## 5. Correlation Analysis

<img width="418" height="327" alt="image" src="https://github.com/user-attachments/assets/b5647603-ac7e-4a3d-8b96-ea9007f4f41c" />


Correlation coefficients between numerical variables:

| Variable 1   | Variable 2   | Correlation |
|-------------|--------------|-------------|
| Price       | Year         | +0.62       |
| Price       | Mileage      | -0.61       |
| Price       | Engine Size  | +0.46       |
| Year        | Mileage      | -0.77       |
| MPG         | Engine Size  | -0.40       |
| Tax         | Engine Size  | +0.43       |

Key relationships:

- **Price increases with newer year** (moderate positive correlation).
- **Price decreases with higher mileage** (strong negative correlation).
- Larger engines are associated with **higher prices and higher tax**.
- Engine size is negatively correlated with fuel efficiency (mpg).

---

## 6. Outlier Analysis

Using the IQR method on `price`:

- Q1 and Q3 were computed.
- Outliers were defined as:
  - Price < Q1 − 1.5 × IQR  
  - Price > Q3 + 1.5 × IQR  

A total of **478 price outliers** were detected.

These likely correspond to:
- High-end luxury or performance models.
- Potential data entry errors at extreme values.

---

## 7. Key Findings

- The dataset is dominated by **diesel vehicles** and **semi-automatic transmissions**.
- Car price is strongly influenced by:
  - Year of manufacture (positive effect)
  - Mileage (negative effect)
  - Engine size (positive effect)
- The price distribution is highly skewed with significant high-value outliers.
- Hybrid vehicles are the most expensive on average, while manual transmission cars are the cheapest.

---

## 8. Conclusion

This descriptive analysis provides a clear overview of the structure, quality, and main patterns in the BMW used car dataset. The results highlight strong relationships between price, age, and mileage, and reveal important differences across fuel types and transmission categories. These insights form a solid foundation for further predictive modeling or inferential analysis.
