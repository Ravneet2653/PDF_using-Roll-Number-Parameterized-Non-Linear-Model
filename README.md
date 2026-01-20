PDF Learning Using Roll Number Parameterized Non Linear Model

Overview

This project focuses on learning a probability density function from real world air quality data using a roll number dependent non linear transformation. The goal is to demonstrate how parameterized transformations affect the distribution of data and how a probabilistic model can be learned using Maximum Likelihood Estimation.

Dataset

The dataset used in this project is the India Air Quality Data available on Kaggle.  
Link: https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data

Feature Used

NO2 concentration values are used as the input feature for modeling.

Methodology

Step 1 Non Linear Transformation

Each NO2 value x is transformed into a new variable z using the following transformation:

z = x + ar * sin(br * x)

The parameters ar and br are derived from the university roll number.

ar = 0.05 * (r mod 7)  
br = 0.3 * (r mod 5 + 1)  

Here, r represents the student’s university roll number. This ensures that each student obtains a slightly different model.

Step 2 Probability Density Function Learning

The transformed variable z is assumed to follow a Gaussian distribution. The parameters of the distribution are estimated using Maximum Likelihood Estimation.

mu is calculated as the mean of z  
sigma is calculated as the standard deviation of z  
lambda is calculated as 1 divided by 2 times sigma squared  
c is calculated as 1 divided by the square root of 2 times pi times sigma squared  

Step 3 Model Validation

A histogram of the transformed values z is plotted along with the learned probability density function. This visualization helps verify how well the Gaussian model fits the transformed data.

Results

The model automatically computes the following parameters:

Lambda  
Mu  
c  

Example Output

Lambda 0.001460  
Mu 25.809623  
c 0.021561  

Tools and Technologies

Python  
Pandas  
NumPy  
Matplotlib  
Google Colab  

Project Structure

PDF_Learning.ipynb  
data.csv  
README.md  

How to Run the Project

1. Download or clone this repository
2. Upload data.csv to Google Colab or your local environment
3. Open PDF_Learning.ipynb
4. Set your university roll number in the code
5. Run all cells to generate results and plots

Learning Outcomes

Understanding non linear data transformations  
Applying Maximum Likelihood Estimation for parameter learning  
Visualizing probability density functions  
Working with real world environmental data  

License

This project is intended for academic and educational use.
