# SKA Array: Lat/Lon → Relative UTM Coordinates

This project demonstrates how to convert an interferometer array’s site list
from **latitude/longitude (WGS84)** into **relative UTM coordinates (meters)**
with respect to a center antenna.  
The example here uses the **Square Kilometre Array (SKA)**, but the method
applies to any telescope array if lat/lon are provided.

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
