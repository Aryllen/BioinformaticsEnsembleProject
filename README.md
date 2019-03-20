# Overview
This repository contains Jupyter Notebooks created specifically for the University of Washington TCSS 588 Bioinformatics Winter 2019 final project. The project built upon the idea of an NCBI Hackathon group, ConsensusML, to use ensemble machine learning models, not for prediction, but for feature selection. They specifically used cancer data with the intent to find genes important to cancer, especially AML, for further study.
<br>
The notebooks in this repository were created by me, Nicole Kauer, and are the following:
1. OriginalDataProcessing: dividing up the data into the needed sets, with the correct labels.
2. DataAnalysis: analyzing data from all the machine learning models.
3. Visualization: creating Venn diagrams depicting the overlap between the genes selected in the different models. 

# Notebook Requirements
Running these notebooks requires the following:
- [Jupyter Notebook](https://jupyter.org/install) or [Jupyter Lab](https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html) and it's dependencies,
- [R](https://www.r-project.org/) installed.
- [IRkernel](https://irkernel.github.io/installation/) installed and setup for Jupyter.
- Visualization notebook requires the ['limma'](https://stats.idre.ucla.edu/r/faq/how-can-i-generate-a-venn-diagram-in-r/) package; the code for this is in the notebook, but it can be installed separately.

## File Requirements
Each notebook requires a set of files to run. These are listed below.

### OriginalDataProcessing
[AML_assay_clinical.csv](https://github.com/NCBI-Hackathons/ConsensusML/blob/master/Clinical_Data/AML_assay_clinical.csv): This notebook used a file from ConsensusML containing a mashup of the clinical and TMM normalized RNA sequence data for TARGET AML patients. This file is not located in this repository due to size constraints and the simple fact that it's not my file. This file should be downloaded and put in the same directory as the OriginalDataProcessing notebook.

### DataAnalysis
The following two files rely on the OriginalDataProcessing notebook:
- aml.data.labels.csv: File containing binary risk labels for all patient samples. This file is created by the OriginalDataProcessing notebook.
- aml.data.RNA.reduced.csv: File containing approximately 10k genes passing the least strict t-Test done by the group. The t-test notebook is not located in this repository and was primarily authored by group member Edgar Elliott. 
The following files are located in the super_matrix folder of the repository:
- coef_100.txt, coef_1k.txt, coef_2.5k.txt, coef_5k.txt, coef_10k.txt: Coefficients or importance values for each model and dataset.
- acc_100.txt, acc_1k.txt, acc_2.5k.txt, acc_5k.txt, acc_10k.txt: Accuracy or MSE scores for each model and dataset.
The super_matrix files were created by the Data Wrangling notebook (not in this repository), that was primarily authored by a group member, Alex Merk.

### Visualization
The following files are located in the super_matrix folder of the repository:
- coef_100.txt, coef_1k.txt, coef_2.5k.txt, coef_5k.txt, coef_10k.txt: Coefficients or importance values for each model and dataset. 
The super_matrix files were created by the Data Wrangling notebook (not in this repository), that was primarily authored by a group member, Alex Merk.
