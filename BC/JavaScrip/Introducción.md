> **Tipo de nota:** curso



# 🧠 Básicos de JS

**ID:** `202512032325`  
**Fecha:** 2025-12-03  
**Tipo:** curso

---

# 🎓 Nota de curso

**Curso:**  JS
**Módulo / Lección:**  1. Introducción a JS
**Profesor / Plataforma:** university.alchemy.com

## 🎯 Objetivo de aprendizaje
Comprender los conceptos básico sobre JavaScript

## 🧠 Conceptos clave
#Variables #Booleanos #Strings #Comentarios

```insta-toc
---
title:
  name: Tabla de contenido
  level: 1
  center: false
exclude: ""
style:
  listType: dash
omit: []
levels:
  min: 1
  max: 6
---

# Tabla de contenido

- 🧠 Básicos de JS
- 🎓 Nota de curso
    - 🎯 Objetivo de aprendizaje
    - 🧠 Conceptos clave
- Variables
    - Variables múltiples
- Booleanos
- Strings
    - Valores dentro de una cadena
- Comentarios
- Funciones
    - return
    - Argumentos
    - Parámetros
        - Caso 1: Argumentos y return
        - Caso 2: Argumentos y sin return
        - Caso 3:  Sin argumento y con return
        - Caso 4: sin argumentos y sin return
    - 🧪 Ejemplos / Código
    - 📝 Ejercicios / Tareas
    - ❓ Dudas pendientes
- 🧠 Conexiones con conocimiento previo
- 🔑 Palabras clave
- 🏷️ Etiquetas
- 🔗 Enlaces internos sugeridos
```

---
# Variables
Una variable es un valor que se almacena dentro de "una caja", el cual podemos utilizar dentro de nuestro programa. Por ejemplo:

```js
const a = 3
```

- `a`: Es la "caja" donde se almacena el valor de la variable.
- `3`: Es el valor que contiene la "caja".
- `const`: Es una palabra clave que se utiliza para declarar la variable y su valor, en este caso un valor constante.
> [!note] 
> Las variables se pueden declaran utilizando:
> - const: No permite cambiar el valor de la variable, es decir, es una variable constante
> - let: Hace que los valores sena mutables, es decir, que se puedan cambiar

## Variables múltiples
Un aspecto importante en JS es saber que cuando se ejecuta código se hace línea por línea, el `;` indica cuando una línea o sentencia termina. 
Lo anterior nos permite asignar a una variable como valor de otra:
````js
const a = 5;
const b = a;
````
Tanto a como b tienen el valor de 5.

# Booleanos
Un booleano es un valor lógico que solo puede tener dos valores `true` o `false` , estos valor indican si una condición es verdadera o falsa, si se cumple una condición o no y en función del valor que se tome, de ejecutan o no ciertos bloques de código.

El usuario ha iniciado sesión?  `false` indica que no.
```js 
const loggedIn = false; 
```
El usuario compro el artículo? `true` nos indica que si.
```js
const purchasedItem = true;
```

> [!attention] 
> En JS es importante tener en cuenta los siguiente al momento de declarar variables:
> - Se escriben utilizando lowerCamelCase (Por estética ya que JS no distingue entre minúsculas y mayúsculas).
> - Los caracteres validos son a-z, A-Z, 0-9, $ y _ .
> - El nombre de la variable siempre debe comenzar por una letra
> - En el caso de variables de entorno (Valores que se determinan antes de la ejecución del programa para que se ejecute de una forma determinada), se escriben con mayúsculas y guiones bajos.  const SERVER_KEY_VALUE = "abcdefghij";

# Strings
Las strings son cadenas o un conjunto de caracteres y en JS se pueden definir utilizando comillas simples o dobles, no hay diferencia entre usar una u otra.

```js
const myName = "Dan";
const anotherName = 'Cody';
```

## Valores dentro de una cadena
También se puede hacer uso de las comillas invertidas, pero estas se usan para envolver una cadena de texto cuando se quiere añadir el valor de una variable dentro de esta. 
```js
const helloMessage = `Hello ${anotherName}, my name es ${myName}!`;
```
La variable `helloMessage` utiliza comillas invertidas y cuando se ejecute se extraerán los valores de `anotherName` y `myName` y se colocarán dentro de la cadena.
Para que lo anterior funcione correctamente, el nombre de la variable debe tener la siguiente sintaxis:
==`${variable}`==

# Comentarios
Los comentarios son líneas en el código las cuales no se ejecutan, sirven para indicar a nosotros mismos o a otros programadores sobre ciertas decisiones o acciones dentro del código y hacen que el código sea más entendible.

==-->Comentario de una línea==
```js
// Este es el precio en dolares
const price = 42;
```
==-->Comentario en varias líneas==
```js
/*El precio de todos nuestros articulos
denominados en dolares*/
const price = 42;
```

# Funciones
Una función es código que se puede reutilizar, y una de sus características principales es que siempre devuelven una salida. 

```js
function getNumber(){
	return 4;
}
```
En este caso, siempre que se mande a llamar a la función `getNumber()` siempre devolverá 4.
Para mandar llamar (ejecutar) a una función se hace de la siguiente manera:
```js 
const num = getNumber();
```

## return
En una función, return realiza dos acciones:
1. Devuelve un valor desde la función.
2. Detiene la ejecución de la función, es decir, todo lo que se encuentre después no se ejecuta.
Cuando no se utiliza return, la función por defecto devuelve `undefined`.
## Argumentos
Los argumentos son valores que se le pasan a la función cuando se le manda a llamar y básicamente son información o datos que la función necesita para trabajar.
==Valores de los parámetros==
## Parámetros
Son las variables de la función que reciben a los argumentos. 
=="casillas vacías" que se llenan con los argumentos==

```js
function saludar(nombre){
    console.log("Hola" + nombre);
}

saludar("Carlos");
```
- `nombre`: Parámetro
- `Carlos`: Argumento

### Caso 1: Argumentos y return
La función recibe datos y devuelve un resultado 
```js
function sumar(a,b) {
    return a+b;
}

const resultado(4,5); //9
```
Es la forma más común en programación

### Caso 2: Argumentos y sin return
La función recibe datos pero no devuelve nada
```js
function sumar(a,b){
    console.log(a+b);
}

const resultado = sumar(3+6);
console.log(resultado); // undefined
```
- Recibe a y b, imprime la suma de a + b, como no tiene return devuelve undefined.
- Es útil para funciones que hacen acciones pero no cálculos. 

### Caso 3:  Sin argumento y con return
La función no recibe datos pero si devuelve un valor
```js
function obtenerNumero(){
    return 4;
}

const resultado = obtenerNumero(4); //4
```
- Útil para constantes, generadores, contadores, configuraciones, etc.

### Caso 4: sin argumentos y sin return
No recibe nada y no devuelve nada
```js
function saludar(){
    console.log("Hola");
}

const resultado = salaudar();
console.log(resultado); //undefined
```
- Útil para funciones que solo realizan efectos como imprimir, animar o actualizar pantalla. 

![[Untitled Diagram.svg]]


---


![[Untitled Diagram.png]]








## 🧪 Ejemplos / Código

```
(Añade aquí ejemplos o código)
```

## 📝 Ejercicios / Tareas

## ❓ Dudas pendientes



---

# 🧠 Conexiones con conocimiento previo

---

# 🔑 Palabras clave

---

# 🏷️ Etiquetas

#Zettelkasten

---

# 🔗 Enlaces internos sugeridos