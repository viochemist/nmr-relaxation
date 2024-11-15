# Parameter Sets

### Setup

- Download pulse sequences, put them in the source directory for pulse programs (e.g., `C:\Bruker\TopSpin4.4.0\exp\stan\nmr\lists\pp\user`)
- Download parameter sets, put them in the source directory for parameter sets (e.g., `C:\Bruker\TopSpin4.4.0\exp\stan\nmr\par\user`)
- Download shape pulses, put them in the source directory for shape files (e.g., `C:\Bruker\TopSpin4.4.0\exp\stan\nmr\list\wave\user`)
- In topspin, open `edprosol` and update shapes 6 and 7 for the 15N decoupler channel (see the `shapes` folder here for more details)
- Run `paracon`, select the 4 relaxation parameter sets and `execute`
- Create a new datset and run `rpar` and load the desired relaxation parameter set
- Run `getprosol` and `gppp` and update p1 value
  - Option 1) use `getprosol 1H <p1> <plw1>W` with optimized pulse width measured separately (e.g. `getprosol 1H 8.7 13W`)
  - Option 2) run `pulsecal`
- Edit `vdlist` (*R*<sub>1</sub>) or `vplist` (*R*<sub>1ρ</sub>), update `p35`
- Update `o1`, `SW`, `TD`, `NS`, `d1`, etc., as desired
