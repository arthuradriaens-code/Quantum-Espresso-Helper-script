# Quantum-Espresso-Helper-script
This is a basic script that will convert a cif file to an in file, already adding the CONTROL, ELECTRON, system parameters and K_points.
The only thing left to do is to add the UPF file names in ATOMIC_SPECIES. Cif2Cell is assumed to be installed
## How to use:

### First make the file executable via
$chmod +x QE_file_prep.sh

### Then follow the following structure:
./QE_file_prep.sh input.cif output.in
