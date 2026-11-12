# Retail BI | ¿Qué productos siguen rezagados?

Proyecto de portafolio con **SQL (SQLite) y Power BI**. Analicé 52 semanas de compras de 811 productos para medir la caída de volumen, evaluar la recuperación y priorizar los productos con mayor brecha.

![Evolución del volumen durante los 13 períodos de cuatro semanas](evolucion.svg)

## Qué encontré

- El volumen cayó **16,4 %** entre las primeras 24 semanas y las siguientes 24, de 188.803 a 157.839 unidades. La diferencia fue de **30.964 unidades**.
- De los **543 productos** cuyo volumen cayó entre los períodos 6 y 8, **225** recuperaron el nivel del período 6, **184** se recuperaron parcialmente y **134** no se recuperaron. Al cierre del período 13, **318** seguían por debajo del nivel inicial.
- **P193, P43 y P135** encabezaron el ranking de brechas, con 66, 65 y 64 unidades pendientes, respectivamente. Son los primeros productos que revisaría.

## Cómo lo hice

1. Transformé las 52 columnas semanales en **42.172 filas producto-semana** y agrupé los datos en 13 períodos de cuatro semanas.
2. Comparé el volumen por producto entre P6, P8 y P13 para clasificar la recuperación. Ordené los productos rezagados por la diferencia entre P6 y P13.
3. Construí el informe en Power BI con los CSV exportados desde SQLite y comprobé que los resultados se mantuvieran al actualizar las tres tablas.

[Descargar el resumen visual completo (HTML)](retail-bi-dashboard.html?raw=true) · [Consultar los CSV del informe](datos/)

**Datos:** James Tan (2014), *Sales Transactions Weekly*, UCI Machine Learning Repository. Los CSV de este proyecto son agregaciones y cálculos derivados del conjunto original. [Fuente](https://doi.org/10.24432/C5XS4Q) · [Licencia CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
