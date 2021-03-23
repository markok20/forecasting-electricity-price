# electricity-price-forecast

Kuinka tehdä täydellinen ennuste sähkön pörssihinnan kehityksestä?

Miten sähköpörssissä muodostuva sähkön hinta kehittyy seuraavien viikkojen tai kuukausien aikana? Onko hinnassa selvä trendi tai kausittaisuus? Minä kuukausina hinta nousee selkeästi keskimääräistä korkeammaksi ja milloin laskee?

Käytettävissä oli tammikuusta 2013 alkaen data, joka sisälsi noin 3 000 riviä spot-hintatietoa. Data ulottui aina 21. maaliskuuhun 2021 saakka. Spot-hinta määräytyy Pohjoismaisessa Nord Pool-sähköpörssissä, jossa  muodostetaan sähkön hinta jokaiselle vuorokauden tunnille. Suomen alueelle muodostuu oma Spot-hinta. Kuvataan hinnan kehitystä tammikuusta 2013 alkaen laskettuna siten, että kullekin kuukaudelle on määritelty keskiarvo.

Miten voidaan luoda täydellinen ennuste sähkön pörssihinnan kehitykselle? Perinteisesti ennustemallina on käytetty liukuvaa keskiarvoa, joka on yksinkertaisin malli ennustaa kehitystä. Liukuvan keskiarvon menetelmässä tulevan ajanhetken kysynnän ennuste on keskiarvo menneiden ajanhetkien kysynnästä. Kuvataan liukuvan keskiarvohinnan kehitystä.

Itse käytän ratkaisuna eksponentiaalisen tasoituksen (liukuva keskiarvo painotettuna tuoreimpiin ajankohtiin) mallia, joka reagoi herkästi muutoksiin ja helposti päivitettävissä. Kyseessä on yksi suosituimmista kysynnän ennustamisen malleista. Malliin voidaan lisätä komponentteja, jotka huomioivat trendin ja kausivaihtelun. Kysyntään vaikuttavia tekijöitä ovat kysynnän perustason lisäksi trendi-, kausi-, sykli- ja markkinointitekijät sekä ennustamaton vaihtelu.

Tarkastellaan seuraavaksi trendin ja kausittaisuuden kehitystä. Trendi on aluksi hieman laskeva, mutta nouseva vuodesta 2016-2019, kunnes siirtyy uudestaan laskevaksi. Kausittaisuudesta nähdään se, että hinta nouse vuodenvaihteessa, mutta kääntyy kesäksi laskuun. Kesän jälkeen hintakäyrä on nouseva vuodenvaihteeseen saakka.
Tehdään datan perusteella ennustus, miten hinta kehittyy seuraavien 12 viikon aikana maaliskuusta puolesta välistä alkaen.

Suomen alueen Spot-hinta määräytyy sähköpörssissä seuraavan vuorokauden jokaiselle tunnille vuorokautta edeltävänä päivänä viimeistään kello 12:30 (CET). Hinta muodostuu sähköpörssiin syötettyjen osto- ja myyntitarjousten leikkauspisteessä. 

Spot-hinta on niin kutsutusti raaka markkinahinta sähköenergialle kullekin alueelle, eikä se ota huomioon sähkönmyyjän toimintakustannuksia, kuten alkuperäsertifikaatteja, toimitusmaksua, profiilikustannuksia tai esimerkiksi sähkönmyyjän laskutusta tai asiakaspalvelua. Nord Poolissa sähkön hintojen yksikkönä käytetään euroa per megawattitunti, eivätkä pörssin listalla näkyvät hinnat sisällä arvonlisäveroa. 
