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
* **RegionEligibleTotal:** The total number of eligible voters in the region spcified by the RegionID.
  * Format: *Numerical* or *NULL* (the total number of eligible voters is not known)
* **RegionTotalVotes:** The total number of casted votes in the region specified by the RegionID.
  * Format: *Numerical*
* **RegionInvalidVotes:** The total number of invalid casted votes in the region specified by the RegionID.
  * Format: *Numerical*
* **RegionValidVotes:** The total number of valid casted votes in the region specified by the RegionID.
  * Format: *Numerical*
* **DistrictID:** The ID of the district (Bezirk) to which the data row refers. The district is located in the region specified by the RegionID.
  * Format: *Numerical* or *NULL* (there is no district-specific data known for the given region - all of the district-specific fields will also be NULL)
* **DistrictEligibleTotal:** The total number of eligible voters in the district specified by the DistrictID.
  * Format: *Numerical* or *NULL* (the total number of eligible voters is not known or district-specific data is unavailable)
* **DistrictEligibleMale:** The number of *male* eligible voters in the district specified by the DistrictID.
  * Format: *Numerical* or *NULL* (district specific data is unavailable)
* **DistrictEligibleFemale:** The number of *female* eligible voters in the district spcified by the DistrictID.
  * Format: *Numerical* or *NULL* (district-specific data is unavailable)
* **DistrictTotalVotes:** The total number of casted votes in the district specified by the DistrictID.
  * Format: *Numerical* or *NULL* (district-specific data is unavailable)
* **DistrictInvalidVotes:** The total number of invalid casted votes in the district specified by the DistrictID.
  * Format: *Numerical* or *NULL* (district-specific data is unavailable)
* **DistrictValidVotes:** The total number of valid casted votes in the district specified by the DistrictID.
  * Format: *Numerical* or *NULL* (district specific data is unavailable)
* **PartyShort:** The (unique) short name of the politicl party.
  * Format: Variable length *String* (e.g. "ÖVP")
* **RegionPartyVotes:** The number of votes received by the political party in the region specified by the RegionID.
  * Format: *Numerical* or *NULL* (The party did not run for election in the region specified by the RegionID)
* **DistrictPartyVotes:** The number of votes received by the political party in the district specified by the DistrictID.
  * Format: *Numerical* or *NULL* (The party did not run for election in the district specified by the DistrictID or district-specific data is unavailable)

