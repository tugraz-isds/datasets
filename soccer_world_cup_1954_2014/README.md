# Soccer Worldcup Data 1954-2014

## Overview 
This dataset was derived from the public-domain [Openfootball Worldcup Dataset](https://github.com/openfootball/world-cup)
and can be freely used without any restrictions. In contrast to the original structured text files (with varying layouts),this dataset contains denormalized CSV files for Squads, Matches, and Goals that have been already cleaned (consistent country names, player names, round types, etc) in order to serve as a data ingestion use case in lectures on database systems. Note that this dataset is limited to the years 1954-2014 (instead of 1930-2014) to remove the complexity of replay games, and goals information is only complete for 2014.


##Structure: 

**1954_2014_Squads.csv:** The Squads file contains the player information of all teams participating in the worldcup. It's detailed structure and examples look as follows.
```
#Year, Host_Country, Country, Jersey_Number, Position, Name, Club_Name, Club_Country
1998,France,Austria,14,FW,Hannes Reinmayr,Sturm Graz,
2014,Brazil,Germany,1,GK,Manuel Neuer,Bayern Munich,Germany
2014,Brazil,Germany,11,FW,Miroslav Klose,Lazio,Italy
```

**1954_2014_Matches.csv:** The Matches file contains all group and play-off match statistics of the worldcup. It's detailed structure and examples look as follows.
```
#Year, Host_Country, Match_ID, Type, Date, Location, Team 1, Team 2, Score 1, Score 2
2006,Germany,571,Group A,Fri Jun/9,Veltins-Arena, Gelsenkirchen,Poland,Ecuador,0,2
2010,South Africa,684,Round of 16,Sun Jun/27 16:00,Free State Stadium, Bloemfontein,Germany,England,4,1
2014,Brazil,761,Final,Sun Jul/13 16:00,Estádio do Maracanã, Rio de Janeiro (UTC-3),Germany,Argentina,1,0
```

**1954_2014_Goals.csv:** The Goals file contains the goals of group and play-off matches including the team, the players name, the time of the game. It's detailed structure and examples look as follows.
```
#Year, Host_Country, Match_ID, Team, Player, Minute
2014,Brazil,760,Netherlands,Daley Blind,17
2014,Brazil,760,Netherlands,Georginio Wijnaldum,90+1
2014,Brazil,761,Germany,Mario Götze,113
```














 cleaned data 

and is parsed into denormalized CSV files to allow for easy 


we restrict ourselves to the years .



*SystemDS is a versatile system for the end-to-end data science lifecycle from data integration, cleaning, and feature engineering, over efficient, local and distributed ML model training, to deployment and serving. To this end, we aim to provide a stack of declarative languages with R-like syntax for (1) the different tasks of the data-science lifecycle, and (2) users with different expertise. These high-level scripts are compiled into hybrid execution plans of local, in-memory CPU and GPU operations, as well as distributed operations on Apache Spark. In contrast to existing systems - that either provide homogeneous tensors or 2D Datasets - and in order to serve the entire data science lifecycle, the underlying data model are DataTensors, i.e., tensors (multi-dimensional arrays) whose first dimension may have a heterogeneous and nested schema.
*
*
*

**Documentation:** [SystemDS Documentation](http://apache.github.io/systemml/dml-language-reference)<br/>

**Status and Build:** SystemDS is still in pre-alpha status. The original code base was forked from [**Apache SystemML**](http://systemml.apache.org/) 1.2 in September 2019. We will continue to support linear algebra programs over matrices, while replacing the underlying data model and compiler, as well as substantially extending the supported functionalities. Until the first release, you can build your own snapshot via Apache Maven: `mvn -DskipTests clean package`.
