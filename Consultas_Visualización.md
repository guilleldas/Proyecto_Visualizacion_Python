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

![grafico_barras_1](https://github.com/guilleldas/Proyecto_Visualizacion_Python/assets/145810000/48c927f7-7549-4d80-af0e-73a68bfd6b29)

</details>

<details>
<summary>Ver gráfico de torta</summary>

![pie_chart_1](https://github.com/guilleldas/Proyecto_Visualizacion_Python/assets/145810000/6d488691-3202-4770-ae5c-ab6d6d2633a0)

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
