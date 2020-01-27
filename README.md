# UpSet of Tissues in the Common Fund Data Ecosystem

## About

This site is based on UpSet, an interactive, web based visualization technique designed to analyze set-based data. UpSet visualizes both, set intersections and their properties, and the items (elements) in the dataset. Please see the project website at [http://vcg.github.io/upset/about](http://vcg.github.io/upset/about) for details about the technique, publications and videos.

## CFDE Program data

I am hosting this instance of UpSet at [https://acharbonneau.github.io/upset/](https://acharbonneau.github.io/upset/). The raw data used for the plot can be viewed (or edited) [here](https://github.com/ACharbonneau/upset/blob/master/data/Programs.csv). Direct links to the pages I used to compile this dataset are provided as in-line links in the next section.

## Data Collection


Starting with GTEx, who helpfully lists all their tissues in a downloadable table
going to each other DCC and going through their data, adding tissues as I came across new ones

[V8 Sample Counts by Tissues](https://gtexportal.org/home/tissueSummaryPage)






['Body Site' filter options](https://portal.hmpdacc.org/search/s?facetTab=cases)


## Data Decisions

if it was the diseased version of a tissue, I counted it as that tissue: for e.g. colon cancer is colon tissue, kidney cancer is kidney tissue
if it was a cell line, i counted it as it’s source tissue unless:
and was undifferentiated, a stem cell, or a metatisticized cell in which case I just excluded them
