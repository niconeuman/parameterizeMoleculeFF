# Files
The structure of the molecule has to be provided in the "initial.xyz" file, which contains the number of atoms, followed by a comment line and the atomic coordinates in angstroms. The names of the files can be changed, while paying attention to the corresponding names in the files. 
## Important variables in the Compound Script
The variables in scanArray[i] are strings containing
'''
%geom scan B AtomA AtomB [bl1 bl2 bl3 bl4 bl5] end end
'''
or
'''
%geom scan A AtomA AtomB AtomC [a1 a2 a3 a4 a5] end end
'''
The length of the scanArray array is nScans, and it has to match the number of elements provided by the user.
## Recommendations on setting up the scans
The numbering of the atoms starts from 0, and the atoms have to be manually identified in the desired molecule by the user, as well as the ranges of atomic distances and angles. It is recommended to have the center value in each scan to be the equilibrium value in the optimized structure of the molecule. The scan steps should be small, to allow fitting with a quadratic expression for the energy (harmonic approximation). 0.05 A steps for bond lengths and 5 º steps for angles are a good starting point. More steps in each scan can be added to get a more accurate energy profile, but the user has to be careful not to input unphysical values that may cause a failure in the optimization and the whole calculation to be interrupted.

