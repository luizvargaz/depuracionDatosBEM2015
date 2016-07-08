---
title: "Untitled"
author: "Luis Vargas. CIMMYT, l.vargas@hotmail.com"
date: "July 8, 2016"
output: html_document
---

# Paso 1. Obtener los Outliers del precio de venta

### Obtener la base de datos en Crudo del sistema BEM 
Enlace para la de descarga [aqui](https://github.com/luizvargaz/depuracionDatosBEM2015/blob/master/EXPORTAR%20oi%202015%20com.xlsx)

### En la hoja **24_rendimiento** agregar las siguientes columnas: 
* Rendimiento (unidad/ha)     =IF(T2="",S2,T2)	
* Tipo produccion     =IF(IFNA(VLOOKUP(B2,'20_riegos_Descripcion'!B:B,1,FALSE), "Temporal")="Temporal", "Temporal", "Riego")
* ID de la parcela (clave foránea)	   =VLOOKUP(A2,'01_caracteristicas Bitácora'!A:I,9,FALSE)
* Estado    =VLOOKUP(Z2,'04_parcelas'!A:I,7,FALSE)	
* Año     =VLOOKUP(A2,'01_caracteristicas Bitácora'!A:D,4,FALSE)	
* Ciclo     =VLOOKUP(A2,'01_caracteristicas Bitácora'!A:F,6,FALSE)


