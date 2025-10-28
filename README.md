# MEAN-VARIANCE-AND-CROSS-CORELATION
## AIM:
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

## APPARATUS REQUIRED

-	 Computer with i3 Processor
- 	SCI LAB


## Algorithm
1.	Define	the	Function:	Specify the	function	you	want	to	simulate.	For	example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2.	Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3.	Evaluate the Function: Compute the function values at each of these sample points.
4.	Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5.	Display Results: Output the computed mean variance and Cross Correlation PROCEDURE
    - Refer Algorithms and write code for the experiment.
    - Open SCILAB in System
    -	Type your code in New Editor
    -	Save the file
    -	Execute the code
    -	If any Error, correct it in code and execute again
    -	Verify the generated results

##  Code
```
clear; clc;
function X = f(x)
    z = 2* (2 - x).^2;
    X = x .* z;
endfunction
a = 0; b = 1;
EX = intg(a, b, f);
function Y = c(y)
    z = (3 - y).^2;
    Y = y .* z;
endfunction
EY = intg(a, b, c);
function X2 = g(x)
    z =  2*(2 - x).^2;
    X2 = (x.^2) .* z;
endfunction
EX2 = intg(a, b, g);
function Y2 = h(y)
    z = (5 - y).^2;
    Y2 = (y.^2) .* z;
endfunction
EY2 = intg(a, b, h);
vX2 = EX2 - (EX)^2;
vY2 = EY2 - (EY)^2;
disp(EX, "i) Mean of X =");
disp(EY, "   Mean of Y =");
disp(vX2, "ii) Variance of X =");
disp(vY2, "   Variance of Y =");
x= input("type in the reference sequence="); 
y= input("type in the second sequence="); 
n1=max(size(y))-1;
n2=max(size(x))-1;
r=corr(x,y,n1);
plot2d3('gnn',r);
```
## Output

<img width="1657" height="890" alt="Screenshot 2025-10-28 110653" src="https://github.com/user-attachments/assets/55c3bb87-c523-4db6-b98b-51250606420e" />

<img width="583" height="502" alt="image" src="https://github.com/user-attachments/assets/0e066c92-4401-4e99-9510-2ef56956e172" />






## TABULAR COLUMN

![WhatsApp Image 2025-10-28 at 11 16 22_a8894a47](https://github.com/user-attachments/assets/c5f76554-2440-4a35-a240-607467fea7eb)


## MANUAL CALCULATION

![WhatsApp Image 2025-10-28 at 11 17 49_bf6eef2f](https://github.com/user-attachments/assets/4c20e4aa-eb52-440d-90f9-ce8b21349ab4)
![WhatsApp Image 2025-10-28 at 11 11 12_a88a5d44](https://github.com/user-attachments/assets/5733973d-f597-4fff-bc5a-a78fc7ab7db5)


## RESULT
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
