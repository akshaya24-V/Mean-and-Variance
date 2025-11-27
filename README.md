# MEAN-VARIANCE-AND-CROSS-CORRELATION

# Aim
To write a program for mean, variance, and cross-correlation in Scilab and verify the output.

# Equipment Needed
1.Computer with i3 Processor

2.Scilab Software

# Algorithm
1.Start.

2.Define function f(x) = 2*x.

3.Set integration limits a = 0, b = 1.

4.Compute mean of X: integrate x*f(x) over [a, b].

5.Compute E[X²]: integrate x²*f(x) over [a, b].

6.Compute variance of X: VarX = EX2 - EX^2.

7.Display EX (mean) and VarX (variance).

8.Input reference sequence x_seq and second sequence y_seq.

9.Compute sequence lengths n1 and n2.

10.Compute cross-correlation r = corr(x_seq, y_seq, n1).

11.Plot cross-correlation using plot2d3.

12.End.

# Procedure
1.Refer to the algorithm and understand the steps of the experiment.

2.Open Scilab on your system.

3.Type your code in a new editor window.

4.Save the file with an appropriate name.

5.Execute the code by pressing F5 or using the Execute option.

6.If any errors occur, check your code, correct them, and execute again.

7.When the code runs successfully, input the sequences for cross-correlation when prompted.

8.Verify the generated results:

9.Mean of X

10.Variance of X

11.Cross-correlation plot

Analyze the results as per your experiment’s requirement.

# Program

clc;
 
 clear;
  
  function fx = pdfx(x)
  
  z = 3*(1-x)^2;
      
  fx = x*z;

  endfunction
  
  a = 0;
  
  b = 1;
  
  EX = intg(a, b, pdfx);
  
  function fy = pdfy(x)
  
z = 6*(1-x)^2;
      
fy = x*z;

  endfunction

  EY = intg(a, b, pdfy);
  
  disp("1)Mean of X =",EX);
  
  disp("2)Mean of Y =",EY);
  
  function p = f1(u)
  
  q = 3*(1-u)^2;
     
  p = u^2 * q;
  
  endfunction
  
  a = 0;
  
  b = 1;
  
  EX2 = intg(a, b, f1);
  
  function r = f2(v)
  
s = 6*(1-v)^2;
      
r = v^2 * s;
  
  endfunction
  
  EY2 = intg(a, b, f2);
  
  vX2 = EX2 - (EX)^2;
  
  vY2 = EY2 - (EY)^2;
  
  disp("3) Variance of X =",vX2);
  
  disp("4)Variance of Y =",vY2);
  
  x= input("type in the reference sequence=");
  
  y= input("type in the second sequence=");
  
  S1=max(size(y))-1;
  
  S2=max(size(x))-1;
  
  r=corr(x,y,S1);
  
  plot2d3('gnn',r);

# Output

<img width="1600" height="836" alt="image" src="https://github.com/user-attachments/assets/a29a2549-7173-423e-9910-7e710c0b3739" />



![WhatsApp Image 2025-11-27 at 21 17 53_6ef7477a](https://github.com/user-attachments/assets/1fa55dc8-4f6c-42a3-8f07-4fbeab2c14ac)


# Tabular Column:

![WhatsApp Image 2025-11-27 at 21 23 01_3ad8b2c0](https://github.com/user-attachments/assets/f15d091f-3e35-4050-952e-143d31daa705)


# MANUAL CALCULATION:

![WhatsApp Image 2025-11-27 at 21 22 05_491a29c3](https://github.com/user-attachments/assets/7a9cb196-7ebf-4ccd-99b4-df119edfd5c6)

![WhatsApp Image 2025-11-27 at 21 22 21_a21292aa](https://github.com/user-attachments/assets/ae001355-5526-4aa8-9895-4c7802ec8785)



RESULT:
Thus the mean , variance and cross correlation are executed in Scilab and output is verified.
