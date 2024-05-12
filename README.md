# Matematikai programcsomagok beadandó
## Reál, nominális GDP és a regressziós egyenes
Az első Jupyter Notebookban beolvastuk a nominális gdp-t tartalmazó adatokat (forrás: Economic Statistics Branch of the United Nations Statistics Division) és a gdp-deflátorokat tartalmazó csv-t (forrás: World Bank). Ezek segítségével, egy kis tisztítás után megkaptuk az évenkénti inflációhoz igazított (reál) GDP-t. A plot_together függvény 4 különböző ábrát rajzol fel a bemeneti országhoz. Ezek közül a legfontosabb a reál gdp-re illesztett regressziós egyenes, ami közel áll a közgazdaságtanban használt növekedési trendre. Az r^2 értékek a legtöbb jelentős országnál 0.7 fölé esik, ami társadalomtudományoknál már megfelelő érték. Az r^2 érték akár az ország gazdasági stabilitására is jó mutatóként tud szolgálni.
![alt text](https://github.com/Geri1126/beadando/blob/main/kepek/Germany.png?raw=true)

## Clusterezés gdp/per capita alapján
A kezdeti, 210 ország, különböző gazdasági mutatóját 1970-2022-ig tartalmazó csv file-t (forrás: ) megtisztítottuk, a hiányzó értékeket tartalmazó sorokat tötöltük. Az eredmény 1990-2022-ig a gdp/per capita adatpont 149 országra. Ezekből az adatokból létrehoztunk egy az adott ország adatainak változását, és annak dinamikáját reprezentáló vektort minden országhoz. Ezeket a vektorokat a KMeans algoritmussal 30 clusterbe particionáltuk.

## Clusterezés oktatási adatok alapján
A kezdeti csv file (forrás: ) 210 országhoz tartozó, két típusú, az ottani oktatás fejlettségét mutató adatot tartalmazott. Ezt a csv file-t megtisztítottuk, hogy csak az előző clusterezésben szereplő országokat tartalmazza. Ebből az adathalmazból is létrehoztunk minden ország adataiból egy reprezentatív vektort, majd ezeket KMeans-zel 30 clusterre osztottuk. 

## A két clusterezés eredméynének összehasonlítása
A kanonikus, az országokat 3 fejlettségi csoportra osztó rendszerezést alapul véve, 3 clusterre bontottuk az országok vektorait. A 3-3 cluster közötti hasonlóságot egy contingency table-lel ábrázoltuk

## Térképek
A projekt utolsó állomása az eredmények térképre rajzolása. A térképen könnyen elkülöníthetők, észrevehetők lettek az országok, régiók közötti különbségek, határok és tendenciák. Más adatokkal is összevetettük a számolásainkat pl.: várható élettartam (forrás: WHO), elégedettség (forrás: Gallup World Poll). Az összevetés nem nyújt nagy meglepetést, viszont szemléletesen ábrázolja az összefüggéseket. Az eltérésekkel érdemes lehet külön foglalkozni, más adatok függvényében vizsgálódni.
![alt_text](https://github.com/Geri1126/beadando/blob/main/kepek/expectancy.png?raw=true)



