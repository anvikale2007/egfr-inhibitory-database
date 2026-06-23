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

| Column | What it means | Why it matters |
|---|---|---|
| Name | Drug name | Identifies the compound |
| CID | PubChem's unique ID number | Used to look up the compound in any chemistry database |
| Formula | Atoms that make up the molecule | Shows molecular complexity at a glance |
| MW_g_mol | Molecular weight in g/mol | Heavier molecules absorb poorly — EGFR TKIs aim to stay under 500 g/mol for oral use |
| XLogP | How oily vs watery the drug is | EGFR TKIs must be slightly oily to cross lung cell membranes and reach the tumour |
| HB_Donors | Number of hydrogen bond donor groups | Too many donors reduce membrane permeability — directly affects how much drug reaches the target |
| HB_Acceptors | Number of hydrogen bond acceptor groups | Influences how tightly the drug binds to the EGFR kinase domain |
| Rotatable_Bonds | How flexible the molecule is | More flexible molecules can adapt their shape to fit mutant EGFR pockets like T790M |
| TPSA_A2 | Topological polar surface area | Predicts whether the drug survives oral dosing and reaches lung tissue intact |
| Lipinski_Ro5 | Pass/fail oral bioavailability check | Directly predicts if the drug can be prescribed as a tablet — critical for outpatient NSCLC treatment |
| SMILES | Text code representing molecular structure | Allows the molecule to be visualised, docked, or modelled computationally |
