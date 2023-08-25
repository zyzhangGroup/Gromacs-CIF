# Gromacs-CIF
Modify Gromacs enabling CIF file supporting

# Installation
1. Download Gromacs 2023.1 version in https://manual.gromacs.org/
2. Replace Gromacs' source files with files in ..\src

   filetypes.h    ——    ..\api\legacy\include\gromacs\fileio\filetypes.h
   
   pdbio.h       ——     ..\api\legacy\include\gromacs\fileio\fpdbio.h
   
   filetypes.cpp   ——   ..\src\gromacs\fileio\filetyoes.cpp
   
   confio.cpp    ——     ..\src\gromacs\fileio\confio.cpp
   
   pdbio.cpp     ——     ..\src\gromacs\fileio\pdbio.cpp
   
4. Follow Gromacs' installation steps

# Usage
Run "gmx pdb2gmx -f x.cif -o x.gro -p x.top -i x.itp"
