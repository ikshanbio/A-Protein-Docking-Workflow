## Project Name
A Ligand Docking Workflow for AlphaFold Predicted Protein Structures.

## Description
This project allows for rigid docking of small ligands against predicted structures of proteins in the AlphaFold database.
The workflow fetches the structure of the ligand from PubChem and calculates the lowest free energy positions against a static, predicted protein structure using AutoDock Vina.
It serves as a quick way to check for suspected protein-ligand interaction hypotheses, for static atomic positions. 
Produced hypotheses can be investigated experimentally using methods like isothermal titration calorimetry, along with providing insights into which residues could be targeted for site-directed mutagenesis, which was the intended use of this script. 


Developed by Ikshan Ganpathi, with affiliation, at the time of development, with the Indian Institute of Science Education and Research, Bhopal (IISERB).

## Installation
```bash
git clone https://github.com/ikshanbio/A-Docking-Workflow
cd A-Docking-Workflow
```

## Tutorial
The .ipynb file fetches Streptavidin (UniProt: A0A9W9DMP7) and Biotin (CID: 171548) by default (a well-known example of protein-ligand interaction).\
\
A box is set up around the protein structure, within which the lowest energy position of the ligand is searched for by AutoDock Vina.\
The following is expected for the default settings - 
```
Docking box is centred at :- [-0.862361   1.3171452 -1.2735325]
Size of the docking box is :- [49.49  44.966 59.579]
```
Docking is run by Vina to produced ligand positions. 
The top ligand position for the default settings - 
```
[[-5.331 -7.046 -0.652  1.714 -0.652]]
```
The ligand positions are saved as a .pdb file, which can be downloaded and viewed for any further analysis or viewing elsewhere.\
\
A default viewer shows the lowest energy value ligand position bound to the protein. Image of the default docked structure - \
<img width="332" height="238" alt="Image" src="https://github.com/user-attachments/assets/3151b9a4-6b76-4cc2-8ee3-ff892b8f4e8c" />
## Dependency Acknowledgements 
This project uses:
- [AlphaFold]
- [AutoDock Vina]
- [Biopython]
- [OpenBabel]
- [PubChem]

## Citations: 
Noel M. O’Boyle, Michael Banck, Craig A. James, Chris Morley, Tim Vandermeersch, Geoffrey R. Hutchison Open Babel: An open chemical toolbox. J. Cheminf. 2011, 3, 33.

## License 
This project is licensed under the GPLv3 License.
