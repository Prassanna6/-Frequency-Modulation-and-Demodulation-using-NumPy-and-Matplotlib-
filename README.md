# -Frequency-Modulation-and-Demodulation-using-NumPy-and-Matplotlib-

__Aim:__

To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries.

__Apparatus Required:__ 

1. Software: Python with NumPy and Matplotlib libraries
   
2. Hardware: Personal Computer

 
__Theory:__

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its 
frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier 
wave is varied according to the instantaneous amplitude of the message signal.

__Algorithm:__

1. Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and 
   frequency deviation.
   
2. Generate Time Axis: Create a time vector for the signal duration.
    
3. Generate Message Signal: Define the message signal as a cosine wave.
    
4. Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
    
5. Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
 
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

__Programme:__

```
import numpy as np
import matplotlib.pyplot as plt

am = 10.3
fm = 386
fs = 38600

t = np.arange(0, 2/fm, 1/fs)

m = am * np.cos(2 * np.pi * fm * t)
plt.subplot(3,1,1)
plt.plot(t, m)

ac = 20.6
fc = 3860

c = ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3,1,2)
plt.plot(t, c)

b = 6.7

s = ac * np.cos(2 * np.pi * fc * t + np.sin(2 * np.pi * fm * t))
plt.subplot(3,1,3)
plt.plot(t, s)
plt tight_layout()

```

__Output:__

<img width="1080" height="704" alt="image" src="https://github.com/user-attachments/assets/60a32836-5b1c-40a2-adf3-baaaab691e99" />

__Tabulation:__

![WhatsApp Image 2026-04-09 at 1 29 55 PM](https://github.com/user-attachments/assets/0931ab7c-b9fa-4296-861c-d264698ac1e3)



__Result:__
Thus, the FM frequency modulation signal is generated using python
