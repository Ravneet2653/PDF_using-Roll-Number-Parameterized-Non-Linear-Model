# PDF_using-Roll-Number-Parameterized-Non-Linear-Model
# 📊 Probability Density Learning using Roll-Number-Parameterized Non-Linear Model

## 📌 Problem Statement  
This project learns a probability density function (PDF) from air quality data using a roll-number-dependent non-linear transformation.

**Dataset:**  
https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data  
**Feature used:** NO2

---

## 🔁 Step 1: Transformation  
Each value of NO2 (x) is transformed into z using:

z = x + a_r sin(b_r x)

Where:
- a_r = 0.05 × (r mod 7)
- b_r = 0.3 × (r mod 5 + 1)
- r = university roll number

---

## 📐 Step 2: Probability Density Function  
We assume the transformed variable z follows a Gaussian distribution:

p̂(z) = c · exp(−λ(z − μ)²)

Using Maximum Likelihood Estimation:
- μ = mean(z)
- σ = standard deviation(z)
- λ = 1 / (2σ²)
- c = 1 / √(2πσ²)

---

## 📊 Step 3: Results  

| Parameter | Value |
|----------|-------|
| Lambda (λ) | Auto-computed |
| Mu (μ) | Auto-computed |
| c | Auto-computed |

---

## 📈 Visualization  
A histogram of transformed values z and the learned PDF curve are plotted to validate the model fit.

---

## 🛠 Tools Used  
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Google Colab  

---

## 📂 Files  
- PDF_Learning.ipynb → Colab notebook  
- data.csv → Dataset file  
- README.md → Project documentation  

---

## 🚀 How to Run  
1. Upload `data.csv` to Colab.  
2. Open the notebook.  
3. Set your roll number `r`.  
4. Run all cells.

---
