#output #fecha #calendario #calculadora #ArtText #echo #cal #figlet #whoami #id #htop
# Salida estándar
---
El comando ==echo== muestra una salida en pantalla de una cadena de caracteres dada.
````bash
echo "Hello word"
````

# Hora y fecha
---
## Mostrar la fecha 
````bash
date
````
 Este comando muestra una salida como esta: `Mon Nov 25 01:48:53 PM CST 2025`

## Mostrar calendario
````bash
cal
````
Muestra los días del mes actual
   ``September 2025     
``Su Mo Tu We Th Fr Sa  
``   1  2  3  4  5  6  
 ``7  8  9 10 11 12 13  
``14 15 16 17 18 19 20  
``21 22 23 24 25 26 27  
``28 29 30 

````bash
cal 2025
````
Muestra el calendario completo del año especificado

# Terminal como calculadora 
---
Para realizar operaciones matemáticas sencillas en la terminal, se debe utiliza el comando ``expr`` seguido de la operación a realizar.
````bash
expr 2025 - 2020
expr 15 / 5
expr 3 * 9
````
El código anterior mostrara en salida por pantalla el resultado de la resta, división y multiplicación especificadas. 
# Arte con texto
---
El comando ``figlet`` se utiliza para transformar el texto, se puede utilizar solo o seguido del parámetro `` -f `` ``nombre de la fuente`` , este parámetro especifica el tipo de fuente que deseamos utilizar. 

````bash
figlet -f slant "I love"
````

![[Pasted image 20250929224801.png]]

# Mostrar el usuario actual
---
El comando ``whoami`` le "pregunta" a la computadora Quién soy? y por tanto responde con la salida del nombre de usuario. Este comando es útil cuando se trabaja con diferentes máquinas o cuando se utilizan diferentes cuentas. 
![[Pasted image 20250929225427.png]]

# Mostrar información de usuario y grupos
---
En Linux los usuarios se organizan en grupos y estos son los que determinan los permisos y derechos de acceso de cada usuario.  
Para saber a que grupo pertenece un usuario se utiliza el comando ``id`` .

![[Pasted image 20250929225808.png]]

- ``uid`` : Identificados número único de usuario.
- ``gid`` : Identificador de grupo principal.
- ``groups`` : Todos los grupos de los que se es miembro.

Se utiliza ``id`` solo cuando se desea ver la información de los grupos del usuario actual, cuando se desea ver la información de otro usuario o cuenta se utiliza seguido del nombre del usuario.

````bash
id root
````
# Monitoreo del sistema
---
La herramienta ``htop`` es un "panel de control" que da una vista en tiempo real de lo que sucede en la computadora. Esta herramienta se instala mediante un gestor de paquetes, un gestor de paquetes es como una tienda de aplicaciones y simplifica el proceso de instalación de software.

El gestor ``apt`` es muy utilizado en sistemas basados en Debian y antes de utilizarlo es importante actualizarlo, esto se realiza con el comando:

````bash
sudo apt update
````

Para la instalación de cualquier software o herramienta que se encuentre en el gestor apt se utiliza:

````bash
sudo apt install <nombre_del_software>
````

Para este caso se utilizará el comando ``sudo apt install htop`` al finalizar la instalación solo se ejecuta ``htop`` , lo que mostrara algo como lo siguiente: 
![[Pasted image 20250929230815.png]]

- En la parte superior se encuentra el uso del CPU, la memoria y el tiempo que la computadora ha estado encendida (uptime).
- En el centro esta la lista de todos los procesos o programas en ejecución.
- En la parte inferior están todas las opciones disponibles para interactuar con htop.