> ##
> ###### Note:
> * Regions may be aggregates of multiple other regions.
>   * e.g. The region "Österreich" (G00000), is an aggregate of "Burgenland" (G10000), "Kärnten" (G20000), "Niederösterreich" (G30000), 
>"Oberösterreich" (G40000), "Salzburg" (G50000), "Steiermark" (G60000), > "Tirol" (G70000), "Vorarlberg" (G80000) and "Wien" (G90000)
> ######
> * A region may be further separated into districts. The region is then an aggregate of all the districts. 
>   * If there is no district-specific data available for a given region, the DistrictID will be NULL as well as all of the district-related fields. 
>   * If district-specific data for a given region is available, the DistrictID will never be NULL.
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
ElectionID,RegionID,RegionEligibleTotal,RegionTotalVotes,RegionInvalidVotes,RegionValidVotes,DistrictID,DistrictEligibleTotal,DistrictEligibleMale,DistrictEligibleFemale,DistrictTotalVotes,DistrictInvalidVotes,DistrictValidVotes,PartyShort,RegionPartyVotes,DistrictPartyVotes
NR2017,G60100,197958,151765,826,150939,,,,,,,,CPÖ,,
NR2017,G60100,197958,151765,826,150939,,,,,,,,EUAUS,,
NR2017,G60100,197958,151765,826,150939,,,,,,,,FLÖ,184,
NR2017,G60100,197958,151765,826,150939,,,,,,,,FPÖ,29267,
NR2017,G60100,197958,151765,826,150939,,,,,,,,GILT,1440,
NR2017,G60100,197958,151765,826,150939,,,,,,,,GRÜNE,9467,
NR2017,G60100,197958,151765,826,150939,,,,,,,,KPÖ,3952,
NR2017,G60100,197958,151765,826,150939,,,,,,,,M,,
NR2017,G60100,197958,151765,826,150939,,,,,,,,NBZ,,
NR2017,G60100,197958,151765,826,150939,,,,,,,,NEOS,12958,
NR2017,G60100,197958,151765,826,150939,,,,,,,,ODP,,
NR2017,G60100,197958,151765,826,150939,,,,,,,,PILZ,11041,
NR2017,G60100,197958,151765,826,150939,,,,,,,,SLP,,
NR2017,G60100,197958,151765,826,150939,,,,,,,,SPÖ,41402,
NR2017,G60100,197958,151765,826,150939,,,,,,,,WEIßE,178,
NR2017,G60100,197958,151765,826,150939,,,,,,,,ÖVP,41050,
NR2017,G60101,197958,120375,704,119671,100,2872,1499,1373,1617,9,1608,CPÖ,,
NR2017,G60101,197958,120375,704,119671,100,2872,1499,1373,1617,9,1608,EUAUS,,
NR2017,G60101,197958,120375,704,119671,100,2872,1499,1373,1617,9,1608,FLÖ,156,3
NR2017,G60101,197958,120375,704,119671,100,2872,1499,1373,1617,9,1608,FPÖ,25260,200
NR2017,G60101,197958,120375,704,119671,100,2872,1499,1373,1617,9,1608,GILT,1096,18
NR2017,G60101,197958,120375,704,119671,100,2872,1499,1373,1617,9,1608,GRÜNE,6932,121
NR2017,G60101,197958,120375,704,119671,100,2872,1499,1373,1617,9,1608,KPÖ,3145,62
NR2017,G60101,197958,120375,704,119671,100,2872,1499,1373,1617,9,1608,M,,
NR2017,G60101,197958,120375,704,119671,100,2872,1499,1373,1617,9,1608,NBZ,,
NR2017,G60101,197958,120375,704,119671,100,2872,1499,1373,1617,9,1608,NEOS,9763,171
NR2017,G60101,197958,120375,704,119671,100,2872,1499,1373,1617,9,1608,ODP,,
NR2017,G60101,197958,120375,704,119671,100,2872,1499,1373,1617,9,1608,PILZ,8507,165
NR2017,G60101,197958,120375,704,119671,100,2872,1499,1373,1617,9,1608,SLP,,
NR2017,G60101,197958,120375,704,119671,100,2872,1499,1373,1617,9,1608,SPÖ,33017,425
NR2017,G60101,197958,120375,704,119671,100,2872,1499,1373,1617,9,1608,WEIßE,148,3
NR2017,G60101,197958,120375,704,119671,100,2872,1499,1373,1617,9,1608,ÖVP,31647,440
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

> ##
> ###### Note:
> * The long (full) name of a political party may change between elections.
> ##


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
* **DistrictID:** The ID of the district (Bezirk) to which the data row refers. The district is located in the region specified by the RegionID.
  * Format: *Numerical* or *NULL* (there is no district-specific data known for the given region - all of the district-specific fields will also be NULL)
* **DistrictName:** The (full) name of the district specified by the DistrictID.
  * Format: Variable length *String* or *NULL* (district-specific data is unavailable)
* **#AdministrativeDistricts:** The number of administrative districts (Sprengel) located in the district specified by the DistrictID.
  * Format: *Numerical* or *NULL*  (district-specific data is unavailable)

The following is an excerpt from the **Locations.csv** file, which is representative of the dataset's structure:

```
ElectionID,RegionID,RegionName,DistrictID,DistrictName,#AdministrativeDistricts
NR2017,G5A000,Salzburg Stadt,,,
NR2017,G5A099,Wahlkarten - Salzburg Stadt,,,
NR2017,G5B000,Flachgau/Tennengau,,,
NR2017,G5B099,Wahlkarten - Flachgau/Tennengau,,,
NR2017,G5C000,Lungau/Pinzgau/Pongau,,,
NR2017,G5C099,Wahlkarten - Lungau/Pinzgau/Pongau,,,
NR2017,G60000,Steiermark,,,
NR2017,G60099,Wahlkarten - Steiermark,,,
NR2017,G60100,Graz(Stadt),,,
NR2017,G60101,Graz,100,Innere Stadt,4
NR2017,G60101,Graz,200,St Leonhard,15
NR2017,G60101,Graz,300,Geidorf,24
NR2017,G60101,Graz,400,Lend,26
NR2017,G60101,Graz,500,Gries,24
NR2017,G60101,Graz,600,Jakomini,31
NR2017,G60101,Graz,700,Liebenau,14
NR2017,G60101,Graz,800,St.Peter,16
```
