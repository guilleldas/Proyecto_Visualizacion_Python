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

### Consulta 3:

```sql
SELECT country AS País, 
SUM(capacity) AS Capacidad, 
AVG(population) AS Poblacion 
FROM estadios_tres_confederaciones 
GROUP BY country 
ORDER BY AVG(population) DESC;
```


