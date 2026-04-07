# EVALUATION-OF-RADAR-RANGE-USING-PYTHON-

__Aim__:

To calculate the maximum range of a radar system using the Radar Range Equation and verify the results 
through Python programming.

__Theory__:

The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum 
range at which a radar can detect a target. It is given by:

<img width="573" height="442" alt="image" src="https://github.com/user-attachments/assets/ba374d30-d11f-41e5-a4fc-a42dde71d8e7" />

__Procedure__:

1. Set Up the Python Environment: Ensure that Python is installed on your system. You can use 
Anaconda for managing Python packages and environments, or any other Python IDE of your choice. 
2. Import Necessary Libraries: Import the math library in Python. 
3. Define the Radar Range Equation Function: Create a function to calculate the maximum range using 
the Radar Range Equation. 
4. Input Parameters for the Radar System: Define the input parameters such as transmitted power, 
transmitter gain, receiver gain, radar frequency, radar cross section, and minimum detectable power. 
5. Calculate the Maximum Range: Use the function to calculate the maximum range of the radar. 
6. Execute the Program: Run the Python script to calculate and display the maximum range of the radar.



   __Program__:

```
Gr = 7;
w = 8;
sigma = 9;  
pmin = 1e-9;
Gt = 6;
Pt = 0.5:0.5:100;   
Rmax1 = (((Pt .* Gt .* Gr .* (w.^2) .* sigma) ./ (((4 * %pi).^3) .* pmin))).^(1/4);
subplot(3,1,1);
plot(Pt, Rmax1);

Pt = 20;
Gt = 0.1:0.1:9;     
Rmax2 = (((Pt .* Gt .* Gr .* (w.^2) .* sigma) ./ (((4 * %pi).^3) .* pmin))).^(1/4);
subplot(3,1,2);
plot(Gt, Rmax2);

Gt = 7;
pmin = 1e-14:1e-13:1e-9;  
Rmax3 = (((Pt .* Gt .* Gr .* (w.^2) .* sigma) ./ (((4 * %pi).^3) .* pmin))).^(1/4);
subplot(3,1,3);
plot(pmin, Rmax3);
```


   __Algorithm__:
   

Initialize constants:

λ (wavelength) = 0.03 m
σ (radar cross section) = 1 m²
Vary each parameter while keeping the others constant:

Pt: 0.1 → 10
Gt: 1 → 50
Pm: 1e⁻¹⁵ → 1e⁻¹⁰
Compute maximum range using: R_max = ((Pt * Gt² * λ² * σ) / ((4π)³ * Pm))¼

Plot the following:

Pt vs Rmax
Gt vs Rmax
Pm vs Rmax


   __Output__:

   
   ![WhatsApp Image 2026-04-07 at 9 44 43 PM](https://github.com/user-attachments/assets/3ddcd112-199f-4fa9-89ed-471d4827ddf9)


__Calculation__:


<img width="1080" height="1289" alt="image" src="https://github.com/user-attachments/assets/a2a480d1-2edb-48f6-8e29-5358ad86777e" />



   __Result__:
   
Thus, the maximum range of a radar system calculated using the Radar Range Equation is successfully verified using Scilab programming.



