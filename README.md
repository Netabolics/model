
# Virtual whole-cell model

This repository illustrates the features of our latest genome-scale generic model of human cell biology.

> Version: `odevc-14.25.131` &nbsp; &nbsp;  Last update: `20260126T151738`


## Overview

A human biological network (in the form of a directed hypergraph) is constructed through semi-automatic extraction and manual curation of data from publicly available as well as proprietary databases and knowledge bases. The network is used to build a mechanistic, compartmentalized, generic model as a systems of ordinary differential equations (ODEs). The generic model can be parametrized using public or private multiomics datasets to make it cell type- or tissue-specific. The parametrized model is used within our AI-Driven Biosimulation platform (https://netabolics.ai/) to perform dynamical (i.e., time-resolved) simulation.


## Features

Overall, the model integrates **gene regulatory network** (GRN) to model upregulation or downregulation of gene products expression, **signal transduction network** (STN) to model activation/inhibition reactions among gene-encoded products, **metabolic reactions network** (MRN) to model biochemical processing of metabolites by enzyme-catalyzed reactions and carrier-mediated transport processes, and **protein-interaction network** (PIN) to model formation of protein (super)complexes. 

Specifically, the model incorporates the components listed in the following table.

| Component | Number | Class | Type/Example |
| --------- | ------ | ----- | ---- |
| Compartments | **9** 
| | | extracellular | extracellular space |
|              |  | intracellular | cytosol<br>mitochondrion (intermembrane space)<br>mitochondrion (matrix)<br>nucleus<br>(sarco)endoplasmic reticulum<br>Golgi apparatus<br>peroxisome<br>lysosome |
| Genes | **14,153** | | see `genes.csv` |
| Molecular Species | **24,518** (*)
| | | gene products | proteins (via mRNA)<br>&nbsp;&nbsp;*signaling proteins*<br>&nbsp;&nbsp;*transcription factors*<br>&nbsp;&nbsp;*enzymes*<br>&nbsp;&nbsp;*channels*<br>&nbsp;&nbsp;*transporters*<br>long non-coding RNAs (lncRNA)<br>micro RNAs (miRNA) |
| | | complexes | enzymatic, regulatory, etc. |
| | | small molecules | metabolites<br>ions<br>cofactors<br>second messengers |
| Gene-associated Reactions | **130,627**
| | | signal transduction | activation/inactivation (kinases, phosphatases, receptors, G-proteins, etc.) |
| | | gene regulation | upregulation/downregulation of gene expression |
| | | complex formation | physical interactions, binding, etc. |
| | | enzymatic catalysis | biosynthesis, energy metabolism, etc. |
| | | intercompartment transport | transmembrane, carrier- or channel-mediated, etc. |
|

(*) As *unique* molecular species. The actual number of species (corresponding to the number of ODEs) is substantially larger as many species exist in different states (e.g., phosphorylated vs dephosphorylated proteins).


## Planned Updates

We are constantly working to extend gene coverage. Currently, we are assessing the confidence of about half million additional gene-associated reactions to reach a complete coverage of the protein-coding genes and almost full coverage of the known non-coding RNA genes.


## Further Reading

DiNuzzo M. How artificial intelligence enables modeling and simulation of biological networks to accelerate drug discovery. *Frontiers in Drug Discovery*, 2:2022. [10.3389/fddsv.2022.1019706](https://doi.org/10.3389/fddsv.2022.1019706)


## Copyright Notice

The biological network, the model, and the biosimulation software are proprietary assets of Netabolics.

For any inquiries, please [contact us](https://netabolics.ai/#contacts).

&nbsp;

Copyright &copy; 2020-2026 by Netabolics SRL. All rights reserved.

