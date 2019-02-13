# Soccer Worldcup Data 1954-2014

## Overview 
This dataset was derived from the public-domain [Openfootball Worldcup Dataset](https://github.com/openfootball/world-cup)
and can be freely used without any restrictions. In contrast to the original structured text files (with varying layouts),this dataset contains denormalized CSV files for Squads, Matches, and Goals that have been already cleaned (consistent country names, player names, round types, etc) in order to serve as a data ingestion use case in lectures on database systems. Note that this dataset is limited to the years 1954-2014 (instead of 1930-2014) to remove the complexity of replay games, and goals information is only complete for 2014.


## Structure: 

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
