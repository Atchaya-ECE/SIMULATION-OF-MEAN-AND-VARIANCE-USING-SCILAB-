# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB-

# AIM:

To write a program for mean, variance and cross correlation in SCILAB and verify the output. 

# EQUIPMENTS NEEDED:
* Computer with i3 Processor 
* SCI LAB 

# ALGORITHM:
1. Define the Function: Specify the function you want to simulate. For example, 
f(x)=sin⁡(x)f(x)=sin(x) or any other function. 
2. Generate Sample Points: Decide on the range and the number of sample points. Generate 
these sample points within the desired range. 
3. Evaluate the Function: Compute the function values at each of these sample points. 
4. Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the 
mean and variance of the computed function values. 
5. Display Results: Output the computed mean variance and Cross Correlation 

# PROCEDURE: 

1.Refer Algorithms and write code for the experiment. 

2.Open SCILAB in System 

3.Type your code in New Editor 

4.Save the file 

5.Execute the code If any Error, correct it in code and execute again 
  
6.Verify the generated results

# PROGRAM:
```
clear;
clc;

// === Mean Value ===

// Define function for Mean of X
function X = f(x)
    z = 3*(1 - x)^2;   // Marginal Probability Density Function
    X = x * z;         // X = x * f(x)
endfunction

a = 0;
b = 1;
EX = intg(a, b, f);    // Mean value of X

// Define function for Mean of Y
function Y = c(y)
    z = 3*(1 - y)^2;   // Marginal Probability Density Function
    Y = y * z;
endfunction

EY = intg(a, b, c);    // Mean value of Y

disp(EX, "i) Mean of X = ");
disp(EY, "Mean of Y = ");

// === Variance ===

function X2 = g(x)
    z = 3*(1 - x)^2;   // PDF
    X2 = x^2 * z;      // x^2 * f(x)
endfunction

EX2 = intg(a, b, g);   // E[X^2]

function Y2 = h(y)
    z = 3*(1 - y)^2;   // PDF
    Y2 = y^2 * z;
endfunction

EY2 = intg(a, b, h);   // E[Y^2]

vX2 = EX2 - (EX)^2;    // Variance of X
vY2 = EY2 - (EY)^2;    // Variance of Y

disp(vX2, "ii) Variance of X = ");
disp(vY2, "Variance of Y = ");

// === Cross Correlation ===

x = input("Type in the reference sequence (x): ");
y = input("Type in the second sequence (y): ");

n1 = max(size(y)) - 1;
r = corr(x, y, n1);

plot2d3(r);
xtitle("Cross Correlation of x and y");
xlabel("Lag");
ylabel("Correlation Coefficient");
```

# OUTPUT GRAPH:
<img width="656" height="299" alt="image" src="https://github.com/user-attachments/assets/21d971ec-ae3a-4fbf-9c0b-416ae84f5c25" />

<img width="760" height="597" alt="image" src="https://github.com/user-attachments/assets/97472310-3bda-4ced-b7d9-f2ea578baeb0" />

# CALCULATION:
![WhatsApp Image 2025-11-16 at 21 29 45_f9017501](https://github.com/user-attachments/assets/7fa5e5b7-f736-4ecc-822a-cbd63bf9f30e)

# RESULT:
![WhatsApp Image 2025-11-16 at 21 31 30_ebe257af](https://github.com/user-attachments/assets/21b55044-19bf-4def-9e42-27d55ff65a89)

