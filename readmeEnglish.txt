input：inputMieDISORT.txt
output：brfMieDISORT.txt, albedoMieDISORT.txt
platform：on a windows computer，double click runMieDISORT.bat to run MieDISORT.exe

inputMieDISORT.txt is a Fortran namelist file. In this input file, we have

1. radius: equivalent radius of snow particles from 10 to 3000 um. If it's set to 0, all radii at interval of 10 um for <1000 um and at 100 um for >1000 um are used.
2. wavelength: wavelength from 0.3 to 2.5um. If it's set to 0, all wavelenth are used.
3. shapeTyp: snow grain shape, 1 for sphere, 2 for spheroid，3 for hexagonal plate, 4 for koch snowflake. LUT of single scattering properties are identical to SNICAR.
4. irrDir: direct irradiance fraction from 0 to1. Default is 0.
5. sza: solar zenith angle from 0 to 90. Default is 0.
6. PHI0: solar azimuth angle from 0 to 360. Default is 0.

specify sequential equally-spaced angles：
7. NUMU:  number of viewing zenith angle, such as 91 for 1 degree resolution.
8. NPHI: number of viewing azimuth angle, such as 181 for 1 degree resolution.
in this case, parameters 9 and 10 are invalid.

or arbitrary geometries：
7. NUMU: number of viewing zenith angle, but in negative presentation, such as -91.
8. NPHI: number of viewing azimuth angle, but in negative presentation, such as -181.
9. iUMU: viewing zenith angles in decending order.
10. iPHI: viewing zenith angles

11. optD: optical depth of snowpack. Default is 30000.
12. ALBEDO: underlying ground albedo. Default is 0.
13. NSTR: number of streams. Default is 1.

