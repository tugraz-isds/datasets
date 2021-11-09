# Austrian National Elections (2017 & 2019)

## Overview

The following dataset is a collection of Austrian National Election records from the years 2017 and 2019. All the records comprised within the datasets are stored in 4 denormalized CSV files (with ',' delimiter and simplified structure without the need for quoting): Elections.csv, Votes.csv, Parties.csv, and Locations.csv.

The dataset used for the assignment is a derivative of datasets obtained from the following public data sources under license Creative Commons Namensnennung 4.0 International ([CC BY 4.0][3]):
* [Open Data Österreich][1]
* [Bundesministerium Inneres][2]

[1]: https://www.data.gv.at/
[2]: https://www.bmi.gv.at/
[3]: https://creativecommons.org/licenses/by/4.0/deed.de


## Structure
**Elections.csv** The *Elections* file contains general data about the elections. The data points have the following structue:

* **ElectionID:**  The ID of the election to which the data row refers.
  * Format: 6-Character *String* ("NR2017" or "NR2019")
* **Number:** The sequential number of the election's legislative period.
  * Format: *Numerical*
* **Date:** The date of the election day.
  * Format: *yyyy-mm-dd*

The following is an excerpt from the **Elections.csv** file, which is representative of the dataset's structure:

```
ElectionID,Number,Date
NR2017,26,2017-10-15
NR2019,27,2019-09-29
```

**Votes.csv:**  The *Votes* file contains data on the eligible voters and the election results. The data points have the following structure:

* **ElectionID:** The ID of the election to which the data row refers.
  * Format: 6-Character *String* ("NR2017" or "NR2019")
* **RegionID:** The ID of the region (Gebiet) to which the data row refers.
  * Format: 6-Character *String* (e.g. "G60101")
* **ParentID:** The ID of the parent region.
  * Format: 6-Character *String* (e.g. "G60101") or *NULL* (the region is not part of any other region)
* **EligibleVoters:** The total number of eligible voters in the region spcified by the RegionID.
  * Format: *Numerical* or *NULL* (the total number of eligible voters is not known)
* **EligibleFemale:** The total number of female eligible voters in the region spcified by the RegionID.
  * Format: *Numerical* or *NULL* (the total number of eligible voters is not known)
* **EligibleMale:** The total number of male eligible voters in the region spcified by the RegionID.
  * Format: *Numerical* or *NULL* (the total number of eligible voters is not known)
* **TotalVotes:** The total number of casted votes in the region specified by the RegionID.
  * Format: *Numerical*
* **InvalidVotes:** The total number of invalid casted votes in the region specified by the RegionID.
  * Format: *Numerical*
* **ValidVotes:** The total number of valid casted votes in the region specified by the RegionID.
  * Format: *Numerical*
* **PartyShort:** The (unique) short name of the politicl party.
  * Format: Variable length *String* (e.g. "ÖVP")
* **PartyVotes:** The number of votes received by the political party in the region specified by the RegionID.
  * Format: *Numerical* or *NULL* (The party did not run for election in the region specified by the RegionID)

> ##
> ###### Note:
> * Regions may be aggregates of multiple other regions. This forms a tree-like hierarchy of regions:
>   * The region "Österreich" (G00000), is an aggregate of "Burgenland" (G10000), "Kärnten" (G20000), "Niederösterreich" (G30000), "Oberösterreich" (G40000), "Salzburg" (G50000), "Steiermark" (G60000), "Tirol" (G70000), "Vorarlberg" (G80000) and "Wien" (G90000)
>   * At the same time "Burgenland" (G10000), is an aggregate of "Wahlkarten - Burgenland" (G10099), "Burgenland Nord" (G1A000) and "Burgenland Süd" (G1B000)
>   * etc.
>
> ######
> * To get a better understanding of how regions are broken down, you may visit the following links:
>   * [National Election Results 2017 (BMI-Application)][3]
>   * [National Election Results 2019 (BMI-Application)][4]
> ##

[3]: https://bundeswahlen.gv.at/2017/
[4]: https://bundeswahlen.gv.at/2019/


The following is an excerpt from the **Votes.csv** file, which is representative of the dataset's structure:

