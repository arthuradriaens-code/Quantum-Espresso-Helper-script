# qeconvert
This is a basic script that will convert a cif file to an in file, already adding the CONTROL, ELECTRON, system parameters and K_points.
The only thing left to do is to add the UPF file names in ATOMIC_SPECIES. Cif2Cell is assumed to be installed,
it now also has the option to make a supercell.
### How to use:

#### First make the file executable via
$chmod +x qeconvert

#### Then follow the following structure:
./qeconvert input.cif output.in

#### or (for supercells)
./qeconvert input.cif output.in scalex scaley scalez

#### or (for supercells with vacuum)
./qeconvert input.cif output.in scalex scaley scalez vacuumx vacuumy vacuumz

#### and even supercells surfaces (e.g 110) with vacuum
see ./qeconvert -h

### How to use: extra
If you forget how to use it, I added a help entry, so just
start the program with the -h flag as "qeconvert -h".

### advice
Put this file in a directory listed in your path so it can 
just be called from anywhere like "qeconvert ..."

### Known problems
When making the cif file yourself, you generally don't have an author added, this screws up the formatting a bit (it still works tho)



## FindVol.sh
Basic script that will simulate for different volumes after which you get a file VolVsE.txt, this file can then be used by ev.x

### How to use:

#### First make the file executable via
$chmod +x RelaxCrystal.sh

#### Then follow the following structure:
RelaxCrystal.sh file.in \<relative x length\> \<relative y length\> \<relative z length\>


## FindVolMultiCore.sh
Same as RelaxCrystal but will spam all your cores

### How to use:
same as RelaxCrystal.sh
