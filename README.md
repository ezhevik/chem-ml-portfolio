# Data analysis and machine learning for chemistry

I am an experimental chemist (PhD candidate, KAUST) working on porous adsorbents for gas and vapour separation.
This repository contains a calculation I use for my adsorption data and my solutions to exercises from the
continuing-education programme *Artificial Intelligence in a Chemist's Work* (ITMO University, 2026).

| # | Notebook | Source | Contents | Tools |
|---|----------|--------|----------|-------|
| 01 | [D₂/H₂ selectivity from isotherms (IAST)](01_adsorption_iast/iast_selectivity_demo.ipynb) | Own lab work | Reading a Micromeritics 3Flex report, dual-site Langmuir fit of H₂ and D₂ isotherms at 77 K, IAST selectivity of an equimolar mixture | pyGAPS |
| 02 | [pymatgen and Materials Project](02_pymatgen_materials_project/pymatgen_materials_project.ipynb) | ITMO course exercise | Structure analysis of a Materials Project entry; electronegativity, electron affinity and ionic-radius descriptors for a list of inorganic materials | pymatgen, mp-api |
| 03 | [Aqueous solubility regression](03_solubility_regression/solubility_regression.ipynb) | ITMO course exercise | Gradient boosting and stacking on RDKit descriptors, hyperparameter tuning, comparison with a linear baseline | scikit-learn |
| 04 | [Blood–brain barrier penetration classification](04_bbbp_classification/bbbp_classification.ipynb) | ITMO course exercise | Random forest and gradient boosting, tuning by ROC-AUC, comparison with kNN | scikit-learn |
| 05 | [PubChem and RDKit](05_pubchem_rdkit/pubchem_rdkit.ipynb) | ITMO course exercise | Compound properties from PubChem by name, RDKit descriptor table, SDF files, substructure search | PubChemPy, RDKit |
| 06 | [Groundwater quality EDA](06_groundwater_quality_eda/groundwater_quality_eda.ipynb) | ITMO course exercise | Distributions, normality and group tests, outliers, correlation analysis | pandas, plotly, SciPy |

Notebook 01 runs on synthetic demo isotherms; the measured data belong to an unpublished study.

## Running

```bash
pip install -r requirements.txt
jupyter lab
```

Notebooks 03, 04 and 06 use course datasets (an AqSolDB-derived table, MoleculeNet BBBP with RDKit descriptors,
and Telangana groundwater quality data), which are not included; place them in each notebook's `data/` folder.
Notebook 02 needs a Materials Project API key in the `MP_API_KEY` environment variable.

## Contact

Viktoriia Zheltova · vic.zheltova@gmail.com · [Google Scholar](https://scholar.google.com/citations?user=RgR3u4UAAAAJ)
