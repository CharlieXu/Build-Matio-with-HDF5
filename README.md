# Build-Matio-with-HDF5
how to build Matio with HDF5

1. change the <configure> file at line 15831:
# Check whether --with-hdf5 was given.
if test "${with_hdf5+set}" = set; then :
  withval=$with_hdf5; HDF5_DIR=${withval}
else
  HDF5_DIR=/usr/local
fi

point the HDF%_DIR to the local install dir. 

2. line 15857
	HDF5_CFLAGS="-I/usr/local/include"
	HDF5_LIBS="-L/usr/local/lib -lhdf5 -lszip -lm -lz -ldl"
  
  change the -L and -I, and add some -l option to make the -lhdf5 work. 
  
  3. :) see the configure file as example
  
