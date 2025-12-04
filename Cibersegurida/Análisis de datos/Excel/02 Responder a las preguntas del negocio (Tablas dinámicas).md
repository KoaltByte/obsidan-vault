No hay que olvidar que el objetivo de un análisis de datos es resolver las preguntas del negocio, para esto se puede utilizar una herramienta rápida y potente de Excel, las tablas dinámicas.

# Tablas dinámicas

> [!NOTE] Qué son?
> Una tabla dinámica es un resumen interactivo de los datos. Con un ejemplo sencillo podemos imaginar que los datos son miles de bloques de lego y una tabla dinámica nos permite agrupar, contar, sumar y organizar todos los ladrillos para así consumir lo que queramos, todo sin necesidad de utilizar formulas. 

## Qué responden?
- Cuanto?
- Quién?
- Cuál es el total por?
## Componentes clave 
- ==Filas== : Agrupación de datos de manera vertical, una fila corresponde a una característica de los datos, por ejemplo: Nombre, Región, edad, etc. 
- ==Columnas== : Agrupación de datos de forma horizontal. Una fila contiene los valores completos de todas las características de la tabla, por ejemplo: Juan Reyes, México. 37.
- ==Valores==: Son los datos unitarios que van en cada fila y es con lo que se pueden realizar cálculos. 
- ==Filtros==: Permite filtrar por una o más categorías. 

# Ejercicio práctico
Objetivo: Utilizando tablas dinámicas responder las siguientes preguntas:
1. Cuáles son nuestras ventas (Sales) totales por cada región? (Se necesita saber cuál es la región más fuerte en ventas).
2. Qué categoría (Category) de productos genera más ventas? Aquí los datos se ordenan de mayor a menor para identificar el producto "estrella".
3. Cómo se distribuyen las ventas por Segment de cliente? (Consumer, Corporate, Home Office).
4. Quiénes son los 10 mejores clientes? Se debe de mostrar un ranking de los 10 mejores clientes (Customer Name) con mayores ventas totales. Se crea primero la tabla dinámica se usa un filtro para mostrar el Top 10.

### Creación de la tabla dinámica 

Pestaña ==Insert== --> ==Tables== --> ==PivotTable== 

![[Pasted image 20250920233014.png]]![[Pasted image 20250920233319.png]]

### Aprender a utilizar las tablas dinámicas
Cada vez que se hace una tabla dinámica en realidad se esta construyendo una frase para hacerle una pregunta a los datos. Cada ==campo== de la tabla dinámica es una parte de esa frase.

#### Valores (Values) : Qué se quiere medir/calcular ?
Este es el corazón de la pregunta
- Pregunta clave: ¿Qué número quiero ver? ¿La suma de...? ¿El conteo de...? ¿El promedio de...? 
- Qué arrastras aquí: Siempre se debe arrastrar un campo numérico, ya que es lo que se desea que Excel calcule por nosotros.
==Ejemplo== 
Si se quieren ver las ventas por región 
#### Filas (Rows)


