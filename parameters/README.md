# Parameter Sets

### First-Time Setup

- Download pulse sequences from the [experiments](https://github.com/viochemist/nmr-relaxation/tree/main/experiments) folder and put them in the source directory for pulse programs. e.g.

      C:\Bruker\TopSpin4.4.0\exp\stan\nmr\lists\pp\user

- Download parameter sets from the [parameters](https://github.com/viochemist/nmr-relaxation/tree/main/parameters) folder (the entire directories) and put them in the source directory for parameter sets. e.g.

      C:\Bruker\TopSpin4.4.0\exp\stan\nmr\par\user
  
- Download shape pulses from the [shapes](https://github.com/viochemist/nmr-relaxation/tree/main/shapes) folder and put them in the source directory for shape files. e.g.

      C:\Bruker\TopSpin4.4.0\exp\stan\nmr\list\wave\user
      
- In TopSpin, open `edprosol` and update shapes 6 and 7 for the 15N decoupler channel (see the [shapes](https://github.com/viochemist/nmr-relaxation/tree/main/shapes/README.md) folder here for more details)
  - This step requires some administrative priveleges. The default password is 'topspin' but this may have been changed by NMR facility staff. Please implement only new experiments only under appropriate supervision.

- Run `paracon`, select the 4 relaxation parameter sets, and `Execute`

  ![image](https://github.com/user-attachments/assets/195f5d15-f553-476d-aa1a-d92ab00042c7)

### Routine Experiment Setup

- Create a new dataset and select the desired relaxation parameter set. Or, in an existing dataset run `rpar`.

  ![image](https://github.com/user-attachments/assets/28fb80ea-7ced-4b3b-a88f-cf0ec3ec876c)

- Run `getprosol` and `gppp` and update p1 value
  - Option 1) use `getprosol 1H <p1> <plw1>W` with optimized pulse width measured separately (e.g. `getprosol 1H 8.7 13W`)
  - Option 2) run `pulsecal`
- Edit `vdlist` (*R*<sub>1</sub>) or `vplist` (*R*<sub>1ρ</sub>), update `p35`

  ![image](https://github.com/user-attachments/assets/059b3211-bd86-4d8e-ba85-b3e124fefd7a)

- Update `O1P`, `SW`, `TD`, `NS`, `D1`, etc., as desired
