PDF Using Roll Number Parameterized Non Linear Model

Problem Statement

This project learns a probability density function from air quality data using a roll number dependent non linear transformation.

Dataset
India Air Quality Data from Kaggle  
https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data

Feature Used
NO2

Step 1 Transformation

Each NO2 value x is transformed into z using the formula:

z = x + ar * sin(br * x)

Where:
ar = 0.05 * (r mod 7)  
br = 0.3 * (r mod 5 + 1)  
r is the university roll number

Step 2 Probability Density Function

The transformed variable z is assumed to follow a Gaussian distribution.

Using Maximum Likelihood Estimation:
mu = mean(z)  
sigma = standard deviation(z)  
lambda = 1 / (2 * sigma * sigma)  
c = 1 / sqrt(2 * pi * sigma * sigma)

Step 3 Results

The model automatically computes:
Lambda  
Mu  
c

Visualization

A histogram of transformed values z is plotted along with the learned probability density function to verify the model fit.

Tools Used

Python  
Pandas  
NumPy  
Matplotlib  
Google Colab  

Files

PDF_Learning.ipynb  
data.csv  
README.md  

How to Run

1. Upload data.csv to Google Colab
2. Open PDF_Learning.ipynb
3. Set your roll number r
4. Run all cells

Sample Output

Lambda 0.001460  
Mu 25.809623  
c 0.021561
