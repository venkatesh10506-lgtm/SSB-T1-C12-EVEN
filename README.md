# SSB-T1-C12-EVEN
AIM:

To write a program for mean, variance and cross correlation in SCILAB and verify the output.

EQUIPMENTS NEEDED:

.Computer with i3 Processor

.SCI LAB

ALGORITHM:

Define the Function: Specify the function you want to simulate. For example, f(x)=sin⁡(x)f(x)=sin(x) or any other function.
Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
Evaluate the Function: Compute the function values at each of these sample points.
Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
Display Results: Output the computed mean variance and Cross Correlation
PROCEDURE:

1.Refer Algorithms and write code for the experiment.

2.Open SCILAB in System

3.Type your code in New Editor

4.Save the file

5.Execute the code If any Error, correct it in code and execute again

6.Verify the generated results

PROGRAM:
```
clc;
clear;

// Parameters
Ac = 15.7;
Am = 31.8;
fm = 566;
fc = 5660;
fs = 56600;

// Time axis (short window)
t = 0:1/fs:0.05;

// SSB signals
LSB = Am*cos(2*%pi*(fc-fm)*t);
USB = Am*cos(2*%pi*(fc+fm)*t);

// Plot LSB
subplot(4,1,1)
plot(t,LSB)
title("SSB Modulated Signal (LSB)")
xlabel("time")
ylabel("Amplitude")

// Plot USB
subplot(4,1,2)
plot(t,USB)
title("SSB Modulated Signal (USB)")
xlabel("time")
ylabel("Amplitude")

// Spectrum
N = length(t);
f = (-N/2:N/2-1)*(fs/N);

LSB_spec = abs(fftshift(fft(LSB)));
USB_spec = abs(fftshift(fft(USB)));

// LSB Spectrum
subplot(4,1,3)
plot(f,LSB_spec)
title("SSB Signal Spectrum (LSB)")
xlabel("Frequency")
ylabel("Magnitude")

// USB Spectrum
subplot(4,1,4)
plot(f,USB_spec)
title("SSB Signal Spectrum (USB)")
xlabel("Frequency")
ylabel("Magnitude")

xgrid();
```


OUTPUT GRAPH:


![WhatsApp Image 2026-04-07 at 11 51 28 AM](https://github.com/user-attachments/assets/3c0fbab6-8eed-4ce2-ad93-32bc795f1bff)
<img width="770" height="508" alt="Screenshot 2026-04-07 115116" src="https://github.com/user-attachments/assets/64ec43a0-41d9-4f8e-b943-57218819abdb" />

Tabulation: 
![WhatsApp Image 2026-04-07 at 11 51 27 AM](https://github.com/user-attachments/assets/b2bb472a-2846-4e4c-8146-6f831e600ee5)

RESULT:
Thus, the SSB-SC-AM Modulation and Demodulation is experimentally done and the output is verified.


