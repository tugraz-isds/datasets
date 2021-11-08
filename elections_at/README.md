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
> * Regions may be aggregates of multiple other regions.
>   * e.g. The region "Österreich" (G00000), is an aggregate of "Burgenland" (G10000), "Kärnten" (G20000), "Niederösterreich" (G30000), 
>"Oberösterreich" (G40000), "Salzburg" (G50000), "Steiermark" (G60000), > "Tirol" (G70000), "Vorarlberg" (G80000) and "Wien" (G90000)
>
> ######
> * To get a better understanding of how regions are broken down, you may visit the following links:
>   * [National Election Results 2017 (BMI-Application)][3]
>   * [National Election Results 2019 (BMI-Application)][4]
>   * Note that these break downs include **only regions**.
> ##

[3]: https://bundeswahlen.gv.at/2017/
[4]: https://bundeswahlen.gv.at/2019/


The following is an excerpt from the **Votes.csv** file, which is representative of the dataset's structure:

```
ElectionID,RegionID,EligibleVoters,TotalVotes,InvalidVotes,ValidVotes,PartyShort,PartyVotes
NR2017,G60117,5623,3684,23,3661,FPÖ,1178
NR2017,G60117,5623,3684,23,3661,GILT,35
NR2017,G60117,5623,3684,23,3661,GRÜNE,95
NR2017,G60117,5623,3684,23,3661,KPÖ,81
NR2017,G60117,5623,3684,23,3661,M,
NR2017,G60117,5623,3684,23,3661,NBZ,
NR2017,G60117,5623,3684,23,3661,NEOS,219
NR2017,G60117,5623,3684,23,3661,ODP,
NR2017,G60117,5623,3684,23,3661,PILZ,162
NR2017,G60117,5623,3684,23,3661,SLP,
NR2017,G60117,5623,3684,23,3661,SPÖ,942
NR2017,G60117,5623,3684,23,3661,WEIßE,4
NR2017,G60117,5623,3684,23,3661,ÖVP,940
NR2017,G60199,,31390,122,31268,CPÖ,
NR2017,G60199,,31390,122,31268,EUAUS,
NR2017,G60199,,31390,122,31268,FLÖ,28
NR2017,G60199,,31390,122,31268,FPÖ,4007
NR2017,G60199,,31390,122,31268,GILT,344
NR2017,G60199,,31390,122,31268,GRÜNE,2535
NR2017,G60199,,31390,122,31268,KPÖ,807
NR2017,G60199,,31390,122,31268,M,
NR2017,G60199,,31390,122,31268,NBZ,
NR2017,G60199,,31390,122,31268,NEOS,3195
NR2017,G60199,,31390,122,31268,ODP,
NR2017,G60199,,31390,122,31268,PILZ,2534
NR2017,G60199,,31390,122,31268,SLP,
NR2017,G60199,,31390,122,31268,SPÖ,8385
NR2017,G60199,,31390,122,31268,WEIßE,30
NR2017,G60199,,31390,122,31268,ÖVP,9403
NR2017,G60300,50288,40062,366,39696,CPÖ,
NR2017,G60300,50288,40062,366,39696,EUAUS,
NR2017,G60300,50288,40062,366,39696,FLÖ,90
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

**Locations.csv:** The *Locations* file contains data on Austrian regions and districts. The data points included are:

* **ElectionID:** The ID of the election to which the data row refers.
  * Format: 6-Character *String* ("NR2017" or "NR2019")
* **RegionID:** The ID of the region (Gebiet) to which the data row refers.
  * Format: 6-Character *String* (e.g. "G60101")
* **RegionName:** The (full) name of the region specified by the RegionID.
  * Format: Variable length *String*
* **DistrictName:** The (full) name of the district specified by the DistrictID.
  * Format: Variable length *String* or *NULL* (district-specific data is unavailable)

The following is an excerpt from the **Locations.csv** file, which is representative of the dataset's structure:

```
ElectionID,RegionID,ParentID,RegionName,DistrictName
NR2017,G60114,G60100,Graz,Eggenberg
NR2017,G60115,G60100,Graz,Wetzelsdorf
NR2017,G60116,G60100,Graz,Straßgang
NR2017,G60117,G60100,Graz,Puntigam
NR2017,G60199,G60100,Wahlkarten - Graz(Stadt),
NR2017,G60300,G6C000,Deutschlandsberg,
NR2017,G60305,G60300,Frauental an der Laßnitz,
NR2017,G60318,G60300,Lannach,
NR2017,G60323,G60300,Pölfing-Brunn,
NR2017,G60324,G60300,Preding,
NR2017,G60326,G60300,Sankt Josef (Weststeiermark),
NR2017,G60329,G60300,Sankt Peter im Sulmtal,
NR2017,G60341,G60300,Wettmannstätten,
NR2017,G60344,G60300,Deutschlandsberg,
NR2017,G60345,G60300,Eibiswald,
NR2017,G60346,G60300,Groß Sankt Florian,
NR2017,G60347,G60300,Sankt Martin im Sulmtal,
NR2017,G60348,G60300,Sankt Stefan ob Stainz,
NR2017,G60349,G60300,Schwanberg,
NR2017,G60350,G60300,Stainz,
NR2017,G60351,G60300,Wies,
NR2017,G60399,G60300,Wahlkarten - Deutschlandsberg,
NR2017,G60600,G6A000,Graz-Umgebung,
NR2017,G60608,G60600,Feldkirchen bei Graz,
NR2017,G60611,G60600,Gössendorf,
NR2017,G60613,G60600,Gratkorn,
NR2017,G60617,G60600,Hart bei Graz,
NR2017,G60618,G60600,Haselsdorf-Tobelbad,
NR2017,G60619,G60600,Hausmannstätten,
NR2017,G60623,G60600,Kainbach bei Graz,
NR2017,G60624,G60600,Kalsdorf bei Graz,
NR2017,G60626,G60600,Kumberg,
NR2017,G60628,G60600,Laßnitzhöhe,
NR2017,G60629,G60600,Lieboch,
```
