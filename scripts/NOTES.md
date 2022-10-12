## Repaso SQL

SQL es un lenguaje de programación para bases de datos. Su traducción literal seria lenguaje estructurado de consultas (structured Query Lenguaje)

SQL es un lenguaje insensible a mayúsculas y minúsculas, "select" == SELECT.

En sql las tablas tienen columnas que tendrán información de cierto **tipo**

Como buena practica los nombres de las tablas deben ser **plural**

llavde primaria: con valor único y no nulo.

CSV: Es un formato de archivo muy popular en los negocios. A partir de XLS se pueden exportar datos en CSV y también importar.'Valores separados por coma'.

SELECT <column>
FROM <table>:

La sentencia **WHERE** es para filtrar información

```sql 
SELECT <column>
FROM <table>
WHERE <column><condition>;
```

```sql
SELECT name, country, area
FROM cities
WHERE area < 1100
AND country = 'Japan'
```
## Ejemplo usando **OR**

``` sql
SELECT name, country, area
FROM cities 
WHERE area <1100
OR country = 'Japan';
```
### Ejemplo ordenando los resultados en forma ascendente

```sql 
SELECT name, country,area
FROM cities
ORDER BY area ASC;
```

# Ejemplo con WHERE, OR Y ORDER

``` sql 
SELECT name, country, area
FROM cities 
WHERE area < 1100
OR country = 'Japan'
ORDER BY area; 
```
## Ejemplo descendente

``` sql 
SELECT name, country, area
FROM cities 
WHERE area < 1100
OR country != 'Japan'
ORDER BY area DESC;
``` 
Nota: Distinto puede ser<> o así !=

## Campos O Columna calculados con AS (como)

```sql
SELECT name, population/area AS density
FROM cities 
ORDER BY density DESC;
```
## Contando elementos con COUNT

```sql
SELECT COUNT(name)
FROM cities 
WHERE country = 'India';
```

## Limitar los resultados con **Limit**

```sql
SELECT name, population/area AS density
FROM cities
ORDER BY density DESC
LIMIT 2; 
```
