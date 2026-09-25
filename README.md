# FASTV7_Compiled

This repository contains the code that allows for easy compilation of FAST V7 with latest `gfortran` compiler.
The source of this codebase can be found here [here](https://github.com/old-NWTC) and [here](https://www.nrel.gov/wind/nwtc/fastv7.html)

## Compiling instructions

- Clone this repository
- `cd FASTV7_Compiled/FASTV7/Compiling`
- make

This would result in an executable named `FAST_glin64`.

## Reading output

The output file of FASTV7 gives an error when read using pandas as it uses an older encoding.
The following code can be used to read the output.

```python
import pandas as pd
outfile = "openfast.out"
df = pd.read_csv(outfile,encoding="cp437",sep=r"\s+",skiprows=[0,1,2,3,4,5,7])
```
