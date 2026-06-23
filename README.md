## EGFR Inhibitor Database

A Python script that pulls molecular data for 10 EGFR inhibitors 
from the PubChem API and builds a searchable CSV database.

### Physicochemical properties of EGFR inhibitors
SMILES strings, molecular weights, XLogP, H-bond counts, TPSA, 
and Lipinski Rule of Five compliance for gefitinib, erlotinib, 
osimertinib, and 7 other EGFR TKIs used in NSCLC treatment.

### Importance of computational analysis
EGFR inhibitors are the frontline therapy for NSCLC patients 
with sensitizing mutations. This database was built to support 
computational analysis of structure-activity relationships 
across three generations of TKIs.

### Column descriptions

| Column | Property | Significance |
| --- | --- | --- |
| Name | Drug name | Allows cross referencing with clinical trial records, pharmacological literature, and regulatory approval databases |
| CID | PubChem unique compound identifier | Enables direct integration with PubChem, ChEMBL, and other cheminformatics platforms for downstream analysis |
| Formula | Elemental composition of the molecule | Reflects molecular complexity and the presence of pharmacophoric elements such as halogens and nitrogen heterocycles |
| MW (g/mol) | Molecular weight in grams per mole | A primary Lipinski parameter. EGFR TKIs ideally remain below 500 g/mol to maintain oral bioavailability in NSCLC patients |
| XLogP | Partition coefficient measuring lipophilicity | Determines membrane permeability. Sufficient lipophilicity is required to penetrate lung tissue and reach the intracellular kinase domain |
| HB Donors | Number of hydrogen bond donor groups (NH, OH) | Excessive donors reduce passive membrane permeability, limiting intracellular drug accumulation at the EGFR active site |
| HB Acceptors | Number of hydrogen bond acceptor atoms (N, O) | Governs binding affinity within the ATP binding cleft of EGFR and influences selectivity over off-target kinases |
| Rotatable Bonds | Count of freely rotating single bonds | Reflects conformational flexibility, relevant to the ability of the molecule to adapt to mutant EGFR isoforms such as T790M and C797S |
| TPSA (Å²) | Topological polar surface area | Predicts gastrointestinal absorption and lung tissue penetration. Values below 140 Å² are associated with adequate oral absorption |
| Lipinski Ro5 | Compliance with Lipinski's Rule of Five | Serves as a rapid computational filter for oral bioavailability, directly relevant to outpatient tablet prescribing in NSCLC |
| SMILES | Simplified Molecular Input Line Entry System string | Machine readable molecular representation enabling structure visualisation, similarity searching, and computational docking studies |
