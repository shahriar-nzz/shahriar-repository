# GPS Satellite Position Calculator

This project calculates the position of GPS satellites over a given time period using broadcast ephemeris data from a RINEX 3.02 Navigation file. The results include both ECI (Earth-Centered Inertial) and ECEF (Earth-Centered Earth-Fixed) coordinates.

## 📌 Project Goals

- Parse RINEX 3.02 navigation files
- Select nearest ephemeris for each epoch
- Compute satellite position in ECI frame
- Convert ECI to ECEF using Earth rotation
- Visualize orbital trajectories in 3D

## 📁 Files in this Repository

- `main.ipynb` – Main script for loading navigation data and computing positions
- `GODS00USA_R_20240010000_01D_GN.rnx` – Sample RINEX 3.02 navigation file (or your own file)
- `correct orbit shape.jpg` – corect shape of gps orbit
- `what i got.png` – what i got
- `README.md` – This description file

## ⚙️ How It Works

1. **Load Navigation Data:** RINEX file is parsed and stored in a structured dictionary format.
2. **Choose Ephemeris:** For each desired epoch, the closest `toe` (time of ephemeris) is selected.
3. **Compute Satellite Position:** Using Keplerian orbital parameters and time difference `tk`.
4. **Convert to ECEF:** Account for Earth's rotation using Greenwich sidereal time (GST).
5. **Plot Results:** ECI and ECEF trajectories are plotted to validate correctness.

## 🛰️ Sample Output

- 3D plots of satellite orbits in ECI and ECEF frames
- Smooth trajectories when using consistent ephemeris data

## 📦 Requirements

- Python 3.8+
- NumPy
- Matplotlib or Plotly
- datetime

Install dependencies with:

```bash
pip install -r requirements.txt
