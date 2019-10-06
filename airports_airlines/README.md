# Airports and airlines

## Overview 
This dataset was derived from [OpenFlights Dataset](https://github.com/jpatokal/openflights/tree/master/data) and contains denormalized CSV files for Airlines, Airports, Routes and Planes.


## Structure: 

**Airlines.csv:** The Airlines file contains the airlines information. It's detailed structure and examples look as follows.
```
#Name, IATA, ICAO, Country, Active
Austrian Airlines,OS,AUA,Austria,Y
Turkish Airlines,TH,THY,Turkey,Y
Lufthansa,MH,DLH,Germany,Y
```

**Airports.csv:** The Airports file contains the airports information. It's detailed structure and examples look as follows.
```
#Name, City, Country, IATA, ICAO, Latitude, Logtitude, Altitude, Timezone, DST
Goroka Airport,Goroka,Papua New Guinea,GKA,AYGA,-6.081689834590001,145.391998291,5282,10,U
Kaduna Airport,Kaduna,Nigeria,KAD,DNKA,10.696000099182129,7.320109844207764,2073,1,N
Brussels Airport,Brussels,Belgium,BRU,EBBR,50.901401519800004,4.48443984985,184,1,E
```

**Routes.csv:** The Routes file contains the flights information. It's detailed structure and examples look as follows.
```
#Airline, Departure, Arrival, Plane
NF,NUS,VLI,YN2;DHT;BNI
Y9,IFN,MRX,TU3
6R,MJZ,YKS,TU3;AN4
3R,ASF,DME,SU9
```

**Planes.csv:** The Planes file contains the planes information. It's detailed structure and examples look as follows.
```
#Name, IATA, ICAO
Aerospatiale SN.601 Corvette,NDC,S601
Airbus A380-800,388,A388
Antonov AN-12,ANF,AN12
Boeing 737-400,734,B734
```