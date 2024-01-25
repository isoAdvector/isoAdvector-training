# IsoAdvector training cases

This repository contains two training cases for learning to use the OpenFOAM 
solver interIsoFoam used for simulating flows of two immiscible, incompressible 
fluids. InterIsoFoam is essentially a copy of the interFoam solver with MULES 
replaced by isoAdvector for the interface advection.

The two cases are:

## dropSplash

Here we will learn to set up a setAlpahFieldDict and how to convert an interFoam
case into an interIsoFoam case.

## standingWave

Here we will investigate the difference in spurious currents created with 
interIsoFoam and interFoam, and learn how to make our own improved interIsoFoam
solver expoiting the geometric interface representation to improve the gravity
discretisation.

The exercises are described in [this](https://docs.google.com/document/d/1TEzo1m-WDn-5wNxDqwnjOR5t6RwTG_8gwh-7EDYdDjA/edit?usp=drive_link) google doc.

Throughout the training I might need to share setup files with you. They will be
placed in [this](https://drive.google.com/drive/folders/1ZexuHosFoV3P3vcqm0d2yRZfFR5FaXXz?usp=drive_link) google drive.

Code snippets or useful terminal commands may be shared in [this](https://docs.google.com/document/d/17q2QGsRNpIDt_GACuwZInKudlj-qZ5cU_gbtIfVUHqY/edit?usp=drive_link) google doc.

Johan Roenby, January 2024