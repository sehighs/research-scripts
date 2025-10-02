# Light-cone Chunks → Power Spectra (with Powerbox)

This mini-tool slices a 21 cm **light-cone cube** (3D array) into **chunks**
along the line-of-sight and computes the **power spectrum** of each chunk using
[`powerbox`](https://powerbox.readthedocs.io/).

Typical 21 cm use cases:
- **Frequency-based slicing** (e.g., bandwidth chunks for interferometers; in a
  50–350 MHz cone, slice every 8 MHz).
- **Redshift-based slicing** (fixed Δz).
- The light-cone’s LoS coordinate is assumed to be gridded in **comoving
  distance**, _not_ redshift or frequency. Chunk functions therefore return
  **slice indices** corresponding to comoving-distance positions.

---

## What the code does

1. **Build slice indices** along LoS from either:
   - a **frequency scheme** `chunk_indices_fre(...)`, or
   - a **redshift scheme** `chunk_indices_redshift(...)`.
2. **Compute power spectra** of each chunk with `powerbox.tools.get_power`,
   returning binned `P(k)` and `Δ²(k) = k³ P(k) / (2π²)` for each chunk.

---

## License

Use and adapt freely for research/education. Please cite your array/site-list
source as appropriate.
