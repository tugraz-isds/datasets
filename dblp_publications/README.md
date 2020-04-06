# DBLP Publications

## Overview 
This dataset was derived from a CC0-licensed dump of the [DBLP](https://dblp.uni-trier.de/) respository (Mar 02, 2020), and contains denormalized CSV files (with ',' delimiter and simplified structure without the need for quoting) for persons, theses, publications, and conferences/journals. Note: Due to free-form conference titles and affiliations as well as a wealth of other issues, we cleaned this dataset with a mix of automatic and semi-automic data cleaning techniques.

## Structure: 

**persons.csv:** The persons file contains author information including name aliases (with ':' delimiter), current affiliation (incl. country), and websites. It's detailed structure and examples look as follows.
```
AKey,Name,Aliases,Affiliation,Country,Website
A266688,Matthias Boehm 0001,Matthias Böhm 0001,Graz University of Technology,Austria,http://matthiasboehm.org/
A1542023,Stefanie N. Lindstaedt,Stefanie N. Lindstädt,,,https://scholar.google.com/citations?user=ZcWoNxgAAAAJ
A982373,Denis Helic,,Graz University of Technology,Austria,https://orcid.org/0000-0003-0725-7450
```

**theses.csv:** The theses file contains the information of public PhD and master theses. It's detailed structure and examples look as follows.
```
TKey,Author,Title,Year,Type,School,Country,Pages,ISBN
T25884,A266688,Cost-based optimization of integration flows,2011,PhD,Dresden University of Technology,Germany,227,
T30374,A1403785,An Architecture for and Fast and General Data Processing on Large Clusters,2013,PhD,UC Berkeley,USA,,
```

**pubs.csv:** The pubs file contains publication information such as articles and papers from data management journals and conferences (in a broad sense) since 2011. It's detailed structure and examples look as follows.
```
PKey,Authors,Title,Pages,CJKey
P311937,A266688:A1624835:A2334724:A828022:A1625689:A1622315:A1621339:A1542023:A728601:A1630329:A2057091:A577685:A2328996,SystemDS: A Declarative Machine Learning System for the End-to-End Data Science Lifecycle,,C39
P525300,A387501:A266688:A266328:A2057091:A69523,MNC: Structure-Exploiting Sparsity Estimation for Matrix Expressions,1607-1623,C44
P1659320,A266688:A2057091:A2051514:A477262:A266328:A393370,On Optimizing Operator Fusion Plans for Large-Scale Machine Learning in SystemML,1755-1768,J238
```

**confs.csv:** The confs file contains the information on conferences. It's detailed structure and examples look as follows.
```
CKey,Shortname,Title,City,Country,Editors,Year,ISBN
C39,CIDR,CIDR 2020; 10th Conference on Innovative Data Systems Research,Amsterdam,The Netherlands,,2020,
C44,SIGMOD,2019 International Conference on Management of Data; SIGMOD Conference 2019,Amsterdam,The Netherlands,A1986864:A1855308:A111462:A1203867:A1044165,2019,978-1-4503-5643-5
```

**journals.csv:** The journals file contains the information on journals. It's detailed structure and examples look as follows.
```
JKey,Shortname,Title,Volume,Number,Year
J238,PVLDB,Proceedings of the VLDB Endowment,11,12,2018
```

