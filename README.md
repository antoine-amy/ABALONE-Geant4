
<table align="center"><tr><td align="center" width="9999">

# Geant4 - an Object-Oriented Toolkit for Simulation in HEP
## ABALONE photosensor

</td></tr></table>

----------------------------------------------------------------------------------------------------------------------------------------------------------------

## Building the simulation from source code:
```
mkdir build
cd build
sudo cmake -DGeant4_DIR=<Your Geant4 install Directory (like /usr/share/geant4/geant4.10.07-install/lib/Geant4-10.7.1/)> <Your Directory>ABALONE_GEANT4/GEANT4
sudo make install -jN && sudo make
```

----------------------------------------------------------------------------------------------------------------------------------------------------------------

## Before running the simulation:

- Change the save directory of the output files in the code in both ```ABEventAction.cc``` and ```ABEventAction.hh```.

- Import the electric fields:
```
mkdir E_fields
cd E_fileds
cp <directory of the electric fields from COMSOL>
```
and change the directory of the electric field map in the file ```ABElectricField.cc```.

Below the folder structrue for reference:

    My Directory
    │  
    ├── build
    ├── GEANT4
    ├── E_field
    └── results
    	├── SiPM
		└── tracking

----------------------------------------------------------------------------------------------------------------------------------------------------------------

## Execute the simulation:

- In 'interactive mode' with visualization: ``` ./ABsimulation```
- In 'batch' mode from macro files: ```./ABsimulation -m full_run.mac```
