# FM-using-Python

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program

import numpy as np

import matplotlib.pyplot as plt


am = 6.8

fm = 574

ac = 13.6

fc = 5740

fs = 57400

beta = 5.8

t = np.arange(0, 2/fm, 1/fs)


m = am * np.cos(2 * np.pi * fm * t)

plt.subplot(3,1,1)

plt.plot(t, m)


c = ac * np.cos(2 * np.pi * fc * t)  
plt.subplot(3,1,2)  
plt.plot(t, c)  

efm = ac * np.cos(2 * np.pi * fc * t + beta * np.sin(2 * np.pi * fm * t))

plt.subplot(3,1,3)

plt.plot(t, efm)

plt.title("FM")

plt.tight_layout()
plt.show()

Output Waveform
![08a8df5e-8d3c-4399-870b-d67e30bad81b](https://github.com/user-attachments/assets/a3f3a544-fe5d-4dcd-95be-4e1015b858e5)

Tabular Column

![45be3af8-0058-43f8-ab0b-6a03ae15bc91](https://github.com/user-attachments/assets/5142d49c-6e9e-48f2-9f5f-2e79ef5ae78a)

Calculation

![068511e2-54c9-4431-b0f8-714938e6bb72](https://github.com/user-attachments/assets/18dc2b3e-87d6-4dde-8845-2d9ddff00eb1)


Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
