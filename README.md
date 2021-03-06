# MaSIF- Molecular Surface Interaction Fingerprints: Geometric deep learning to decipher patterns in molecular surfaces.

[![bioRxiv shield](https://img.shields.io/badge/bioRxiv-1709.01233-green.svg?style=flat)](https://www.biorxiv.org/content/10.1101/606202v1)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.2625420.svg)](https://doi.org/10.5281/zenodo.2625420)


# Table of Contents: 

- [Description](#description)
- [Software requirements](#software-requirements)
- [Installation](#Installation)
- [Data preparation](#Data-preparation)
- [MaSIF applications](#MaSIF-applications)
- [License](#License)
# Description

MaSIF is a proof-of-concept method for identifying patterns (fingerprints) in protein surfaces. It contains a protocol to prepare protein structure files into feature-rich surfaces, to decompose these into patches, and to identify patterns in these using deep geometric learning.

This code base is structured to reproduce the experiments found in: 

Gainza, P., Sverrisson, F., Monti, F., Rodola, E., Bronstein, M. M., & Correia, B. E. (2019). Deciphering interaction fingerprints from protein molecular surfaces. bioRxiv, 606202.

MaSIF it is meant to form as a base for any protein surface-oriented learning task. 

![MaSIF conceptual framework and method](https://raw.githubusercontent.com/LPDI-EPFL/masif/master/Fig0_v11-01.png)


# Software requirements 
MaSIF relies on external software/libraries to handle  protein databank files and surface files, to compute chemical/geometric features and coordinates, and to perform neural network calculations.  
* Python (>= 2.7)
* [reduce] (>= 3.23)(http://kinemage.biochem.duke.edu/software/reduce.php). To add protons to proteins. 
* [MSMS](>= 2.6.1)(http://mgltools.scripps.edu/packages/MSMS/). To compute the surface of proteins. 
* [BioPython] (>= 1.66)(https://github.com/biopython/biopython). To parse PDB files. 
* [PyMesh](>= 0.1.14)(https://github.com/PyMesh/PyMesh). To handle ply surface files, attributes, and to regularize meshes.
* [pyflann] (>= 1.6.14)(https://github.com/primetang/pyflann). To perform nearest neighbor searches of vertices.
* PDB2PQR (>= 2.1.1), multivalue, and [APBS] (>= 1.5)(http://www.poissonboltzmann.org/). These programs are necessary to compute electrostatics charges.
* [open3D] (>= 0.5.0.0)(https://github.com/IntelVCL/Open3D). Mainly used for RANSAC alignment.
* [matlab] (>= R2018a)(https://ch.mathworks.com/products/matlab.html). Used to compute some geometric features and angular/radial coordinates.
* [Pymol](https://pymol.org/2/). This optional plugin allows one to visualize surface files in PyMOL.
* [Tensorflow] (>= 1.9)(https://www.tensorflow.org/). For the neural network models. Models were trained and evaluated on a NVIDIA Tesla K40 GPU.
 
We are working to reduce this list of requirements for future versions.


# Installation 

# Data preparation

Mention zenodo repository with data. 
Description on data preparation for each application

# MaSIF applications

## MaSIF-ligand
## MaSIF-site
## MaSIF-search

## License

MaSIF is released under an Apache v2 license. Copyright Gainza, P., Sverrisson, F., Monti, F., Rodola, E., Bronstein, M. M., & Correia, B. E.
