# Adiabatic Half Passages for R1rho Relaxation

Save these files in the appropirate shape pulse folder in the Bruker TopSpin directory. This is typically called 'wave/user'. Example, on PC it is:

    C:\Bruker\TopSpin4.4.0\exp\stan\nmr\lists\wave\user

In TopSpin, edit the prosol table using 'edprosol'. Select the "HR Shape Pulses" tab and "15N" under the Decouple dropdown menu. Press the "..." for shape #6, "T1rho, ramp down" and choose "AHP-2m-XtoZ-Hi2Lo.4000". Repeat this for shape #7, "T1rho, ramp up" and choose "AHP-2m-ZtoX-Lo2Hi.4000". Use 2ms for the pulsewidth of each. The power level should be calculated automatically. The shapes can now be read into the R1rho pulse sequence using "getprosol". 
