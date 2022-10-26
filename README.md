# Quantum-Espresso-Helper-scripts
## QE_file_prep.sh
This is a basic script that will convert a cif file to an in file, already adding the CONTROL, ELECTRON, system parameters and K_points.
The only thing left to do is to add the UPF file names in ATOMIC_SPECIES. Cif2Cell is assumed to be installed
### How to use:

#### First make the file executable via
$chmod +x QE_file_prep.sh

#### Then follow the following structure:
./QE_file_prep.sh input.cif output.in

### Known problems
When making the cif file yourself, you generally don't have an author added, this screws up the formatting a bit (it still works tho)


## RelaxCrystal.sh
Basic script that will simulate for different volumes after which you get a file VolVsE.out, this file can then be used by ev.x

### How to use:

#### First make the file executable via
$chmod +x RelaxCrystal.sh

#### Then follow the following structure:
RelaxCrystal.sh file.in <relative x length> <relative y length> <relative z length>
