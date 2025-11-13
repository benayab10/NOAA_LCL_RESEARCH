README
This script loads MPLNET lidar data and surface meteorological data, converts all timestamps into standard datetimes, calculates the lifting condensation level (LCL), and plots the LCL on top of an NRB (Normalized Relative Backscatter) time–height plot.
What the script does


Opens an MPLNET .nc4 netCDF file


Converts the MPLNET Julian time variable into normal Python datetime values


Reads a surface meteorological file (met.2012.dat)


Converts year + Julian day + decimal hour into timestamps


Computes dewpoint and LCL from the met data


Creates a pcolormesh plot of NRB vs. altitude vs. time


Overlays the LCL as scatter points


(Optional) Reads a CSV of hourly LCL values for comparison


Displays the final figure


Requirements


Python 3


netCDF4


numpy


pandas


matplotlib


Install missing libraries with:
pip install netCDF4 numpy pandas matplotlib

Input Files


MPLNET netCDF file


Surface met data met.2012.dat


Optional: lcl_output_hourly.csv


How to run
Update the file paths inside the script, then run:
python your_script_name.py

Output


A time–height plot showing:


NRB as a color mesh


LCL values plotted on top



