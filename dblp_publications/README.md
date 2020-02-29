# DBLP Publications

## Overview 
This dataset was derived from a CC0-licensed dump of the [DBLP](https://dblp.uni-trier.de/) respository (Feb 01, 2020), and contains denormalized CSV files (with '|' delimiter) for persons, theses, publications, and conferences/journals. Note: We're still in the process of performing additional cleaning and restructuring.

## Structure: 

**persons.csv:** The persons file contains author information including name aliases (with ':' delimiter), current affiliation, and websites. It's detailed structure and examples look as follows.
```
#PID | name | aliases | affiliation | url
A261789|Matthias Boehm 0001|Matthias Böhm 0001|Graz University of Technology, Austria| http://matthiasboehm.org/
A1537639|Stefanie N. Lindstaedt|Stefanie N. Lindstädt||https://scholar.google.com/citations?user=ZcWoNxgAAAAJ
A977823|Denis Helic||Graz University of Technology, Austria|https://orcid.org/0000-0003-0725-7450
```

**theses.csv:** The theses file contains the information of public PhD and master theses. It's detailed structure and examples look as follows.
```
#TKey | author | title | year | type | school | pages | isbn
T25621|A261789|Cost-based optimization of integration flows.|2011|PhD|Dresden University of Technology, Germany|227|
T30052|A1399369|An Architecture for Fast and General Data Processing on Large Clusters.|2013|PhD|University of California, Berkeley, USA||
```

**pubs.csv:** The pubs file (or better, its individual parts) contains publication information such as articles, papers, books, etc. It's detailed structure and examples look as follows.
```
#PKey | authors| title | year | type | journal | volumne | number | pages | isbn | CKey
P519327|A382693:A261789:A261428:A2051042:A69590|MNC: Structure-Exploiting Sparsity Estimation for Matrix Expressions.|2019|IP||||1607-1623||C8036
P1640801|A261789:A2051042:A2047447:A472485:A261428:A388567|On Optimizing Operator Fusion Plans for Large-Scale Machine Learning in SystemML.|2018|A|PVLDB|11|12|1755-1768||
P12485|A1399369:A1703306:A1416241:A557115:A650354:A863102:A345039:A1315778:A699758|Resilient Distributed Datasets: A Fault-Tolerant Abstraction for In-Memory Cluster Computing.|2012|IP||||15-28||C76
```

**confs.csv:** The confs file contains the information on conferences. It's detailed structure and examples look as follows, but will likely be further improved soon.
```
#CKey | title | editors | year | isbn
C8036|Proceedings of the 2019 International Conference on Management of Data, SIGMOD Conference 2019, Amsterdam, The Netherlands, June 30 - July 5, 2019.|A1982769:A1851158:A111556:A1199401:A1039606|2019|978-1-4503-5643-5
C76|Proceedings of the 9th USENIX Symposium on Networked Systems Design and Implementation, NSDI 2012, San Jose, CA, USA, April 25-27, 2012|A830515:A851612|2012|
```
