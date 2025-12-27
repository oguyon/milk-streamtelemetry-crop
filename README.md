# milk-streamtelemetry-crop
Crop telemetry FITS files

## Usage

```
milk-streamtelemetry-crop <infile> <outfile> x0 x1 y0 y1
```

## Description

Crops the first 2 axes of 3D FITS cubes. The crop window is specified with start and end for respectively the first (x0,x1) and second (y0,y1) axes.
The input must be a 3D FITS file. The output file will be a 3D FITS cube will all FITS header keywords unchanged from the input, except for NAXIS1 and NAXIS2.


## Compilation

The program is written in C, uses the FITSIO library to read and write cubes. Compilation is performed with cmake and gcc.

```
mkdir build
cd build
cmake ..
make
```

## Details

The FITSIO extended file syntax is used to read the crop region of the input FITS file.
