# Summer Olympics

## Overview

The following dataset presents a collection of Summer Olympics records from the games held in Athens (1896) to the games,  which took place in Rio (2016). All the records comprised within the datasets are stored in 3 denormalized CSV files (with ',' delimiter and simplified structure without the need for quoting): AthleteEvents.csv, HostCities.csv and NOCRegions.csv.

The dataset used for the assignment is a derivative of the following public datasets:

* [120 years of Olympic history: athletes and results][1], License: CC0 (Public Domain)
* [Olympic Sports and Medals, 1896-2014][2], License: CC BY-SA 4.0 (Attribution-ShareAlike) 

[1]: https://www.kaggle.com/heesoo37/120-years-of-olympic-history-athletes-and-results
[2]: https://www.kaggle.com/the-guardian/olympic-games

This extensive collection of data holds records of almost 140 thousand athletes from over 200 different countries.


## Structure

**AthleteEvents.csv:** The AthleteEvents file contains data on all of the athletes and the Olympic events they competed in. The data points included in the file are:

* *AID* : An ID that uniquely identifies the athlete.
* *Name* : The first and last name of the athlete. In some cases it can contain also the athletes' nickname. Two separate athletes may have the same name.
* *Gender* : The gender of the athlete.
  * Values: M (= Male), F (= Female), O (= Other)
* *DateOfBirth* : The birth date of the athlete.
  * Format: yyyy-mm-dd
* *Height* : The height of the athlete in centimeters.
* *Weight* : The weight of the athlete in kilograms.
* *Team* : The name of the team/country for which the athlete played.
* *NOC* : The National Olympic Committee code of the team/country.
* *Games* : The name/title of the Olympic games the athlete participated in.
* *Year* : The year the Olympic games took place.
* *City* : The city in which the Olympic games took place.
* *Sport* : The name of the sport in which the athlete competed.
* *Event* : The name of the event in which the athlete competed in.
* *Medal* : The medal won by the athlete in a particular event.
  * Values: Gold, Silver, Bronze, NULL (empty field, indicating participation but no medal won)

The following is an excerpt from the **AthleteEvents.csv** file, which is representative of the dataset's structure:

```
AID,Name,Gender,DateOfBirth,Height,Weight,Team,NOC,Games,Year,City,Sport,Event,Medal
105331,Tonya Denise "Teee" Sanders-Williams (-Slacanin),F,1968-01-01,180,66,United States of America,USA,1992 Summer,1992,Barcelona,Volleyball,Volleyball Women's Volleyball,Bronze
105331,Tonya Denise "Teee" Sanders-Williams (-Slacanin),F,1968-01-01,180,66,United States of America,USA,1996 Summer,1996,Atlanta,Volleyball,Volleyball Women's Volleyball,
105332,Cael Norman Sanderson,M,1979-01-01,182,84,United States of America,USA,2004 Summer,2004,Athina,Wrestling,Wrestling Men's Light-Heavyweight; Freestyle,Gold
105333,Fred R. Sanderson,M,1873-01-01,,,United States of America,USA,1904 Summer,1904,St. Louis,Tennis,Tennis Men's Singles,
105334,Keith Sanderson,M,1975-01-01,183,95,United States of America,USA,2008 Summer,2008,Beijing,Shooting,Shooting Men's Rapid-Fire Pistol; 25 metres,
105334,Keith Sanderson,M,1975-01-01,183,95,United States of America,USA,2012 Summer,2012,London,Shooting,Shooting Men's Rapid-Fire Pistol; 25 metres,
105334,Keith Sanderson,M,1975-01-01,183,95,United States of America,USA,2016 Summer,2016,Rio de Janeiro,Shooting,Shooting Men's Rapid-Fire Pistol; 25 metres,
105335,Nicole Sanderson,F,1976-01-01,182,65,Australia,AUS,2004 Summer,2004,Athina,Beach Volleyball,Beach Volleyball Women's Beach Volleyball,
105336,Ronald Harcourt Sanderson,M,1877-01-01,,85,Great Britain,GBR,1908 Summer,1908,London,Rowing,Rowing Men's Coxed Eights,Gold
105337,Theresa Ione "Tessa" Sanderson (-White),F,1956-01-01,168,70,Great Britain,GBR,1976 Summer,1976,Montreal,Athletics,Athletics Women's Javelin Throw,
```

**HostCities.csv:** The HostCities file contains data on the cities that hosted any of the summer Olympic games. The data points included in the file are:

* *NOC* : The National Olympic Committee code of the country in which the city is located.
* *Country* : The name of the country in which the city is located.
* *City* : The name of the city.
* *Year* : The year in which the Olympic games took place.
* *StartDate* : The date on which the Olympic games started.
  * Format: yyyy-mm-dd
* *EndDate* : The date on which the Olympic games ended.
  * Format: yyyy-mm-dd

If the Olympic games took place in two different cities, then the multi-valued data fields are separated by a pipe "|".

The following is an excerpt from the **HostCities.csv** file, which is representative of the dataset's structure:

```
NOC,Country,City,Year,StartDate,EndDate
AUS,Australia,Sydney,2000,2000-09-15,2000-10-01
AUS|SWE,Australia|Sweden,Melbourne|Stockholm,1956,1956-06-10,1956-12-08
BEL,Belgium,Antwerp,1920,1920-08-14,1920-09-12
BRA,Brazil,Rio de Janeiro,2016,2016-08-05,2016-08-21
CAN,Canada,Montreal,1976,1976-07-17,1976-08-01
FIN,Finland,Helsinki,1952,1952-07-19,1952-08-03
FRA,France,Paris,1900,1900-05-14,1900-10-28
FRA,France,Paris,1924,1924-07-05,1924-07-27
FRA,France,Paris,2024,2024-07-26,2024-08-11
GER,Germany,Berlin,1936,1936-08-01,1936-08-16
```

**NOCRegions.csv:** The Countries file contains data on countries. The data points included in the file are:

* *NOC* : The National Olympic Committee code of the country/team.
* *Region* : The name of the country/team.
* *Population* : The population of the country.
* *GDP* : The gross domestic product of the country.

The following is an excerpt from the **NOCRegions.csv** file, which is representative of the dataset's structure:

```
NOC,Region,Population,GDP
IOP,Independent Olympic Participants,,
IRI,Islamic Republic of Iran,79109272,5550.1
IRL,Ireland,4640703,78661.0
IRQ,Iraq,36423395,5955.1
ISL,Iceland,330823,66944.8
ISR,Israel,8380400,43592.1
ISV,Virgin Islands; US,103574,35938.0
ITA,Italy,60802085,33228.2
IVB,Virgin Islands; British,30117,34200.0
JAM,Jamaica,2725941,5582.3
```
