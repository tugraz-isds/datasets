# Districts of Graz (2006-2022)

## Overview

The following dataset is a collection of:
*  Graz population records from 2006-01-01 to 2022-01-01 (inclusive) as well as
*  educational institutions located in Graz.

All the records comprised within the datasets are stored in 4 denormalized CSV files (with ',' delimiter and simplified structure without the need for quoting): Districts.csv, EducationalInstitutions.csv, PopulationByCitizenship.csv, and PopulationByGender.csv.

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
* **Streets:** A '|' separated list of the streets located in the district and their id.
  * Format: *StreetName1=StreetID1|StreetName2=StreetID2*
    * StreetName is a varible length *string*
    * StreetID is *numerical*

The following is an excerpt from the **Districts.csv** file, which is representative of the dataset's structure:

```
DistrictID,Name,Population,LandArea,PostalCodes,Streets
1,Innere Stadt,3446,1.16,8010,Abraham-a-Santa-Clara-Gasse=1|Admonter Gasse=39|Albrechtgasse=108|Am Eisernen Tor=130|Am Fuße des Schloßberges=134|Andreas-Hofer-Platz=158|Baden-Powell-Allee=303|Badgasse=304|Ballhausgasse=312|Bindergasse=402|Bischofplatz=403|Bürgergasse=578|Burggarten=583|Burggasse=579|Burgring=580|Coventrypromenade=669|Davidgasse=702|Dr.-Karl-Böhm-Allee=856|Dr.-Muck-Anlage=843|Dubrovnik Allee=875|Einspinnergasse=972|Elise-Steininger-Steg=990|Emichplatzl=997|Enge Gasse=1006|Erich-Edegger-Steg=1020|Erzherzog-Johann-Allee=1029|Europaratweg=1058|Färbergasse=1105|Färberplatz=1106|Felsensteig=1139|Fischer-von-Erlach-Gasse=1166|Franz-Graf-Allee=1253|Franziskanergasse=1255|Franziskanerplatz=1256|Frauengasse=1261|Freiheitsplatz=1263|Friedrich-von-Gagern-Allee=1280|Girardigasse=1366|Glacisstraße=1396|Gleisdorfer Gasse=1398|Glockenspielplatz=1399|Gorbachplatz=1440|Groningenplatz=1496|Hamerlinggasse=1508|Hans-Sachs-Gasse=1518|Hartiggasse=1526|Hauptplatz=1533|Henri-Dunant-Weg=1587|Herrengasse=1573|Hofgasse=1667|Jahngasse=1900|Jakominiplatz=1906|Jerusalemplatz=1943|Joanneumsviertel=1949|Joanneumring=1951|Jungferngasse=1993|Kaiserfeldgasse=2003|Kaiser-Franz-Josef-Kai=2004|Kaiser-Josef-Platz=2005|Kalchberggasse=2007|Kapaunplatz=2012|Kapistran-Pieller-Platz=2015|Karmeliterplatz=2024|Korbgasse=2191|Kriegssteig=2228|Landhausgasse=2303|Major-Hackher-Weg=2504|Marburger Kai=2510|Maria-Theresia-Allee=2515|Mehlplatz=2552|Mesnergasse=2554|Montclair Allee=2684|Murgasse=2760|Nelkengasse=2841|Neue Welt=2850|Neue-Welt-Gasse=2852|Neutorgasse=2863|Nürnbergergasse=2961|Opernring=3091|Palais Trauttmansdorff-Passage=3220|Paradeisgasse=3204|Parkring=3206|Parkstraße=3207|Paulustorgasse=3209|Pecs Allee=3229|Platz der Ehrenamtlichen=3321|Platz der Menschenrechte=3314|Platz der Versöhnung=3312|Pomeranzengasse=3328|Prokopigasse=3359|Radetzkystraße=3452|Raubergasse=3459|Ritter-von-Formentini-Allee=3600|Robert-Stolz-Promenade=3629|Roseggergarten=3643|Sackstraße=3750|Salzamtsgasse=3752|Sauraugasse=3760|Schloßberg=3807|Schloßbergplatz=3808|Schlossergasse=3810|Schmiedgasse=3813|Sparkassenplatz=3959|Sporgasse=3964|Stadtpark=3983|Stainzergasse=3985|Stempfergasse=3998|Stiegengasse=4004|Stubenberggasse=4046|Trauttmansdorffgasse=4229|Tummelplatz=4266|Weldenstraße=4659|Wickenburggasse=4691|Wiednerplätzchen=4703|Wilhelm-Fischer-Allee=4698|Wurmbrandgasse=4771|Erzherzog-Johann-Brücke=5002|Keplerbrücke=5001|Radetzkybrücke=5004|Tegetthoffbrücke=5003
2,St. Leonhard,15075,1.83,8010|8047,Alberstraße=106|Beethovenstraße=351|Berthold-Linder-Weg=361|Brandhofgasse=512|Brockmanngasse=518|Dietrichsteinplatz=761|Dürergasse=881|Eduard-Richter-Gasse=924|Elisabethstraße=987|Engelgasse=1007|Felix-Dahn-Platz=1137|Friedensgasse=1265|Friedrich-Hebbel-Gasse=1269|Gabriel-Seidl-Gasse=1302|Gartengasse=1306|Gaußgasse=1315|Glacisstraße=1396|Gleisdorfer Gasse=1398|Hallerschloßstraße=1507|Hans-Brandstetter-Gasse=1557|Hartenaugasse=1522|Hauslabgasse=1536|Haydngasse=1537|Herrandgasse=1572|Hohlweg=1672|Jakominiplatz=1906|Jensengasse=1941|Johannes-Zwerger-Platz=1947|Kaiser-Josef-Platz=2005|Katzianergasse=2028|Koßgasse=2198|Krenngasse=2224|Leonhardgürtel=2347|Leonhardplatz=2348|Leonhardstraße=2349|Lessingstraße=2351|Lichtenfelsgasse=2381|Luthergasse=2464|Maiffredygasse=2501|Mandellstraße=2507|Merangasse=2553|Morellenfeldgasse=2685|Naglergasse=2800|Nibelungengasse=2881|Obstgasse=3004|Odilienweg=3041|Pappenheimgasse=3203|Paracelsusgasse=3224|Pauluzzigasse=3217|Petersgasse=3239|Plüddemanngasse=3311|Ragnitzstraße=3455|Raimundgasse=3456|Rechbauerstraße=3511|Reiterweg=3518|Reitschulgasse=3519|Rembrandtgasse=3520|Riesstraße=3574|Ruckerlberggasse=3701|Ruckerlberggürtel=3702|Schillerplatz=3797|Schillerstraße=3798|Schlögelgasse=3806|Schörgelgasse=3820|Schumanngasse=3831|Schützenhofgasse=3832|Seebachergasse=3851|Semmelweisgasse=3855|Siemensgasse=3894|Sonnenstraße=3921|Sparbersbachgasse=3961|Swethgasse=4091|Technikerstraße=4131|Tegetthoffplatz=4132|Uhlandgasse=4351|Waltendorfer Gürtel=4612|Wastiangasse=4618|Wittekweg=4709|Zwerggasse=4988
3,Geidorf,24301,5.5,8010|8036|8043,Aigner-Rollett-Allee=92|Alexander-Rollett-Weg=109|Am Hofacker=135|Amschlgasse=149|Amundsengasse=197|Anton-Füster-Weg=166|Anton-Leb-Gasse=171|Attemsgasse=241|Auenbruggerplatz=265|Auersperggasse=257|August-Musger-Gasse=262|Baumschulgasse=316|Beethovenstraße=351|Bergmanngasse=353|Blütengasse=453|Bogengasse=482|Brandhofgasse=512|Brunngasse=525|Carnerigasse=601|Charlottendorfgasse=641|Droste-Hülshoff-Gasse=770|Eichendorffstraße=967|Elisabethstraße=987|Elise-Steininger-Steg=990|Eschenbachgasse=1041|Fischergasse=1164|Födranspergweg=1226|Franckstraße=1252|Fritz-Pregl-Weg=1271|Geidorfgürtel=1332|Geidorfplatz=1333|Glacisstraße=1396|Goethestraße=1423|Grabengürtel=1446|Grabenhofenweg=1447|Grabenstraße=1448|Grillparzerstraße=1469|Gustav-Scherbaum-Promenade=1498|Halbärthgasse=1506|Hans-Friz-Weg=1515|Harrachgasse=1525|Hartenaugasse=1522|Hasnerplatz=1530|Heinrich-Casper-Gasse=1564|Heinrichstraße=1567|Herdergasse=1570|Hilgergasse=1611|Hilmgasse=1612|Hilmteichstraße=1613|Hochsteingasse=1662|Holteigasse=1676|Hugo-Schuchardt-Straße=1746|Hugo-Wolf-Gasse=1747|Humboldtstraße=1750|Humperdinckgasse=1751|Jahngasse=1900|Jakob-Dirnböck-Gasse=1902|Jakobsleiter=1904|Johann-Fux-Gasse=1952|Johann-Michael-Steffn-Weg=1955|Johann-Strauß-Gasse=1959|Kahngasse=2000|Kettengasse=2052|Kirchengasse=2084|Kirschengasse=2090|Körblergasse=2192|Körösistraße=2195|Kreuzgasse=2225|Laimburggasse=2302|Lange Gasse=2304|Leechgasse=2341|Lehargasse=2354|Lenaugasse=2343|Leonhardplatz=2348|Liebiggasse=2386|Liliencrongasse=2387|Lindweg=2394|Ludwig-Seydler-Gasse=2462|Makartgasse=2505|Martha-Tausk-Park=2530|Mautgasse=2527|Max-Mell-Allee=2542|Merangasse=2553|Millöckergasse=2592|Mozartgasse=2689|Muchargasse=2751|Ortweingasse=3120|Panoramagasse=3201|Parkstraße=3207|Peinlichgasse=3231|Quellengasse=3411|Rembrandtgasse=3520|Richard-Wagner-Gasse=3572|Riesstraße=3574|Rittergasse=3576|Robert-Stolz-Gasse=3632|Roseggerweg=3644|Rosenberggasse=3647|Rosenberggürtel=3648|Rosenhain=3652|Rosenhaingasse=3650|Rottalgasse=3656|Rückertgasse=3703|Saumgasse=3759|Schanzelgasse=3791|Scheidtenbergergasse=3793|Schönbrunngasse=3819|Schröckingerweg=3846|Schröttergasse=3847|Schubertstraße=3825|Schwimmschulkai=3837|Seebachergasse=3851|Sonnenfelsplatz=3918|Steggasse=3989|Stiftingtalstraße=4049|Strassoldogasse=4041|Theodor-Körner-Straße=4170|Uferweg=4331|Universitätsplatz=4422|Universitätsstraße=4423|Villefortgasse=4542|Vogelweiderstraße=4572|Wartingergasse=4614|Wassergasse=4615|Wastlergasse=4616|Weg zum Reinerkogel=4642|Wickenburggasse=4691|Wilhelm-Kienzl-Gasse=4699|Wilhelm-Raabe-Gasse=4700|Wormgasse=4731|Ziernfeldgasse=4938|Zinzendorfgasse=4940|Zusertalgasse=4971|Kalvarienbrücke=5009|Keplerbrücke=5001
4,Lend,31711,3.7,8020|8051,Afritschgasse=66|Alte Poststraße=112|Am Damm=128|Am Freigarten=131|Am Fröbelpark=132|Annenstraße=164|Anton-Gerstl-Straße=167|Asperngasse=216|Augasse=261|Austeingasse=263|Babenbergerstraße=300|Bahnhofgürtel=305|Baumkircherstraße=315|Bienengasse=401|Buhnengasse=573|Bunsengasse=574|Darmstadtgasse=705|Daungasse=701|Doblergasse=781|Dominikanerriegel=783|Dorngasse=786|Dreierschützengasse=847|Eggenberger Straße=943|Erich-Edegger-Steg=1020|Erlengasse=1027|Esperantoplatz=1043|Europaplatz=1061|Fellingergasse=1138|Fichtestraße=1161|Floßlendplatz=1195|Floßlendstraße=1196|Friedenspark=1283|Fröbelgasse=1272|Gabelsbergerstraße=1300|Ghegagasse=1356|Glasfabrikstraße=1397|Grimmgasse=1473|Grüne Gasse=1477|Hackhergasse=1502|Hans-List-Platz=1523|Hans-Resel-Gasse=1517|Hanuschgasse=1552|Heimgartenweg=1584|Hirtengasse=1617|Josefigasse=1973|Kalvarienbergstraße=2009|Kalvariengürtel=2010|Keplerstraße=2043|Kinkgasse=2082|Kleiststraße=2122|Komzakgasse=2206|Konsumweg=2194|Kosakengasse=2196|Lastenstraße=2306|Laudongasse=2309|Lendkai=2344|Lendplatz=2345|Leuzenhofgasse=2352|Mariahilferplatz=2513|Mariahilferstraße=2514|Mariengasse=2517|Marienplatz=2518|Marschallgasse=2523|Metahofgasse=2557|Mohsgasse=2681|Mühlgasse=2753|Mühlriegel=2754|Netzgasse=2845|Neubaugasse=2846|Neue Bienengasse=2848|Ökonomiegasse=3066|Orpheumgasse=3113|Ostwaldgasse=3132|Papiermühlgasse=3202|Peter-Tunner-Gasse=3235|Pflanzengasse=3264|Plabutscherstraße=3306|Pommergasse=3330|Radgasse=3453|Rebengasse=3526|Reinbacherweg=3516|Remygasse=3521|Resselgasse=3522|Schleifbachgasse=3804|Schmölzergasse=3814|Schrödingerstraße=3824|Sigmundstadl=3895|St.-Georgen-Gasse=4053|Stahlgasse=3984|Starhemberggasse=3987|Stigergasse=4010|Stockergasse=4011|Stradiotgasse=4019|Strauchergasse=4042|Südtiroler Platz=4073|Trondheimgasse=4233|Überfuhrgasse=4300|Viktor-Franz-Straße=4550|Volksgarten=4579|Volksgartenstraße=4573|Waagner-Biro-Straße=4623|Waldertgasse=4608|Weißeneggergasse=4652|Wiener Straße=4693|Wolkensteingasse=4720|Zeillergasse=4916|Zollgasse=4956|Erzherzog-Johann-Brücke=5002|Kalvarienbrücke=5009|Keplerbrücke=5001
5,Gries,30352,5.05,8020|8053|8055,Adalbert-Stifter-Gasse=36|Ägydigasse=76|Albert-Schweitzer-Gasse=114|Alte Poststraße=112|Am Innovationspark=205|Am Lindenkreuz=139|Amselgasse=150|Andrägasse=157|Annenstraße=164|Arche Noah=195|Arnold-Luschin-Gasse=201|Auf der Tändelwiese=259|Belgiergasse=352|Bessemergasse=358|Bethlehemgasse=359|Bozener Straße=483|Brückengasse=519|Brückenkopfgasse=520|Buchkogelgasse=572|Bürgerspitalgasse=582|Custozzagasse=676|David-Herzog-Platz=710|Defreggergasse=730|Dominikanergasse=782|Dornschneidergasse=787|Dorothee-Sölle-Weg=792|Dr.-Hans-Spitzy-Platzl=835|Dr.-Schlossar-Park=853|Dreihackengasse=848|Eggenberger Gürtel=942|Eggenberger Straße=943|Elisabethinergasse=986|Entenplatz=1009|Fabriksgasse=1100|Falkenhofgasse=1103|Fasangartengasse=1107|Feldgasse=1129|Feuerbachgasse=1141|Finkengasse=1162|Florianigasse=1193|Franz-Riepl-Gasse=1257|Friedhofgasse=1266|Granatengasse=1452|Grasweg=1456|Grenadiergasse=1461|Griesgasse=1466|Grieskai=1467|Griesplatz=1468|Großmarktstraße=1491|Gürtelturmplatz=1485|Hammer-Purgstall-Gasse=1510|Hans-Groß-Gasse=1516|Hedwig-Katschinka-Straße=1588|Hermann-Bahr-Gasse=1579|Hermann-Löns-Gasse=1571|Herrgottwiesgasse=1574|Hohenstaufengasse=1670|Idlhofgasse=1811|Igelgasse=1821|Jakob-Lorber-Gasse=1926|Josef-Huber-Gasse=1964|Josef-Hyrtl-Gasse=1965|Kantgasse=2011|Kapellenstraße=2014|Karlauergürtel=2017|Karlauerstraße=2018|Karlauplatz=2019|Kärntner Straße=2025|Kernstockgasse=2045|Kindermanngasse=2081|Kleegasse=2121|Köflacher Gasse=2182|Korngasse=2193|Köstenbaumgasse=2197|Kratkystraße=2237|Kurze Gasse=2261|Lagergasse=2301|Laubgasse=2307|Lauzilgasse=2315|Lazarettgasse=2310|Lazarettgürtel=2311|Lidlsdorfgasse=2383|Limonigasse=2389|Lissagasse=2395|Martingasse=2524|Mauergasse=2526|Niesenbergergasse=2882|Nikolaigasse=2883|Nikolaiplatz=2891|Oeverseegasse=3051|Paula-Wallisch-Straße=3226|Payer-Weyprecht-Straße=3210|Peter-Rosegger-Straße=3234|Pflastergasse=3265|Platz der Freiwilligen Schützen=3313|Prankergasse=3357|Prokesch-Osten-Gasse=3358|Puchstraße=3376|Quergasse=3413|Rankengasse=3457|Reichengasse=3514|Reiherstadlgasse=3515|Rosenkranzgasse=3653|Rösselmühlgasse=3655|Sahlaweg=3765|Schiffgasse=3796|Schröderhofweg=3826|Schützgasse=3848|Sechsundzwanziger-Schützen-Gasse=3852|Siebenundvierzigergasse=3891|St.-Andräplatz=3969|Staatsbahnstraße=3981|Stadlgasse=3982|Steinfeldgasse=3993|Sterngasse=4000|Storchgasse=4013|Sturzgasse=4047|Südbahnstraße=4071|Südliches Lazarettfeld=4072|Südtiroler Platz=4073|Tiergartenweg=4196|Traungauergasse=4228|Triester Straße=4230|Ungergasse=4421|Viehmarktgasse=4541|Vinzenz-Muchitsch-Straße=4551|Vorbeckgasse=4574|Weißenhofgasse=4653|Wetzelsdorfer Straße=4661|Wiesengasse=4695|Zweiglgasse=4987|Augartenbrücke=5005|Augartensteg=5015|Bertha-von-Suttner-Friedensbrücke=5006|Eisenbahnbrücke=5007|Erzherzog-Johann-Brücke=5002|Puchsteg=5012|Radetzkybrücke=5004|Tegetthoffbrücke=5003
6,Jakomini,31908,4.06,8010|8041|8042,Ackergasse=21|Adolf-Kolping-Gasse=40|Am Langedelwehr=156|Angergasse=161|Anzengrubergasse=170|Arndtgasse=200|Borromäumgasse=485|Brahmsstraße=511|Brockmanngasse=518|Brucknerstraße=521|Buchenweg=571|Conrad-von-Hötzendorf-Straße=661|Dietrichsteinplatz=761|Dr.-Plochl-Straße=855|Dr.-Robert-Sieger-Straße=842|Draisgasse=846|Ehrenfelsgasse=957|Emil-Ertl-Gasse=996|Engelbert-Rückl-Gasse=1005|Ernst-Haeckel-Straße=1028|Evangelimanngasse=1065|Fliedergasse=1191|Flurgasse=1197|Friedrichgasse=1268|Friedrich-Kaulbach-Straße=1270|Fröhlichgasse=1273|Froschaugasse=1277|Gartenstadtstraße=1309|Genossenschaftsweg=1334|Grazbachgasse=1457|Hafnerriegel=1504|Händelstraße=1513|Harmsdorfgasse=1520|Haselweg=1528|Heckenweg=1583|Hollerweg=1675|Hüttenbrennergasse=1752|Inffeldgasse=1850|Jakob-Redtenbacher-Gasse=1915|Jakominigürtel=1905|Jakominiplatz=1906|Jakoministraße=1907|Jauerburggasse=1911|Johann-Sebastian-Bach-Gasse=1950|Josef-Pongratz-Platz=1979|Karl-Maria-von-Weber-Gasse=2021|Karl-Schönherr-Gasse=2031|Kasernstraße=2026|Kastellfeldgasse=2027|Keesgasse=2041|Klosterwiesgasse=2124|Kochstraße=2181|Konrad-Deubler-Gasse=2189|Kopernikusgasse=2190|Kronesgasse=2230|Leitnergasse=2342|Liebenauer Tangente=2405|Maygasse=2502|Messeplatz=2555|Mondscheingasse=2682|Monsbergergasse=2690|Moserhofgasse=2688|Mühlgangweg=2752|Münzgrabengürtel=2767|Münzgrabenstraße=2758|Neufeldweg=2854|Neuholdaugasse=2858|Neulandgasse=2859|Nordweg=2922|Obere Bahnstraße=3000|Ortweinplatz=3112|Pestalozzistraße=3233|Petersgasse=3239|Plankengasse=3308|Pomisgasse=3329|Pula Kai=3374|Purgleitnerstraße=3381|Radetzkystraße=3452|Raiffeisenstraße=3468|Reitschulgasse=3519|Roseggerkai=3642|Sandgasse=3753|Scheigergasse=3794|Schießstattgasse=3795|Schönaugasse=3816|Schönaugürtel=3817|Schörgelgasse=3820|Schwarzenberggasse=3834|St.Petersburg Allee=4061|Steyrergasse=4002|Stremayrgasse=4043|Trattenweg=4231|Ulrich-Lichtenstein-Gasse=4381|Untere Bahnstraße=4424|Weinholdstraße=4648|Widowitzgasse=4714|Wielandgasse=4692|Winkelgasse=4701|Wittenbauerstraße=4702|Zimmerplatzgasse=4939|Augartenbrücke=5005|Augartensteg=5015|Bertha-von-Suttner-Friedensbrücke=5006|Eisenbahnbrücke=5007|Radetzkybrücke=5004

```

