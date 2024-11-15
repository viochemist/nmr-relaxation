# Adiabatic Half Passages for R1rho Relaxation

Save these files in the appropirate shape pulse folder in the Bruker TopSpin directory. This is typically called 'wave/user'. Example, on PC it is:

    C:\Bruker\TopSpin4.4.0\exp\stan\nmr\lists\wave\user

In TopSpin, edit the prosol table using 'edprosol'. 

Select the "HR Shape Pulses" tab and "15N" under the Decouple dropdown menu. 

Double-click the filename column next to shape #6 ("T1rho, ramp down") and choose "AHP-2m-XtoZ-Hi2Lo.4000". Set the pulsewidth to 2000 μs.

![image](https://github.com/user-attachments/assets/999b58fc-3f75-4bec-b233-ef04968fe285)

Repeat this for shape #7, "T1rho, ramp up" and choose "AHP-2m-ZtoX-Lo2Hi.4000". 

Calculate the power level to be 2 kHz, or whatever is recommended for your system.
- Under the dropdown 'View' -> 'View Mode for Power' select 'Power / Watt'
- Using the 15N pulse width and power in the 90 deg. Pulses tab, calculate the power level for 2 kHz
   - e.g. With the high power nitrogen being 32 μs at 100W: 100W * (32 / 125) ^ 2 = 6.5536 W
- Add this value to the last column of shape #6 and shape #7

        NOTE: The 2ms shape is appropriate only for 1 kHz and above. For lower power, the 4ms shape will be necessary.

The shapes can now be read into the *R*<sub>1ρ</sub> pulse sequence automatically using `getprosol` or `pulsecal`. 
