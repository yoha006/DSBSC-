# DSBSC


EX NO: 2	DSB-SC-AM MODULATOR AND DEMODULATOR

AIM:

To write a program to perform DSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

EQUIPMENTS REQUIRED

•	Computer with i3 Processor
•	SCI LAB

Note: Keep all the switch faults in off position

Algorithm:

1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the message signal.
•	Amplitude: Maximum amplitude of the message signal.
2.	Generate Signals:
•	Message Signal: A sinusoidal signal that will be modulated.
•	Carrier Signal: A high-frequency sinusoidal signal used for modulation.
3.	DSBSC Modulation:
•	Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
4.	DSBSC Demodulation:
•	Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components).
•	Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
5.	Visualization:
Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation.
PROCEDURE

•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
 
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform

Model Waveform

<img width="703" height="679" alt="image" src="https://github.com/user-attachments/assets/e7c7c7f8-ccf2-41ac-b1f3-325989941a6f" />

Program
```
Am=8.65;
fm=1521;

fc=15210;
fs=152100;
t=0:1/fs:2/fm;
Ac=12.975;

em=Am*cos(2*3.14*fm*t);
subplot(3,1,1);
plot(t,em);
ec=Ac*cos(2*3.14*fc*t);
subplot(3,1,2);
plot(t,ec);
eam1=(Ac+em).*cos(2*3.14*fc*t);

eam2=(Ac-em).*cos(2*3.14*fc*t);
eDSBSC=eam1-eam2;
subplot(3,1,3);
plot(t,eDSBSC);
```


Output Graph
<img width="610" height="460" alt="WhatsApp Image 2026-06-07 at 16 41 13" src="https://github.com/user-attachments/assets/d8f31943-dfcc-4a1e-b529-502b15521fb6" />




Tablular Column
<img width="1599" height="899" alt="image" src="https://github.com/user-attachments/assets/72d0f936-1018-48c2-91aa-f667e77df850" />


Result

Thus the DSB-SC-AM Modulation and Demodulation is generated.

