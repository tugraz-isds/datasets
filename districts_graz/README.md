# Districts of Graz (2006-2022)

## Overview

The following dataset is a collection of:
*  Graz population records from 2006-01-01 to 2022-01-01 (inclusive) as well as
*  educational institutions located in Graz.

All the records comprised within the datasets are stored in 5 denormalized CSV files (with ',' delimiter and simplified structure without the need for quoting): Districts.csv, EducationalInstitutions.csv, PopulationByCitizenship.csv, and PopulationByGender.csv.

The dataset used for the assignment is a derivative of datasets obtained from the following public data sources under license Creative Commons Namensnennung 4.0 International ([CC BY 4.0][3]):
* [Open Data Österreich][1]
* [Open Government Data Graz][2]

[1]: https://www.data.gv.at/
[2]: https://ckan.data.graz.gv.at
[3]: https://creativecommons.org/licenses/by/4.0/deed.de


## Structure
**Districts.csv** The *Districts* file contains general data on the districts of Graz. The data points have the following structure:

* **DistrictID:**  The unique ID of the district.
  * Format: *numerical*
* **Name:** The name of the district.
  * Format: variable length *string*
* **Population:** The population count in the district as of 1st January 2022.
  * Format: *numerical*
* **LandArea:** The area of the district, given in square kilometers $[km^2]$.
  * Format: *numerical*
* **PostalCodes:** A '|' separated list of all postal codes used in the district.
  * Format: *Code1|Code2*
    * Code is *numerical*

The following is an excerpt from the **Districts.csv** file, which is representative of the dataset's structure:

```
DistrictID,Name,Population,LandArea,PostalCodes
1,Innere Stadt,3446,1.16,8010
2,St. Leonhard,15075,1.83,8010|8047
3,Geidorf,24301,5.5,8010|8036|8043
4,Lend,31711,3.7,8020|8051
5,Gries,30352,5.05,8020|8053|8055
6,Jakomini,31908,4.06,8010|8041|8042
```

**Streets.csv** The *Streets* file contains the streets of Graz. The data points have the following structure:

StreetID,StreetName,DistrictID

* **StreetID:**  The unique ID of the streets.
  * Format: *numerical*
* **StreetName:** The name of the street.
  * Format: variable length *string*
* **DistrictID:** A '|' separated list of the district's IDs, through which the street goes.
  * Format: *DistrictID1|DistrictID2*
    * DistrictID is *numerical*

The following is an excerpt from the **Streets.csv** file, which is representative of the dataset's structure:

```
StreetID,StreetName,DistrictID
106,Alberstraße,2
114,Albert-Schweitzer-Gasse,5
108,Albrechtgasse,1
109,Alexander-Rollett-Weg,3
100,Alfafarweg,7
111,Alfred-Coßmann-Gasse,16
110,Algersdorfer Straße,14
115,Allerheiligenweg,14
104,Alois-Kabelka-Weg,15
113,Alpassy-Pastirk-Gasse,12
112,Alte Poststraße,4|5|14|15|16|17
```



**Institutions.csv:**  The *EducationalInstitutions* file contains data on the educational institutions located in Graz. The data points have the following structure:

* **Name:** The name of the institution.
  * Format: variable length *string*
* **Address:** The address of the institution including the street name and number.
  * Format: variable length *string*
* **PostalCode:** The postal code of the institution.
  * Format: 4-digit *numerical* value
* **PhoneNumber:** The phone number of the institution.
  * Format: a variable length *string* starting with '+43(0)316'
* **InstitutionsCategory:** The category to which the institution belongs to.
  * Format: variable lenght *string*
* **InstitutionsType:** The type of the institution.
  * Format: variable length *string*

The following is an excerpt from the **EducationalInstitutions.csv** file, which is representative of the dataset's structure:

