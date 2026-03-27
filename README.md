EXP NO:07	EVALUATION OF RADAR RANGE USING PYTHON

Aim:
To calculate the maximum range of a radar system using the Radar Range Equation and verify the results through Python programming.

Theory:
The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum range at which a radar can detect a target. It is given by:


Procedure
1.	Set Up the Python Environment: Ensure that Python is installed on your system. You can use Anaconda for managing Python packages and environments, or any other Python IDE of your choice.
2.	Import Necessary Libraries: Import the math library in Python.
3.	Define the Radar Range Equation Function: Create a function to calculate the maximum range using the Radar Range Equation.
4.	Input Parameters for the Radar System: Define the input parameters such as transmitted power, transmitter gain, receiver gain, radar frequency, radar cross section, and minimum detectable power.
5.	Calculate the Maximum Range: Use the function to calculate the maximum range of the radar.
6.	Execute the Program: Run the Python script to calculate and display the maximum range of the radar.

<img width="457" height="528" alt="image" src="https://github.com/user-attachments/assets/14d1fc2b-5915-45dd-bc86-823bee85df68" />
CODE 
Gt = 1200;

Gr = 1200;

lambda = 0.04;

sigma = 1.5;

Pmin = 2e-10;



Pt = 1:100:100000;

Rmax1 = ((Pt .* Gt .* Gr .* lambda^2 .* sigma) ./ ((4*%pi)^3 .* Pmin)).^(1/4);



subplot(2,1,1);

plot(Pt, Rmax1);

xlabel("Pt (W)");

ylabel("Rmax (m)");

title("Rmax vs Pt");

xgrid();


Pmin2 = 1e-15:1e-15:1e-12;

Pt2 = 6000;


Rmax2 = ((Pt2 .* Gt .* Gr .* lambda^2 .* sigma) ./ ((4*%pi)^3 .* Pmin2)).^(1/4);


subplot(2,1,2);

plot(Pmin2, Rmax2);

xlabel("Pmin (W)");

ylabel("Rmax (m)");

title("Rmax vs Pmin");

xgrid();
TABULATION 
<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/7410b02f-b65e-41ef-b78e-7445f4b09e26" />
<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/50f537a5-2436-46a9-a820-994e002a3977" />
<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/4049c243-7048-4567-a4fb-0bf2314baa7f" />




OUTPUT 
<img width="1918" height="983" alt="image" src="https://github.com/user-attachments/assets/c63692cb-9094-4c62-9050-778be7aa47e4" />

Result:

Thus, the maximum range of a radar system using the Radar Range Equation is verified through a Python program.
