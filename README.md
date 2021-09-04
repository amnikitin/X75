# X75
Force Field generator for molecular mechanics


                  Alexei Nikitin


# Installation

Unpack the archive.

In parallel with the X75 folder, create an ORCA folder, in which to place the ORCA 4.2.1 package.
https://orcaforum.kofo.mpg.de

Edit the job_control.txt file to specify a valid path to chargemol\atomic_densities\. 



# Usage

Place the model of the molecule in the model.xyz file in the xyz/xmol format:

 The number of atoms.
 
 Empty string or comment.
 
 Element  x y z  charge or comment or nothing.
 
 ...


In FF.cfg file, specify the dielectric constant of the medium and the total integer charge of the model.
You should not remove lines or insert new ones.
It is not recommended to edit the "System:" section. 

If the total charge is zero, run the 0.run.bat.

If not, then run the -1.bat.
After completing its work, change zero to the correct charge in the MyMol.wfx file

<Net Charge> 
0.0 
</Net Charge> 

then run the -2.bat


The output of the program is in the "res" folder.
Models of molecules with partial charges on atoms are in the A_PDC.mlm file 
in .mlm format http://www.biomolecular-modeling.com/Abalone/index.html
Force field in the "ForceField" folder.



