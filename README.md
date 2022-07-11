# NMR_code

This repository contains information on the calculations presented in: A. T. Grigas, Z. Liu, L. Regan, and C. S. O'Hern, ''Core packing of well-defined x-ray and NMR protein structures is the same,'' to appear in Protein Science (2022)

Files:

-xtal_PDBID.txt contains a list of the PDB IDs of the x-ray crystal structures analyzed. These structures have a resolution cutoff of <= 1.8 Angstroms, as well as a 20% sequency identity cutoff. This set was access from the PISCES server: http://dunbrack.fccc.edu/pisces/

-xtal_packing_data.npy is a NumPy array that contains packing data and other features for the x-ray structures, where each row is a different x-ray structure, corresponding to the order in xtal_PDBID.txt. The columns contain the following:

| Average core packing fraction | Fraction core | Number of residues | Percent Ramachandran outliers | Percent Side chain dihedral angle outliers | Clashscore | Bond length outliers | Bond angle outliers

-NMR_PDBID.txt  contains a list of the PDB IDs of the NMR structures analyzed. This includes all available NMR structures on the PDB that have accessible experimental restraint data and are not missing any heteroatoms. Restraint data was accessed using the Python API PyPDB: https://github.com/williamgilpin/pypdb

-nmr_packing_data.npy is a NumPy array that contains packing data and other features for the NMR structures, where each row is a different NMR bundle, corresponding to the order in NMR_PDBID.txt. The columns contain the following, averaged over the bundle were applicable:

| Average core packing fraction | Fraction core | Number of residues | Percent Ramachandran outliers | Percent Side chain dihedral angle outliers | Clashscore | Fraction of backbone chemical shifts assigned | Field strength | Whether RDCs were collected | Bond length outliers | Bond angle outliers | PDB Deposition date