**EducationalInstitutions.csv:**  The *EducationalInstitutions* file contains data on the educational institutions located in Graz. The data points have the following structure:

* **Name:** The name of the institution.
  * Format: variable length *string*
* **Address:** The address of the institution including the street name and number.
  * Format: variable length *string*
* **PostalCode:** The postal code of the institution.
  * Format: 4-digit *numerical* value
* **PhoneNumber:** The phone number of the institution.
  * Format: a variable length *string* starting with '+43(0)316'
* **Category2:** ?
  * Format: variable lenght *string*
* **Category3:** ?
  * Format: variable length *string*

The following is an excerpt from the **EducationalInstitutions.csv** file, which is representative of the dataset's structure:

```
Name,Address,PostalCode,PhoneNumber,Category2,Category3
TU-Graz; Fakultät für Informatik; IICM; CGV,Inffeldgasse 16c,8010,+43(0)3168735613,Universitäten; Hoch- & Fachhochschulen,Technische Universität Graz
TU-Graz; Fakultät für Informatik; IWM,Inffeldgasse 21a,8010,+43(0)3168739251,Universitäten; Hoch- & Fachhochschulen,Technische Universität Graz
Uni-Graz; Institut der Fakultät für Sozial- u. Wirtschaftswissenschaften,Elisabethstraße 50b,8010,+43(0)3163807189,Universitäten; Hoch- & Fachhochschulen,Karl-Franzens-Universität Graz
Uni-Graz; Karl-Franzens-Universität,Attemsgasse 8,8010,+43(0)3163800,Universitäten; Hoch- & Fachhochschulen,Karl-Franzens-Universität Graz
FH Joanneum; Radiologietechnologie,Eggenberger Allee 13,8020,+43(0)31654536570,Universitäten; Hoch- & Fachhochschulen,Fachhochschule
KUG Institut 2 Klavier,Brandhofgasse 21/III,8010,+43(0)3163893020,Universitäten; Hoch- & Fachhochschulen,Kunstuniversität Graz
Uni-Graz; Institut für Soziologie; Frauen- und Geschlechterforschung,Strassoldogasse 10,8010,+43(0)3163807088,Universitäten; Hoch- & Fachhochschulen,Karl-Franzens-Universität Graz
TU-Graz; Institute der Fakultät für Technische Mathematik u. Technische Physik,Münzgrabenstraße 11,8010,+43(0)3168736475,Universitäten; Hoch- & Fachhochschulen,Technische Universität Graz
TU-Graz; Fakultät für Technische Chemie; Verfahrenstechnik u. Biotechnologie,Petersgasse 16,8010,+43(0)3168730,Universitäten; Hoch- & Fachhochschulen,Technische Universität Graz

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