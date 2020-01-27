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

- For MoTrPAC, I used [this tissue list](http://study-docs.motrpac-data.org/MoTrPAC_External_Data_Release_ReadMe.pdf)

- Kids First

- HuBMAP does not yet have data, and so has only zeros.

- KOMP

- UDN

- IDG

- A2CPS does not yet have data, and so has only zeros. 

- ExRNA




## Data Decisions

if it was the diseased version of a tissue, I counted it as that tissue: for e.g. colon cancer is colon tissue, kidney cancer is kidney tissue
if it was a cell line, i counted it as it’s source tissue unless:
and was undifferentiated, a stem cell, or a metatisticized cell in which case I just excluded them
