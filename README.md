# Machine Learning | Predicting Worker Productivity in the Apparel Manufacturing Industry

This prediction project combined business requirements with machine learning modeling (Random Forest Regressor and Classifier) to solve a real-world allocation problem. The result is an accurate prediction model and a practical decision-making framework. This ML project demonstrates the power of analytics to generate financial impact on the manufacturing industry.

Check out the full notebook here: [Predicting Workers Productivity](https://github.com/SalazarHerna/ML-Predicting-Worker-s-Productivity/blob/a5347abeee04a754cf29b2c541548ac470b60ee1/Documents%20%26%20Code/Jupyter%20Notebook%20-%20Predicting%20Workers%20Productivity.ipynb)

---
## What Was Achieved?

Developed a **dual-purpose machine learning solution** that predicts garment workers’ productivity and optimizes worker placement decisions to maximize profitability for two types of clients:
- **Client A:** Pays based on actual productivity ($120 × P).
- **Client B:** Pays a flat fee ($250) **if** productivity exceeds 0.80.

![Visual Description](https://github.com/SalazarHerna/ML-Predicting-Worker-s-Productivity/blob/fe789e42f336a38ca5eca9b24dd1e3538ef8e7b8/Documents%20%26%20Code/Profit%20Comparison%20Model%20vs%20Random%20Allocation.jpeg)

By deploying a **Random Forest Regressor** and a **Random Forest Classifier**, the model performs smarter placement decisions, resulting in up to **$9,720 in added profit** compared to random placement.

---

## Insights

- **Client B (Classification)** benefited the most from ML guidance, with a **profit increase of $9,720** using the model vs. random placement.
- **Client A (Regression)** still saw a **profit lift of $641**, proving model-guided decisions create tangible value.
- Key predictive features included **idle time**, **incentives**, and **number of workers** — revealing how team dynamics and motivation shape productivity.

---

## Project Description

The garment manufacturing industry is highly labor-intensive, and accurate worker placement is key to operational efficiency. The business challenge was to:
> **Predict individual worker productivity** and **decide if/where to place each worker** to maximize profit for either Client A or Client B.

Using real-world data from the [UCI Garment Worker Productivity dataset](https://archive.ics.uci.edu/dataset/597/productivity+prediction+of+garment+employees), the project simulated a staffing agency making data-driven placement decisions under different client contracts.

---

## Tools Used

| Tool/Library           | Purpose                                      |
|------------------------|----------------------------------------------|
| **Python**             | Core programming language                    |
| **Pandas, NumPy**      | Data manipulation and numerical operations   |
| **Matplotlib, Seaborn**| Visualization of distributions and insights  |
| **scikit-learn**       | Model development and evaluation             |
| **Jupyter Notebook**   | Interactive coding and reporting             |

---

## Steps to Model Building & Analysis 

### Step 1. Data Preparation

### Step 2. Modeling for Client A (Regression)
- **Model:** Random Forest Regressor
- **Performance:** R² = **0.443**, lowest MSE among models tested
- **Decision Rule:** Place a worker **only if** `predicted_P × $120 − $70 > 0`

### Step 3. Modeling for Client B (Classification)
- **Model:** Random Forest Classifier
- **Performance:**
  - Accuracy = **0.8625**
  - AUC-ROC = **0.9388**
- **Decision Rule:** Place a worker **only if** `P(predicted > 0.8) × $250 − $70 > 0`

### Step 4. Revenue & Profit Analysis
- **Client A:**
  - Workers placed: 198
  - Total profit: $4,669.10
  - Average profit per placement: $23.58
- **Client B:**
  - Workers placed: 137
  - Total profit: $16,410.00
  - Average profit per placement: $119.78

### Step 5. Random Allocation vs. Model Comparison
- **Client A:**
  - Random Profit: $4,027.82
  - Value from Model: **+$641.28**
- **Client B:**
  - Random Profit: $6,690.00
  - Value from Model: **+$9,720.00**

---

## Business Value

This project illustrates how machine learning can **enhance decision-making** in operational settings. By making efficient predictions for different custromers, the models enabled more **profitable, data-driven worker placements**, saving costs and improving margins.

---
