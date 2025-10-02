# Lat/Lon → Relative UTM Coordinates

This project demonstrates how to convert an interferometer array’s site list
from **latitude/longitude (WGS84)** into **relative UTM coordinates (meters)**
with respect to a center antenna.  
The example here uses the **Square Kilometre Array (SKA)**, but the method
applies to any telescope array if lat/lon are provided.

---

## Requirements

```text
numpy
utm
pyproj
# (optional) pandas — if you load from CSV/XLSX into a DataFrame
```

Install:

```bash
pip install numpy utm pyproj
# and, if needed:
pip install pandas
```
---

## Data description

- **ska.xlsx** (512): full information of SKA array, but the codes only using 296 stations as example:
                     `data.values[2:298]` — each row is `[lon_deg, lat_deg]`.
- **Center antenna** (1): `data.values[1:2]` — used as the origin.
- ska_centre.txt: save the output of codes to use in other codes.

> Adjust the slices and column order if your table differs.  
> Example load (commented below) is `pandas.DataFrame` named `data`.

---

## License

Use and adapt freely for research/education. Please cite your array/site-list
source as appropriate.
