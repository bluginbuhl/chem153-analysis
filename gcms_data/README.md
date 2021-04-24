# Raw GC-MS Data Key

## Method details

`MTBEC.M`: method file for GC-MS instrument

GC oven method info is contained in `GC5890.MTH`

## Sample Key

| Sample Name | Details    |
|:------------|:-----------|
| C153AC1A    | Standard 1 |
| C153AC2A    | Standard 2 |
| C153AC3A    | Standard 3 |
| C153AG1     | Gasoline 1 |
| C153AG2     | Gasoline 2 |
| C153AG3     | Gasoline 3 |

### ANDI format (.CDF)

`/andi_format`: raw data in CDF format - can be read using [PyMassSpec](https://pymassspec.readthedocs.io/en/master/index.html)

```python
from pathlib import Path
from pyms.GCMS.IO.ANDI import ANDI_reader

andi_file = Path('/path/to/andi_file.CDF')

data = ANDI_reader(andi_file)

# returns a `GCMS_data` object
```

### Proprietary format (.D, .MS)

`/proprietary_format`: raw data from insturment - can be viewed using [OpenChrom](https://lablicate.com/platform/openchrom)