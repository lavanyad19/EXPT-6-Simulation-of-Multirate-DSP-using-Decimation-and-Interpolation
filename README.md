# EXPT-6-Simulation-of-Multirate-DSP-using-Decimation-and-Interpolation

# AIM: 

 To perform and verify Multirate-DSP-using-Decimation-and-Interpolation.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clear;
clc;
close;

// Generate the original signal
n = 0:%pi/50:2*%pi;
x = sin(%pi * n);

// Input factors
M = input("Enter the Downsampling Factor (M): ");
L = input("Enter the Upsampling Factor (L): ");

//-------------------------
// Downsampling
//-------------------------
downsampling_x = x(1:M:length(x));

disp(x, "Input Signal x(n) = ");
disp(downsampling_x, "Downsampled Signal = ");

// Plot Original and Downsampled Signals
figure(1);

subplot(2,1,1);
plot2d3(1:length(x), x);
xtitle("Original Signal");

subplot(2,1,2);
plot2d3(1:length(downsampling_x), downsampling_x);
xtitle("Downsampled Signal by a Factor of M");

//-------------------------
// Upsampling
//-------------------------
upsampling_x = zeros(1, L * length(x));

for i = 1:length(x)
    upsampling_x(1, L*i) = x(i);
end

disp(x, "Input Signal x(n) = ");
disp(upsampling_x, "Upsampled Signal = ");

// Plot Original and Upsampled Signals
figure(2);

subplot(2,1,1);
plot2d3(1:length(x), x);
xtitle("Original Signal");

subplot(2,1,2);
plot2d3(1:length(upsampling_x), upsampling_x);
xtitle("Upsampled Signal by a Factor of L");
```

# OUTPUT: 
<img width="757" height="692" alt="WhatsApp Image 2026-09-02 at 8 30 49 AM" src="https://github.com/user-attachments/assets/e1f052e0-fa59-4259-b560-9bdc008d7508" />

<img width="758" height="690" alt="WhatsApp Image 2026-09-02 at 8 30 22 AM" src="https://github.com/user-attachments/assets/8c85e96d-780e-4bd6-90ea-af13aeb60233" />


# RESULT: 
Thus the Multirate-DSP-using-Decimation-and-Interpolation using python was performed and verified.
