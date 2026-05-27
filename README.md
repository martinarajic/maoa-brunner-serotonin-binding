This repository contains the files necessary to reproduce the computational results reported in the manuscript:

Rajić M, Stare J, Vrban Đerek L, Sollner Dolenc M, Mavri J, Vianello R.  
Elucidating the Molecular Basis of Brunner Syndrome: How Clinically Relevant Mutations Disrupt Serotonin Binding and Active-Site Stability in MAO-A.

#### REPOSITORY STRUCTURE

```text
maoa-brunner-serotonin-binding/
├── DOCKING/
│   ├── Harmine_validation/
│   ├── Mutants_validation/
│   └── MAOA_docking/
└── MD/
    ├── CRYSTAL/
    │   ├── WT/
    │   ├── V244I/
    │   ├── E446K/
    │   ├── C266F/
    │   └── R45W/
    ├── MINIMIZED/
    │   ├── WT/
    │   ├── V244I/
    │   ├── E446K/
    │   ├── C266F/
    │   └── R45W/
    ├── NEUTRAL/
    │   ├── WT/
    │   ├── V244I/
    │   ├── E446K/
    │   ├── C266F/
    │   └── R45W/
    └── INPUTS/
```
#### DOCKING

##### Harmine Validation
This folder contains files used to validate the docking protocol by re-docking the co-crystallized ligand harmine into the MAO-A active site. 

##### Mutants Validation
The folder contains docking files used to validate the crystal-based protocol, in which the WT MAO-A structure with docked SRO serotonin was used as the starting structure for generating the mutant systems.

##### MAOA Docking
This folder includes docked structures of both serotonin protonation states, SRP and SRO, together with the corresponding MAO-A structures. 
These serotonin-bound wild-type structures were used as the starting structures for the main crystal-based protocol. 
The WT MAO-A structure with docked serotonin was used to generate the mutant structures in Chimera.
The resulting mutant systems were then used as starting structures for MD simulations.

#### MD
This folder contains files required to run MD simulations in AMBER 22.3.
This includes AMBER coordinate files (.coord), topology files (.prmtop), MD input files, and PDB structures used for preparing and running the simulations.

##### CRYSTAL
This folder contains systems prepared using the crystal-based protocol.
In this protocol, serotonin was first docked into the wild-type crystal structure of MAO-A.
The WT MAO-A structure with docked serotonin was used to generate the mutant structures in Chimera.
This protocol was used as the main production setup for comparing the effect of mutations starting from the same binding pose.

##### MINIMIZED
This folder contains systems used to validate the crystal-based protocol.
Here, each WT or mutant MAO-A structure was prepared separately, minimized, and then docked with serotonin.
These files were used to check that serotonin adopts a comparable binding pose to the one obtained in the crystal-based protocol.

##### NEUTRAL
This folder contains MD simulation files for the neutral form of serotonin.

##### INPUTS
The INPUTS folder contains general input files used for system preparation, equilibration, and production MD simulations in AMBER.

##### NOTES
Large trajectory files are not included due to file-size limitations and are available from the corresponding author upon reasonable request. 
Representative structures, input files, docking files, and selected outputs are provided to document the computational workflow and enable reproduction of the docking and MD simulations described in the manuscript.
