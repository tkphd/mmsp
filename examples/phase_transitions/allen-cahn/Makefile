# Makefile
# GNU makefile for example Allen-Cahn model code
# Questions/comments to gruberja@gmail.com (Jason Gruber)

# includes
incdir = ../../../include

# compilers/flags
compiler = g++
pcompiler = mpic++
flags = -O3 -I $(incdir)
pflags = $(flags) -include mpi.h

# the program
allen-cahn: allen-cahn.cpp
	$(compiler) $(flags) $< -o $@ -lz

parallel: allen-cahn.cpp
	$(pcompiler) $(pflags) $< -o $@ -lz

clean:
	rm -f allen-cahn parallel
