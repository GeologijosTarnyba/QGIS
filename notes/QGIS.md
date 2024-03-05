
### Problemos
##### Grafiniame sluoksnyje yra kitų tipų objektų (pvz. poligonų sluoksnyje yra ne poligonų)
###### Sprendimas
Layer properties -> Source -> Provide Feature Filter
```SQL
SDO_GEOMETRY.GET_GTYPE(OBJEKTAS) = 3
```
Čia `OBJEKTAS` - objekto stulpelis oracle db

Galimos reikšmes vietoj `3`:
|Reikšmė|Objekto tipas|
|---|---|
|1|Point|
|2|Line|
|3|Polygon|
|4|Collection|
|5|Multi-Point|
|6|Multi-Line|
|7|Multi-Polygon|
|1003|Polyhedral Surface|
|2001|TIN (Triangulated Irregular Network)|
|2002|Triangle Strip|
|3001|Compound Curve|
|3002|Curve Polygon|
