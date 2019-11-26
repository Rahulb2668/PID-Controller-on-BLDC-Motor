# PID-Controller-on-BLDC-Motor
Using PID controller controlling the Speed of a BLDC motor to maintain a beam horizontal


P, PI & PID controller are being used with the BLDC servomotor drive control system to achieve satisfactory transient 
and steady state response. Nowdays, PID & FUZZY logic controllers are the main controller being used to control BLDC. 
It is essential to know the exact mathematical model of the systems or response of the system for designing these controllers. 
In this project,transient performances of BLDCM with conventional controller like PID havebeen employed as controllers. 
The PID controller is applied in various fields in engineering owing to its simplicity, robustness, reliability and 
easy tuning parameters. The famous method to find PID parameters Ziegler-Nichols rule but sometimes are not the best. 
So, it can be realized by using genetic optimization technique based on three different cost functions to find the best 
PID control parameters.


A proportional–integral–derivative controller (PID controller) is a control loop feedback mechanism commonly used in 
industrial control systems. A PID controller continuously calculates an error value e(t) as the difference between 
a desired set point and a measured process variable and applies a correction based on proportional, integral, and 
derivative terms (sometimes denoted P, I, and D respectively) which give their name to the controller type.
In this project we will use this mechanism to control some brushless motor in order to calibrate our drone. 
We will put the motors on a balance and calculate the angle using the MPU6050 or the MPU9250 IMU module. So in our case the value
that we will control is the inclination angle of our drone. The e(t) error will be the difference between the real angle of the 
drone and the desired one.The desired one will be 0, which means that the drone is perfectly horizontal.


The code is not that complicated. We know that we have to read some data from the IMU (inertial movement unit) module. 
Using that data we calculate the real inclination angle of the axis. We will use just one axis for the balance, the x-axis. 
We have to compare that angle with the desired one which is 0o because we want the drone to be horizontal. 
To control the brushless motors we have to send a PWM signal to each ESC with a pulse with between 1000us and 2000us because 
that is the range of the ESCs that we've calibrated. We will divide the code in a few parts. But first we have to know a 
little bit of mathematic. We will use some formulas to calculate the angles. This are called Euler formulas.


I did this project with reference from electronoobs tutorial.
link : https://www.youtube.com/watch?v=AN3yxIBAxTA&t=871s
