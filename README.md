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

| Column | What it means |
|---|---|
| MW_g_mol | Molecular weight in g/mol. Heavier molecules absorb less easily |
| XLogP | How oily vs watery the drug is. EGFR TKIs need to be slightly oily to cross cell membranes |
| HB_Donors | Hydrogen bond donors — affects how the molecule binds to its target protein |
| HB_Acceptors | Hydrogen bond acceptors — same idea, different direction |
| TPSA_A2 | Predicts oral absorption — higher values mean harder to absorb as a tablet |
| Lipinski_Ro5 | Pass/fail checklist for oral bioavailability |
| SMILES | Text encoding of the full molecular structure — readable by chemistry software |
