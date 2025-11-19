# FM-using-Python
![be6fb90b-7add-4fc6-898b-57ff09018247](https://github.com/user-attachments/assets/00c2afee-ef00-41b1-bec2-ee4aa0f5bca8)# FM-using-Python

Aim

@@ -27,16 +27,44 @@ Algorithm
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
![734f21aa-051c-4bd7-8ff9-414b02aab1e2](https://github.com/user-attachments/assets/205253de-65c2-4e43-a383-a812becf10f5)


Tabular Column
![Uploading be6fb90b-7add-4fc6-898b-57ff09018247.jpg…]()



Calculation
![b33a7294-0583-40af-b102-044caed94a81](https://github.com/user-attachments/assets/77bd2c21-614b-4252-923e-908810b99ee5)