```
Name,Address,PostalCode,PhoneNumber,InstitutionsCategory,InstitutionsType
TU-Graz; Fakultät für Informatik; IICM; CGV,Inffeldgasse 16c,8010,+43(0)3168735613,Universitäten; Hoch- & Fachhochschulen,Technische Universität Graz
TU-Graz; Fakultät für Informatik; IWM,Inffeldgasse 21a,8010,+43(0)3168739251,Universitäten; Hoch- & Fachhochschulen,Technische Universität Graz
Uni-Graz; Institut der Fakultät für Sozial- u. Wirtschaftswissenschaften,Elisabethstraße 50b,8010,+43(0)3163807189,Universitäten; Hoch- & Fachhochschulen,Karl-Franzens-Universität Graz
Uni-Graz; Karl-Franzens-Universität,Attemsgasse 8,8010,+43(0)3163800,Universitäten; Hoch- & Fachhochschulen,Karl-Franzens-Universität Graz
FH Joanneum; Radiologietechnologie,Eggenberger Allee 13,8020,+43(0)31654536570,Universitäten; Hoch- & Fachhochschulen,Fachhochschule
KUG Institut 2 Klavier,Brandhofgasse 21/III,8010,+43(0)3163893020,Universitäten; Hoch- & Fachhochschulen,Kunstuniversität Graz
Uni-Graz; Institut für Soziologie; Frauen- und Geschlechterforschung,Strassoldogasse 10,8010,+43(0)3163807088,Universitäten; Hoch- & Fachhochschulen,Karl-Franzens-Universität Graz
TU-Graz; Institute der Fakultät für Technische Mathematik u. Technische Physik,Münzgrabenstraße 11,8010,+43(0)3168736475,Universitäten; Hoch- & Fachhochschulen,Technische Universität Graz
```

**PopulationByCitizenship.csv:** The *PopulationByCitizenship* file contains data on the yearly population in Graz based on citizenship. The data points included are:

* **Date:** The date of the population count.
  * Format: *yyyy-mm-dd*
* **DistrictID:** The id of the district to which the population count refers to.
  * Format: *numerical*
* **Citizenship:** The name of the country from which the population comes from or one of [stateless, unresolved, unknown].
  * Format: variable length *string*
* **EUStatus:** Refers to the EU status of the country.
  * Format: one of the following:
    * *A* = Austria
    * *EU* = Member of the European Union
    * *N-EU* = Not a Member of the European Union
* **Count:** The population count.
  * Format: *numerical*

The following is an excerpt from the **PopulationByCitizenship.csv** file, which is representative of the dataset's structure:

```
Date,DistrictID,Citizenship,EUStatus,Count
2006-01-01,2,Austria,A,15145
2006-01-01,2,Pakistan,N-EU,7
2006-01-01,2,Paraguay,N-EU,1
2006-01-01,2,Peru,N-EU,1
2006-01-01,2,Poland,EU,26
2006-01-01,2,Portugal,EU,3
2006-01-01,2,Rwanda,N-EU,1
2006-01-01,2,Romania,N-EU,38
...
2022-01-01,17,Korea; Republic of,N-EU,2
2022-01-01,17,Kosovo,N-EU,78
2022-01-01,17,Croatia,EU,585
2022-01-01,17,Latvia,EU,10
2022-01-01,17,Lebanon,N-EU,2
2022-01-01,17,Malaysia,N-EU,2
2022-01-01,17,Malta,EU,1
2022-01-01,17,Morocco,N-EU,2

```

**PopulationByGender.csv:** The *PopulationByGender* file contains data on Austrian regions. The data points included are:
* **Date:** The date of the population count.
  * Format: *yyyy-mm-dd*
* **DistrictID:** The id of the district to which the population count refers to.
  * Format: *numerical*
* **Gender:** The gender of the population.
  * Format: one of the following:
    * *M* = Male
    * *F* = Female
    * *O* = Other
* **Count:** The population count.
  * Format: *numerical*


The following is an excerpt from the **PopulationByGender.csv** file, which is representative of the dataset's structure:

```
DistrictID,Date,Gender,Count
2021-08-01,1,M,2206
2021-08-01,1,W,1983
2021-08-01,2,M,8988
2021-08-01,2,W,9520
2021-08-01,3,M,13862
2021-08-01,3,W,15894
2021-08-01,4,M,17437
2021-08-01,4,W,17267
2021-08-01,5,M,18010
2021-08-01,5,W,15645
2021-08-01,6,M,18921
2021-08-01,6,O,1
2021-08-01,6,W,17905
2021-08-01,7,M,8487
2021-08-01,7,W,8573
```