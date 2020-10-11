---
title: "Hvad koster de danske mønter?"
author: "Simon Grundt Straubinger"
date: 2020-05-21
links:
 - name: code to charts
   url: https://github.com/Straubinger/dataviz/tree/master/03_dkk_coins
   icon_pack: fab
   icon: github
#categories: ["R"]
#tags: ["R Markdown", "plot", "regression"]
---

En mønt har to værdier: den nominelle værdi, som er fastsat af den udstedende nationalbank, og metalværdien, som er bestemt af de internationale råstofpriser. Man kan tage den danske 1-krone som eksempel. Den vejer 3,6 gram og er fremstillet af kobbernikkel, som er en legering bestående af 75 pct. kobber og 25 pct. nikkel. Den gennemsnitlige kobberpris i april 2020 var ≈3 øre/gram, mens nikkelprisen var ≈8 øre/gram. Metalværdien for en dansk 1-krone i april 2020 var dermed ≈17 øre. Herunder fremgår vægten og metalsammensætningen for den seneste [danske møntserie](http://www.nationalbanken.dk/da/sedlerogmoenter/danske_moenter/Sider/default.aspx), som blev sat i cirkulation. I oktober 2008 blev 25-øren taget ud af cirkulation.

| Mønt          | Vægt | Legering     | Metaller                                  |
| ------------- |-----:| -------------|-------------------------------------------|
| 25-øre        | 2,8g | tinbronze    | 97 % kobber<br>0,5 % tin<br>2,5 % zink    |
| 50-øre        | 4,3g | tinbronze    | 97 % kobber<br>0,5 % tin<br>2,5 % zink    |
| 1-krone       | 3,6g | kobbernikkel | 75 % kobber<br>25 % nikkel                |
| 2-krone       | 5,9g | kobbernikkel | 75 % kobber<br>25 % nikkel                |
| 5-krone       | 9,2g | kobbernikkel | 92 % kobber<br>2,0 % nikkel<br>6,0 % aluminium|
| 10-krone      | 7,0g | kobbernikkel | 92 % kobber<br>2,0 % nikkel<br>6,0 % aluminium|
| 20-krone      | 9,3g | kobbernikkel | 92 % kobber<br>2,0 % nikkel<br>6,0 % aluminium|

Der er risiko for, at gamle cirkulerende mønter kan opnå en højere reel værdi end den nominelle værdi, som står påtrykt dem. Grunden til at metalværdien på længere sigt overstiger den nominelle værdi skyldes forskellige faktorer forbundet til udbud og efterspørgsel. Men der er særlig én faktor som gør, at de to værdier altid vil nærme sig hinanden, og det er inflation. Inflation udhuler penges købekraft (den nominelle værdi) og hæver prisen på håndgribelige aktiver (metalværdien). Er spændet mellem den nominelle og reelle værdi ikke stort nok fra starten, vil metalværdien overgå den nominelle værdi på sigt, eller også vil mønterne blive taget ud af cirkulation. Det var tilfældet med den [canadiske penny](https://edition.cnn.com/2012/03/30/business/canada-penny/), som kostede 60 pct. mere at producere end den pålydende værdi.

De danske mønters metalværdi fra januar 1990 til april 2020 fremgår af grafen herunder. Data er beregnet på baggrund af mønternes metalsammensætning samt de [månedlige råstofpriser](https://www.imf.org/en/Research/commodity-prices).

{{< figure src="plot_coins_value.png" title="👆 enlarge" lightbox="true" >}}

Metalværdierne følger hinanden ganske tæt gennem hele perioden, da alle mønterne hovedsageligt består af kobber. Det største udsving kan observeres op til og under finanskrisen 2007-2008. Her steg råstofpriserne eksplosivt, hvorefter de faldt lige så drastisk igen. Det var især gældende for nikkelpriserne, hvilket ses afspejlet i metalværdierne for 1-, 2- og 5-kronen. Mønten med den højeste metalværdi er 5-kronen, som da den peakede kostede næsten 1 krone at producere. Det skyldes, at den med 9,2 gram er den tungeste mønt efter 20-kronen samt består af 25 pct. nikkel, som indtil 2010 var det dyreste af metallerne nu kun overgået af tin. Nedenstående graf viser, hvor stor en procentdel mønternes metalværdi udgør af den nominelle værdi.

{{< figure src="plot_coins_pct.png" title="👆 enlarge" lightbox="true" >}}

Ikke overraskende findes der en negativ sammenhæng mellem den nominelle værdi, og hvor stor en andel metalværdien udgør af denne. På sit højeste udgjorde metalværdien af 20-kronen kun 2,5 pct. af den nominelle værdi, hvorimod metalværdien af 25-øren har udgjort hele 60 pct. af den nominelle værdi. Som det kan ses har 25-ørens metalværdi dog aldrig som ved den canadisk penny oversteget dens nominelle værdi.
