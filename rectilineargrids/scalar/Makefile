# Edit the following variables as needed
HDF_INSTALL = $(HDF5_DIR)
EXTLIB = -L$(HDF_INSTALL)/lib
CC          = g++
CFLAGS      = 
LIB         = -L$(MAALI_SZIP_HOME)/lib -lsz -L$(MAALI_ZLIB_HOME)/lib -lz -ldl -lm

INCLUDE   = -I$(HDF_INSTALL)/include
LIBSHDF   = $(EXTLIB) $(HDF_INSTALL)/lib/libhdf5.a 

all: scalar

scalar: scalar.cpp
	$(CC) $(CFLAGS) -o $@ scalar.cpp $(INCLUDE) $(LIBSHDF) $(LIB)


clean: 
	rm -f *.h5 *.o \
        scalar\
 
.SUFFIXES:.o.cpp
