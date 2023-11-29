# wind-data-analysis
This repository contains code to perform wind data analysis. 

Columns in the CSV file are: 
date, time, period, s1a, s1x, s1i, s1s, s2a, s2x, s2i, s2s, s3a, s3x, s3i, s3s, d1a, d1s, d2a, d2s, h1a, h1x, h1i, t1a, t1x, t1i, b1a, b1x, b1i, p1a, p1x, p1i, p1s, tia, tix, tii, vxa, vxx, vxi, bla, blx, bli, bra, brx, bri. 

where each column represents:  
s1a (Wind Speed 1 mean), 
s1x (Wind Speed 1 max), 
s1i (Wind Speed 1 min), 
s1s (Wind Speed 1 Sigma), 
s2a (Wind Speed 2 mean), 
s2x (Wind Speed 2 max), 
s2i (Wind Speed 2 min), 
s2s (Wind Speed 2 Sigma), 
s3a (Wind Speed 3 mean), 
s3x (Wind Speed 3 max), 
s3i (Wind Speed 3 min), 
s3s (Wind Speed 3 Sigma), 
d1a (Wind Direction 1 mean), 
d1s (Wind Direction 1 Sigma), 
d2a (Wind Direction 2 mean), 
d2s (Wind Direction 2 Sigma), 
h1a (Relative Humidity mean), 
h1x (Relative Humidity max), 
h1i (Relative Humidity min), 
t1a (Temperature mean), 
t1x (Temperature max), 
t1i(Temperature min), 
b1a (Air Pressure mean), 
b1x(Air Pressure max), 
b1i (Air Pressure min), 
p1a (Wind Speed 4 mean), 
p1x (Wind Speed 4 max), 
p1i (Wind Speed 4 min), 
p1s (Wind Speed 4 Sigma), 
tia (Temperature Internal mean), 
tix (Temperature Internal max), 
tii (Temperature Internal min), 
vxa (External Supply mean), 
vxx (External Supply max), 
vxi (External Supply min), 
bla(Battery left mean), 
blx (battery left max), 
bli (Battery left min), 
bra (Battery right mean), 
brx (Battery right max), 
bri (Battery right min). 

Here is the raw data description: 
	1. Wind Speed 101.5m (s1), Unit - 10 Hz, avg - 1, max - 2, min - 2, std - 4. 
	2. Wind Speed 100.0 m (s2), Unit - 10 Hz, avg - 5, max - 6, min - 7, std - 8
	3. Wind Speed 80.0 m (s3), Unit - 10 Hz, avg - 9, max - 10, min - 11, std - 12
 
Remarks: 
Evaluation of wind speed in m/s using the slope and offset values of the adapted calibration certificate win the formula.
ws (avg, max, min) =frequenz*(slope*0, 1)+ offset ws (std)= frequenz* (slope*0, 1)

  4. Wind Direction 99.5 m (d1), Unit - deg, avg - 13, std - 14
	5. Wind Direction 49.5 m (d2), Unit - deg, avg - 15, std - 16

Remarks: 
Evaluation of wind direction consider an offset of 170° 
Evaluation of wind direction to Geographic north considers furthermore a magnetic declination of around 6 degree

 6. Air humidity 100.0 m (h1), Unit - %, avg - 17, max - 18, min - 19
 7. Air Temperature 100.0 m (t1), Unit - 10 Kelv, avg - 20, max - 21, min - 22
    
Remarks: 
Evaluation of temperature in C uses the formula:
°C=(Kelvin/10)-273,15

 8. Air Pressure 8.0 m (b1), Unit - hPa, avg - 23, max - 24, min - 25
 9. Wind Speed 10.0 m (p1), Unit - 10 Hz, avg - 26, max - 27, min - 28, std - 29.
     
Remarks: 
Evaluation of wind speed in m/s uses the slope and offset values of the adapted calibration certificate with the formula:
ws (avg, max, min) =frequenz*( slope*0.1)+offset ws (std)= frequenz*(slope*0.1)

  10. Temp. Intern, Unit - 10 degrees C, avg - 30, max - 31, min - 32
	11. External Supply, Unit - 10 V, avg - 33, max - 34, min - 35
	12. Battery Left, Unit - 10 V, avg - 36, max - 37, min - 38
	13. Battery right - Unit - 10 V, avg - 39, max - 40, min - 41

Perform advanced data analysis using Python. Derive meaningful insights with the data using various statistical operations and data visualizations. Perform data analysis for each and every column of the wind data in each CSV file one by one. Not all CSV files at once. Don't write a loop to analyze all the CSV data in the for loop.  I need code to analyze one by one CSV file.
