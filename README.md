# Gromacs-CIF
In the Protein Data Bank (PDB), the PDB format stands as the major file format for protein structures. However, there are certain intrinsic limitations in the PDB format, such as the storage of structural information in a fixed-width format that would be an issue for very large protein complexes. Therefore, the CIF (Crystallographic Information Framework) format has been proposed, which is characterized by superior expansibility. GROMACS, a widely used software suite for molecular dynamics simulations, presently only supports the PDB format. In this study, we have modified the source code of GROMACS, which enables it to support the CIF format structure files as input and subsequently generate molecular topology files. This work would simplify the pre-processing of large protein complexes for MD simulations.

# Installation
1. Download Gromacs 2023.1 version in https://manual.gromacs.org/
2. Replace Gromacs' source files with files in ..\src

   filetypes.h    ——    ..\api\legacy\include\gromacs\fileio\filetypes.h
   
   pdbio.h       ——     ..\api\legacy\include\gromacs\fileio\pdbio.h
   
   filetypes.cpp   ——   ..\src\gromacs\fileio\filetypes.cpp
   
   confio.cpp    ——     ..\src\gromacs\fileio\confio.cpp
   
   pdbio.cpp     ——     ..\src\gromacs\fileio\pdbio.cpp
   
3. Follow Gromacs' installation steps

# Usage
Run "gmx pdb2gmx -f x.cif -o x.gro -p x.top -i x.itp"

# Development
All modified parts in source files are surrounded with "//Gromacs-CIF"

# Citation
DOI: https://doi.org/10.1101/2023.09.01.555884

# Author
Hengyue Wang & Zhiyong Zhang
