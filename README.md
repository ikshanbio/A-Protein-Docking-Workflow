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
git clone https://github.com/ikshanbio/A-Protein-Docking-Workflow
cd A-Protein-Docking-Workflow
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
Values may differ slightly in each run due to stochasticity of the process, however, the obtained value would be lower than the experimentally-determined value of Streptavidin-Biotin interaction (~ -20 kcal mol<sup>-1</sup>), as docking alone doesn't account for any entropic contributions, or enthalpic contributions from the surrounding buffer.
Consider carrying out some form of MD simulations for greater accuracy.\
The ligand positions are saved as a .pdb file, which can be downloaded and viewed for any further analysis or viewing elsewhere.\
\
A default viewer shows the lowest energy value ligand position bound to the protein. Image of the default docked structure - \
<img width="332" height="238" alt="Image" src="https://github.com/user-attachments/assets/3151b9a4-6b76-4cc2-8ee3-ff892b8f4e8c" />
## Dependency Acknowledgements 
### This project uses:
- [Biopython]
- [Meeko]
- [AutoDock Vina]
- [RDKit]
- [py3Dmol]
### This project fetches data from:
- [AlphaFold]  - Protein structure
- [PubChem] - Ligand structure

## Citations: 
1. (Biopython) Cock, P. J. A., Antao, T., Chang, J. T., Chapman, B. A., Cox, C. J., Dalke, A., Friedberg, I., Hamelryck, T., Kauff, F., Wilczynski, B., & de Hoon, M. J. L. (2009). Biopython: freely available Python tools for computational molecular biology and bioinformatics. Bioinformatics, 11, 1422–1423. https://doi.org/10.1093/bioinformatics/btp163 
2. (AlphaFold) Jumper, J., Evans, R., Pritzel, A., Green, T., Figurnov, M., Ronneberger, O., Tunyasuvunakool, K., Bates, R., Žídek, A., Potapenko, A., Bridgland, A., Meyer, C., Kohl, S. A. A., Ballard, A. J., Cowie, A., Romera-Paredes, B., Nikolov, S., Jain, R., Adler, J., … Hassabis, D. (2021). Highly accurate protein structure prediction with AlphaFold. Nature, 7873, 583–589. https://doi.org/10.1038/s41586-021-03819-2
3.  (PubChem) Kim, S., Chen, J., Cheng, T., Gindulyte, A., He, J., He, S., Li, Q., Shoemaker, B. A., Thiessen, P. A., Yu, B., Zaslavsky, L., Zhang, J., & Bolton, E. E. (2025). PubChem 2025 update. Nucleic Acids Res., 53(D1), D1516–D1525. https://doi.org/10.1093/nar/gkae1059
4.  (RDKit) Landrum, G., Tosco, P., Rodriguez, R., Kelley, B., Cosgrove, D., Vianello, R., sriniker, Gedeck, P., Jones, G., Nealschneider, D., Kawashima, E., NadineSchneider, tadhurst-cdd, Maeder, N., Boyd, K., Dalke, A., Pechersky, Y., Swain, M., Cole, B., … Buchthal, K. (2026, November 5). rdkit/rdkit: 2026_09_2 (Q3 2026) Release | Zenodo. Zenodo; Zenodo. https://doi.org/10.5281/zenodo.591637 
5. (3Dmol) Rego, N., & Koes, D. (2014). 3Dmol.js: molecular visualization with WebGL. Bioinformatics, 8, 1322–1324. https://doi.org/10.1093/bioinformatics/btu829
6. (Meeko) Santos-Martins, D., He, Y., Eberhardt, J., Sharma, P., Bruciaferri, N., Holcomb, M., Llanos, M. A., Hansel-Harris, A., Barkdull, A. P., Tillack, A. F., Bianco, G., Paulsen, M.-L., Mato, J., Taneja, I., & Forli, S. (2025). Meeko: Molecule Parametrization and Software Interoperability for Docking and Beyond. Journal of Chemical Information and Modeling, 24, 13045–13050. https://doi.org/10.1021/acs.jcim.5c02271 
7. (AutoDock Vina) Trott, O., & Olson, A. J. (2009). AutoDock Vina: Improving the speed and accuracy of docking with a new scoring function, efficient optimization, and multithreading. Journal of Computational Chemistry, 2, 455–461. https://doi.org/10.1002/jcc.21334

## License 
This project is licensed under the GPLv3 License.
