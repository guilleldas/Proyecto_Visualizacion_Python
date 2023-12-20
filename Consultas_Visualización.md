## Consultas y Visualización

#### Creo este archivo con el objetivo de resumir el proyecto. Consultas, resultados y gráficos.


### Consulta 1:

```sql
SELECT confederation AS Confederacion, SUM(capacity) AS Capacidad
FROM estadios_tres_confederaciones 
GROUP BY confederation 
ORDER BY SUM(capacity) DES;
```

<details>
<summary>Ver resultado</summary>

|Confederacion|Capacidad|
|-------------|-------------|
|UEFA         |20,158,727   |
|CONCACAF     |9,001,050    |
|CONMEBOL     |4,223,002    |

</details>

<details>
<summary>Ver gráfico de barras</summary>

![grafico_barras_1](https://github.com/guilleldas/Proyecto_Visualizacion_Python/assets/145810000/33597153-c8dd-489c-b20f-a942040d198f)

</details>

<details>
<summary>Ver gráfico de torta</summary>

![pie_chart_1](https://github.com/guilleldas/Proyecto_Visualizacion_Python/assets/145810000/188f3de7-9ee5-4a22-a000-c13f6480eb76)

</details>

### Consulta 2:

```sql
SELECT country AS País, SUM(capacity) AS Capacidad 
FROM estadios_tres_confederaciones 
WHERE confederation = 'conmebol' 
GROUP BY country 
ORDER BY SUM(capacity) DESC;
```

<details>
<summary>Ver resultado</summary>

|País     |Capacidad|
|---------|---------|
|Brazil   |1,614,462|
|Argentina|746,576  |
|Chile    |401,683  |
|Venezuela|361,597  |
|Colombia |286,529  |
|Peru     |216,661  |
|Paraguay |187,000  |
|Ecuador  |180,754  |
|Uruguay  |137,740  |
|Bolivia  |90,000   |

</details>

<details>
<summary>Ver TreeMap</summary>

![treemap_1](https://github.com/guilleldas/Proyecto_Visualizacion_Python/assets/145810000/5fe6a881-5a48-41c6-a2ab-fafcd0d49bb7)

</details>

<details>
<summary>Ver gráfico de barras horizontal</summary>

![grafico_hbarras_1](https://github.com/guilleldas/Proyecto_Visualizacion_Python/assets/145810000/f3ff4b4c-d315-4213-a1e7-c5a71c9fe053)

</details>

### Consulta 3:

```sql
SELECT country AS País, 
SUM(capacity) AS Capacidad, 
AVG(population) AS Poblacion 
FROM estadios_tres_confederaciones 
GROUP BY country 
ORDER BY AVG(population) DESC;
```

<details>
<summary>Ver resultado</summary>

|País                    |Capacidad|Poblacion  |
|------------------------|---------|-----------|
|United States of America|7,150,367|325,719,178|
|Brazil                  |1,614,462|210,147,125|
|Russia                  |1,066,224|144,526,636|
|Mexico                  |1,022,560|133,140,936|
|Germany                 |2,453,107|82,800,000 |
|Turkey                  |849,098  |80,810,525 |
|France                  |1,427,886|67,348,000 |
|Italy                   |1,323,616|60,483,973 |
|England                 |2,383,457|55,619,400 |
|Colombia                |286,529  |49,996,445 |
|Spain                   |1,686,729|46,710,000 |
|Argentina               |746,576  |43,847,430 |
|Ukraine                 |588,981  |42,418,235 |
|Poland                  |842,187  |38,433,600 |
|Canada                  |496,496  |37,067,011 |
|Peru                    |216,661  |32,162,184 |
|Venezuela               |361,597  |31,568,179 |
|Romania                 |320,365  |19,638,000 |
|Kazakhstan              |108,858  |18,311,700 |
|Chile                   |401,683  |17,574,003 |
|Guatemala               |84,453   |17,263,239 |
|Netherlands             |531,275  |17,100,715 |
|Ecuador                 |180,754  |16,385,068 |
|Belgium                 |454,053  |11,420,163 |
|Bolivia                 |90,000   |11,248,864 |
|Greece                  |427,384  |10,768,477 |
|Czech Republic          |249,074  |10,610,947 |
|Portugal                |608,341  |10,291,027 |
|Sweden                  |463,883  |10,215,250 |
|Azerbaijan              |80,870   |9,898,100  |
|Hungary                 |215,363  |9,797,561  |
|Belarus                 |105,320  |9,491,800  |
|Honduras                |118,000  |9,112,867  |
|Israel                  |185,624  |8,958,730  |
|Austria                 |332,123  |8,857,960  |
|Switzerland             |254,609  |8,508,898  |
|Paraguay                |187,000  |7,052,984  |
|Bulgaria                |294,736  |7,050,034  |
|Serbia                  |213,286  |7,001,444  |
|Denmark                 |275,925  |5,806,015  |
|Finland                 |96,755   |5,520,535  |
|Slovakia                |181,173  |5,445,087  |
|Scotland                |502,034  |5,424,800  |
|Norway                  |222,666  |5,323,933  |
|Costa Rica              |80,174   |4,857,274  |
|Ireland                 |194,139  |4,857,000  |
|Croatia                 |188,931  |4,154,200  |
|Georgia                 |105,422  |3,718,200  |
|Bosnia-Herzegovina      |102,154  |3,511,372  |
|Uruguay                 |137,740  |3,444,006  |
|Moldova                 |46,531   |3,350,900  |
|Wales                   |167,206  |3,125,000  |
|Armenia                 |80,321   |2,924,816  |
|Albania                 |49,240   |2,876,591  |
|Lithuania               |28,040   |2,795,674  |
|Macedonia               |30,784   |2,103,721  |
|Slovenia                |73,659   |2,070,050  |
|Latvia                  |39,373   |1,925,800  |
|Northern Ireland        |48,090   |1,876,695  |
|Trinidad and Tobago     |49,000   |1,359,193  |
|Estonia                 |33,700   |1,319,133  |
|Cyprus                  |94,105   |1,170,125  |
|Luxemburg               |37,184   |602,005    |
|Malta                   |21,029   |475,700    |
|Iceland                 |40,077   |355,620    |
|Greenland               |2,500    |55,877     |
|Faroe Islands           |26,240   |51,095     |
|Gibraltar               |5,000    |32,194     |

</details>

<details>
<summary>Ver gráfico Scatter Plot</summary>

![scatterplot_1](https://github.com/guilleldas/Proyecto_Visualizacion_Python/assets/145810000/1d12b0fc-64d4-45e7-88fe-2a05a9f6b439)

</details>

### Consulta 4:

```sql
WITH RankingEstadios AS 
  (SELECT confederation, country, stadium, capacity, 
  ROW_NUMBER() OVER (PARTITION BY confederation ORDER BY capacity DESC) 
  AS row_num FROM estadios_tres_confederaciones) 
SELECT confederation AS Confederacion, country AS Pais, stadium AS Estadio, capacity AS Capacidad 
FROM RankingEstadios 
WHERE row_num <= 3
```

<details>
<summary>Ver resultado</summary>
  
|Confederacion|Pais                    |Estadio                       |Capacidad|
|-------------|------------------------|------------------------------|---------|
|CONCACAF     |United States of America|Bristol Motor Speedway        |153,000  |
|CONCACAF     |United States of America|Michigan Stadium              |107,601  |
|CONCACAF     |United States of America|Beaver Stadium                |106,572  |
|CONMEBOL     |Peru                    |Estadio Teodoro Lolo Fernández|80,093   |
|CONMEBOL     |Brazil                  |Maracanã                      |78,838   |
|CONMEBOL     |Brazil                  |Estádio Nacional              |72,888   |
|UEFA         |Spain                   |Camp Nou                      |99,354   |
|UEFA         |England                 |Wembley                       |90,652   |
|UEFA         |Spain                   |Estadio Santiago Bernabéu     |85,454   |

</details>

<details>
<summary>Ver gráfico de barras</summary>

![grafico_barras_2](https://github.com/guilleldas/Proyecto_Visualizacion_Python/assets/145810000/8923271e-8926-4f5e-b45f-0a7716f1f244)

</details>



  
