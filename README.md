# Getting the data

Data Source: ([https://microvesicles.org/]https://microvesicles.org/)

The SSL certificate of the site is old or misconfigured and does not work with popular browsers (e.g. Chrome, Edge, ect.). Hence, the below alternative is used to download the data.

```import requests

archives = ["VESICLEPEDIA_PROTEIN_MRNA_DETAILS_5.1.txt", "VESICLEPEDIA_GENE_DETAILS_5.1.txt"]

for a in archives:
    url = f"https://microvesicles.org/Archive/{a}"
    r = requests.get(url, verify=False)  # disable SSL verify only for this call
    open(a, "wb").write(r.content)
```

## Data description

### VESICLEPEDIA_PROTEIN_MRNA_DETAILS_5.1.txt

A curated compendium of molecular data related to extracellular vesicles (EVs) (such as exosomes, microvesicles, and ectosomes).

#### 🧬 Purpose

Vesiclepedia aggregates experimentally validated molecules that have been identified in extracellular vesicles from various organisms, tissues, and cell types.
This particular file (PROTEIN_MRNA_DETAILS_5.1.txt) lists proteins and mRNAs associated with those vesicles.

It’s a tab-delimited text file with tens of thousands of rows — each row is an entry describing a protein or mRNA identified in EVs.

### Vesiclepedia Protein/mRNA Details (v5.1)

| **Column Name**        | **Description**                                                                 |
|--------------------------|---------------------------------------------------------------------------------|
| **Entry_ID**             | Unique Vesiclepedia identifier for each record                                 |
| **Accession**            | Accession number from UniProt, RefSeq, or Ensembl                              |
| **Molecule_Name**        | Official name or symbol of the molecule (protein or mRNA)                      |
| **Category**             | Type of molecule, e.g., *Protein* or *mRNA*                                    |
| **Organism**             | Source organism (e.g., *Homo sapiens*, *Mus musculus*)                         |
| **Sample_Type**          | Type of extracellular vesicle (e.g., exosome, microvesicle, ectosome)          |
| **Cell_Line_or_Tissue**  | Origin of the sample (e.g., plasma, serum, fibroblast cell line)               |
| **Experimental_Method**  | Technique used to identify the molecule (e.g., LC–MS/MS, microarray)           |
| **Subcellular_Location** | Reported subcellular or vesicular localization (if available)                  |
| **Fold_Change_or_Abundance** | Quantitative value or relative expression (if reported)                   |
| **PubMed_ID**            | PubMed reference supporting the identific**_**
