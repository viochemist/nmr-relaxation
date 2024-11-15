# Adiabatic Half Passages for R1rho Relaxation

Save these files in the appropirate shape pulse folder in the Bruker TopSpin directory. This is typically called 'wave/user'. Example, on PC it is:

    C:\Bruker\TopSpin4.4.0\exp\stan\nmr\lists\wave\user

In TopSpin, edit the prosol table using `edprosol`. 

Under the dropdown menu "View" $\rightarrow$ "View Mode for Power" select "Power / Watt"

Select the "HR Shape Pulses" tab and "15N" under the Decouple dropdown menu. 

![image](https://github.com/user-attachments/assets/d732d811-1c1c-456a-87e4-e61417281102)

Double-click the filename column next to shape #6 ("T1rho, ramp down") and choose "AHP-2m-XtoZ-Hi2Lo.4000". Set the pulsewidth to 2000 μs.

![image](https://github.com/user-attachments/assets/999b58fc-3f75-4bec-b233-ef04968fe285)

Repeat this for shape #7, "T1rho, ramp up" and choose "AHP-2m-ZtoX-Lo2Hi.4000". 

Go to the `HR Square Pulses` tab and find #15 (T1rho) for the 15N decouple channel.

  ![image](https://github.com/user-attachments/assets/e4cc3658-c010-4414-b25f-6e41953c59c8)

Note the power level in the last column and copy this to shapes #6 and #7 that you created.

        NOTE: Work with an appropriate staff or NMR manager when implementing new experiments and shapes. 
        Use the recommended power level specified in the `HR Square Pulses` prosol table. This is typically 
        2kHz (pulsewidth 125μs) but may vary depending on the field and probe. The 2ms shape is appropriate 
        only for 1 kHz and above. For lower power, the 4ms shape will be required.

The shapes can now be read into the *R*<sub>1ρ</sub> pulse sequence automatically using `getprosol` or `pulsecal`. 
