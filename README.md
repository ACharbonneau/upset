# UpSet of Tissues in the Common Fund Data Ecosystem

## About

This site is based on UpSet, an interactive, web based visualization technique designed to analyze set-based data. UpSet visualizes both, set intersections and their properties, and the items (elements) in the dataset. Please see the project website at [http://vcg.github.io/upset/about](http://vcg.github.io/upset/about) for details about the technique, publications and videos.

## CFDE Program data

I am hosting this instance of UpSet at [https://acharbonneau.github.io/upset/](https://acharbonneau.github.io/upset/). The raw data used for the plot can be viewed (or edited) [here](https://github.com/ACharbonneau/upset/blob/master/data/Programs.csv). Direct links to the pages I used to compile this dataset are provided as in-line links in the next section.

## Data Collection

The dataset is a simple binary code:
- 0 means 'this tissue is not found in this programs dataset'
- 1 means 'this tissue is found in this programs dataset'

Very generally, the data was compiled by starting with the GTEx tissue list, checking each other programs data against that list, and adding tissues as needed.

More specifically:

- I downloaded the [V8 Sample Counts by Tissues](https://gtexportal.org/home/tissueSummaryPage) from GTEx, extracted column one, and assigned GTEx a '1' for each row. 

- I used the ['Body Site' filter options](https://portal.hmpdacc.org/search/s?facetTab=cases) from the Human Microbiome Project.

- I used the [unlabeled list of tissue types (third filter section from the top on the left side of this page](http://lincsportal.ccs.miami.edu/cells/#/catalog) at LINCS.

- I used the tissues shown in the ['Sample Source' bubble plot](https://www.metabolomicsworkbench.org/data/Bubble_source3.php) at Metabolomics.

- I clicked 'EXPLORE DATASET' for [each dataset listing, and read through the descriptions](https://data.sparc.science/browse/#/?searchType=datasets&searchTerms=) for SPARC.

- On the [4D Nucleome Data Browser](https://data.4dnucleome.org/browse/?award.project=4DN&experimentset_type=replicate&type=ExperimentSetReplicate) I restricted the datasets to only '4DNucleome' and used the 'Tissue Source' filter options.

- For MoTrPAC, I used [this tissue list](http://study-docs.motrpac-data.org/MoTrPAC_External_Data_Release_ReadMe.pdf).

- On the [Kids First Data Portal](https://portal.kidsfirstdrc.org/explore), I used the filtering options for Biospecimens/Anatomical Site (Source Text).

- HuBMAP does not yet have data, and so has only zeros.

- For KOMP, I searched the entire set of tissue types in my list at the [KOMP Phenotyping website](https://www.kompphenotype.org/index.php). Since this was a search rather than getting a list of their tissues, I'm sure some are missing. 

- For UDN, I scrolled through the BioSamples associated with [Clinical and Genetic Evaluations of Individuals with Undiagnosed Disorders Through the Undiagnosed Diseases Network (human)](https://www.ncbi.nlm.nih.gov/biosample?Db=biosample&DbFrom=bioproject&Cmd=Link&LinkName=bioproject_biosample&LinkReadableName=BioSample&ordinalpos=1&IdsFromResult=350184,350185)

- IDG was recently renewed, and I couldn't easily locate data on their new site, so I used the [disease listing from the data site for their first phase](https://pharos.nih.gov/diseases) and associated the diseases with their tissues. There are 34697 disease entries, and they are arranged by the amount of data available for each one. I did not scroll through all 34697, I just did the first ~2000.

- A2CPS does not yet have data, and so has only zeros. 

- At ExRNA, I used the [list of biofluids in the 'Biofluids vs Condition Grid](https://exrna-atlas.org/exat/fluidVsDis)




## Data Decisions

if it was the diseased version of a tissue, I counted it as that tissue: for e.g. colon cancer is colon tissue, kidney cancer is kidney tissue
if it was a cell line, i counted it as it’s source tissue unless:
and was undifferentiated, a stem cell, or a metatisticized cell in which case I just excluded them
