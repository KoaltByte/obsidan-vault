- ==Dataset de trabajo: Superstore Sales Dataset==
- ==Fuente: Kaggle==

# Análisis inicial exploratorio
-  Qué ves? Se ven 18 columnas con datos sobre la compra de productos de una tienda.
- Qué columnas hay? 
   1.  Row ID (Identificación de fila)
   2. Order ID (Identificación de orden)
   3. Order Date (fecha de orden)
   4. Ship Date (Fechad e envío)
   5. Ship Mode
   6. Customer ID
   7. Customer name
   8. Segment
   9. Country
   10. City
   11. State
   12. Postal code
   13. Region
   14. Product ID 
   15. Category
   16. Sub-Category
   17. Product Name
   18. Sales 
- Se puede ver algo extraño a simple vista? Las columnas de Ship Date y Order date no contiene datos como tal, las celdas contienen ######
# Limpieza de datos

> [!NOTE] Importante
> Cualquier modificación a los datos se debe de realizar en una copia de estos, nunca en los datos originales.

## 1. Verificación y eliminación de duplicados
### Por qué se hace?
Esto se realiza debido a que los datos duplicados "inflan" los resultados en un análisis, por ejemplo, una venta registrada dos veces es un error grave que puede llevar a decisiones incorrectas.

### Cómo se hace

1. Nos ubicamos dentro de cualquier celda dentro de la tabla de datos.
2. Nos dirigimos a la pestaña ==Datos (Data)== .
3. Buscamos el botón ==Eliminar duplicados== o ==Remove Duplicates==
4. La columna que se muestra a continuación contiene todas las columnas del data set de trabajo. Se seleccionan todas para eliminar las filas que son idénticas en todas las columnas. 
![[Captura de pantalla 2025-09-20 215510.png]]
## Corrección de formato de datos
### Por que se hace?
Se debe de hacer ya que puede que Excel no reconozca una fecha como fecha o un número como número, por lo cual no se podrían hacer cálculos, crear gráficos, hacer filtros, etc. de forma correcta. 
### Cómo se hace?
1. Se selecciona toda la columna o columnas a las que se desea dar formato.
2. En la pestaña ==Home== se da clic en ==Number== a continuación se selecciona el tipo de dato y su formato.

| Antes                                | Después |
| ------------------------------------ | ------- |
| ![[Pasted image 20250920215820.png]] | ![[Pasted image 20250920220235.png]]        |

## Manejo de datos faltantes o nulos
### Por qué se hace?
Los datos faltantes pueden hacer que el análisis sea erróneo, por lo cual se deben de ser identificados y tener claro que se debe de hacer con ellos. 

### Cómo se encuentran?
1. Se hace clic en cualquier celda de la tabla de datos.
2. Desde la pestaña ==Data== => ==Filter== o se usa el atajo `Ctrl + Shift + L`
3. Lo anterior hará que aparezcan flechas en el encabezado de cada columna 
4. clic en la fecha del encabezado => Ir al final de la lista => Si existen datos nulos habrá una opción llamada ==Blanks== => Se marca solo esa casilla para ver e identificas las filas con un dato nulo (en esa columna en especifico).

## Estandarización de datos
Se dice que los datos no estan estandarizados cuando se encuentrar datos escritos de manera diferente o con una ortografia incorrecta, esto hace que Excel los interprete como datos diferentes cuando en realidad son los mismo. Por ejemplo: en la columna Country se pueden encontrar datos "United States" y "United states"
### Cómo se hace?
1. Se hace uso de los filtros de cada columna, en la lista que se despliega podemos observar si existe alguna inconsistencia en los datos que nos pueda indicar que nos están estandarizados.
2. Una vez identificados se puede proceder a la estandarización. 