```
ElectionID,RegionID,EligibleVoters,EligibleFemale,EligibleMale,TotalVotes,InvalidVotes,ValidVotes,PartyShort,PartyVotes
NR2017,G60000,969653,,,774037,5902,768135,CPÖ,
NR2017,G60000,969653,,,774037,5902,768135,EUAUS,
NR2017,G60000,969653,,,774037,5902,768135,FLÖ,1688
NR2017,G60000,969653,,,774037,5902,768135,FPÖ,225990
NR2017,G60000,969653,,,774037,5902,768135,GILT,6523
NR2017,G60000,969653,,,774037,5902,768135,GRÜNE,21430
NR2017,G60099,,,,30,30,0,CPÖ,
NR2017,G60099,,,,30,30,0,EUAUS,
NR2017,G60099,,,,30,30,0,FLÖ,0
NR2017,G60099,,,,30,30,0,FPÖ,0
NR2017,G60099,,,,30,30,0,GILT,0
NR2017,G60100,197958,,,151765,826,150939,CPÖ,
NR2017,G60100,197958,,,151765,826,150939,EUAUS,
NR2017,G60100,197958,,,151765,826,150939,FLÖ,184
NR2017,G60100,197958,,,151765,826,150939,FPÖ,29267
NR2017,G60100,197958,,,151765,826,150939,GILT,1440
NR2017,G60101,2872,1373,1499,1617,9,1608,CPÖ,
NR2017,G60101,2872,1373,1499,1617,9,1608,EUAUS,
NR2017,G60101,2872,1373,1499,1617,9,1608,FLÖ,3
NR2017,G60101,2872,1373,1499,1617,9,1608,FPÖ,200
NR2017,G60101,2872,1373,1499,1617,9,1608,GILT,18
```

**Parties.csv:** The *Parties* file contains data on the political parties of the elections. The data points included are:

* **ElectionID:** The ID of the election to which the data row refers.
  * Format: 6-Character *String* ("NR2017" or "NR2019")
* **PartyShort:** The (unique) short name of the politicl party.
  * Format: Variable length *String* (e.g. "ÖVP")
* **PartyLong:** The long (full) name of the political party.
  * Format: Variable length *String*
* **BallotPosition:** A (unique) number identifying the political party on the ballot.
  * Format: *Numerical* or *NULL* (data is unavailable)

The following is an excerpt from the **Parties.csv** file, which is representative of the dataset's structure:

```
ElectionID,PartyShort,PartyLong,BallotPosition
NR2017,EUAUS,Für Österreich; Zuwanderungsstopp; Grenzschutz; Neutralität; EU-Austritt,
NR2017,M,Männerpartei - für ein faires Miteinander,
NR2017,CPÖ,Christliche Partei Österreichs,
NR2017,NBZ,NBZ - Neue Bewegung für die Zukunft,
NR2017,ODP,Obdachlose in der Politik,
NR2019,ÖVP,Österreichische Volkspartei,1
NR2019,SPÖ,Sozialdemokratische Partei Österreichs,2
NR2019,FPÖ,Freiheitliche Partei Österreichs,3
NR2019,NEOS,NEOS - Das Neue Österreich,4
```

**Locations.csv:** The *Locations* file contains data on Austrian regions. The data points included are:

* **ElectionID:** The ID of the election to which the data row refers.
  * Format: 6-Character *String* ("NR2017" or "NR2019")
* **RegionID:** The ID of the region (Gebiet) to which the data row refers.
  * Format: 6-Character *String* (e.g. "G60101")
* **RegionName:** The (full) name of the region specified by the RegionID.
  * Format: Variable length *String*

The following is an excerpt from the **Locations.csv** file, which is representative of the dataset's structure:

```
ElectionID,RegionID,ParentID,RegionName
NR2017,G5A099,G5A000,Wahlkarten - Salzburg Stadt
NR2017,G5B000,G50000,Flachgau/Tennengau
NR2017,G5B099,G5B000,Wahlkarten - Flachgau/Tennengau
NR2017,G5C000,G50000,Lungau/Pinzgau/Pongau
NR2017,G5C099,G5C000,Wahlkarten - Lungau/Pinzgau/Pongau
NR2017,G60000,G00000,Steiermark
NR2017,G60099,G60000,Wahlkarten - Steiermark
NR2017,G60100,G6A000,Graz(Stadt)
NR2017,G60101,G60100,Graz;Innere Stadt
NR2017,G60102,G60100,Graz;St Leonhard
NR2017,G60103,G60100,Graz;Geidorf
NR2017,G60104,G60100,Graz;Lend
NR2017,G60105,G60100,Graz;Gries
NR2017,G60106,G60100,Graz;Jakomini
NR2017,G60107,G60100,Graz;Liebenau
```
