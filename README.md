# EVALUATION OF RADAR RANGE 
# Aim:
To calculate the maximum range of a radar system using the Radar Range Equation and verify the results through Python programming.

# Theory:
The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum range at which a radar can detect a target. It is given by:

<img width="367" height="424" alt="Screenshot 2025-10-29 154151" src="https://github.com/user-attachments/assets/3958d1ea-e021-4629-96f7-65a3a177d555" />

# Procedure:
1.	Set Up the Python Environment: Ensure that Python is installed on your system. You can use Anaconda for managing Python packages and environments, or any other Python IDE of your choice.
2.	Import Necessary Libraries: Import the math library in Python.
3.	Define the Radar Range Equation Function: Create a function to calculate the maximum range using the Radar Range Equation.
4.	Input Parameters for the Radar System: Define the input parameters such as transmitted power, transmitter gain, receiver gain, radar frequency, radar cross section, and minimum detectable power.
5.	Calculate the Maximum Range: Use the function to calculate the maximum range of the radar.
6.	Execute the Program: Run the Python script to calculate and display the maximum range of the radar.

# Code:
Pt = 1000;
G = 1000;
sigma = 1;
Ae = 10;

Smin = logspace(-12, -6, 100);
Rmax = ((Pt * G * sigma * Ae) ./ (16 * %pi^2 .* Smin)).^(1/4);
subplot(3,1,1);
plot(Smin, Rmax);

Ppeak = linspace(100, 10000, 100);
Rmax2 = ((Ppeak * G * sigma * Ae) ./ (16 * %pi^2 * 1e-10)).^(1/4);
subplot(3,1,2);
plot(Ppeak, Rmax2);

Gt = linspace(100, 2000, 100);
Rmax3 = ((Pt * Gt * sigma * Ae) ./ (16 * %pi^2 * 1e-10)).^(1/4);
subplot(3,1,3);
plot(Gt, Rmax3);
# Output:
![WhatsApp Image 2025-11-20 at 20 19 15_8de936e3](https://github.com/user-attachments/assets/0be88c41-7c15-4a37-ac65-a705c0d25e79)

# Tabulation:

# Result :
Thus the maximum range of a radar system using the Radar Range Equation is verified through a Python program.
