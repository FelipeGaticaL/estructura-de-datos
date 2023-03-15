### Estructuras de datos :eye_speech_bubble: :eye_speech_bubble:


A veces, una de las grandes falencias de un developer, es no entender ciertas bases de la programación, una de ellas es la **"Estructura de Datos"**. Tener claro qué es la estructura de datos es súper importante ya que nos permite tener un mejor panorama al momento de enfrentarse a los problemáticas de cada proyecto, porque nos da una dimensión y/o perspectiva sobre **qué, cómo y de qué forma vamos a organizar, almacenar y manipular la información (datos)**. La estructura de datos es esencial para la gestión eficiente de grandes volúmenes de data, y son la puerta de entrada para esbozar algoritmos y desarrollar aplicaciones. 

Existen dos grandes aristas en la estructura de datos, de **dimensiones internas o externas**. **La primera manera de ver esto**, es pensar qué tipo de almacenamiento va a utilizar el computador, si la **memoria principal propia (RAM)** o si va a utilizar un dispositivo externo, ya sea base de datos, disco duro u otros. **La capacidad interna, suele ser más eficiente y rápida**, y está determinada por una cantidad limitada de almacenamiento. Mientras que la **estructura de datos externa**, es más lenta, pero tiene **mayor capacidad de almacenamiento**. Entonces, de acuerdo a la primera visión, una es más eficiente pero de menor volumen de capacidad de almacenamiento de datos, y la otra es menos eficiente pero de mayor volumen. 
		
**_La segunda manera de ver esto_**, _es pensar que la estructura de datos tiene dos líneas generales, en las cuales existe un set de herramientas, que dependen de las necesidades del proyecto por el **tipo de flujo, eficiencia y volumen en el manejo de datos.**_ 


**Diagrama de Estructura de Datos**

![Image text](https://github.com/FelipeGaticaL/estructura-de-datos/blob/main/assets/EstructuraDatosDiagramBlack.png)

---
#### ¿Por qué es importante? :collision::collision:
	
Porque nos permite definir **herramientas y métodos** tanto a nivel hardware como a nivel de lenguaje/software para solucionar y generar desarrollo de acuerdo a las necesidades propias del proyecto.

:dizzy: Por ejemplo: 

- ¿El proyecto por su tipo de flujo de datos, bastará con una estructura JSON o será necesario generar una persistencia en una Base de Datos?
- ¿El volumen de datos, tendrá mejor eficiencia y eficacia a través de métodos/funciones lineales o no lineales?
- ¿El retorno de una petición a una API, será mejor trabajarla con X algoritmo para trabajar el flujo de información?

Teniendo claro qué estructuras de datos hay, y cuáles son las más comunes, posiblemente nos podremos hacernos una idea de cuál serán los problemas que nos vamos a enfrentar, y con ello, manejar un stack tecnológico que nos ayude a poder hacerle frente de mejor manera. 

---
### Estructura de datos internos:
	
Existen de dos tipos, **estática y dinámica**. La primera es un elemento que se sabe que su tamaño será fijo, y tendrá asignada una memoria durante la ejecución del programa, por su características, suelen ser las más eficientes. La segunda, si bien parte con una memoria asignada, durante la ejecución, está variará y no se sabe a priori cuánto será el total utilizado. 
		
**Aterrizando esto a lenguaje:** :robot:
				
- Estático sería: **variable = [a,b,c,d]** -> Ya existe declarada por tanto se sabe la memoria a utilizar.
- Dinámico sería: **new variable = [e,f,g,h]** -> Tiene asignado una memoria inicial, pero, digamos que debemos iterar más elementos con un **bucle for y push (js)**. Bueno, ahora dependerá del flujo y cantidad de datos, cuánta memoria final abarcará al terminar el proceso.


**Ejemplo de iteración dinámica**

```js

const numeros = []; // Asignamiento de memoria

// Ciclo iterativo dinámico
for (let i = 0; i < 10; i++) {
  if (i % 2 === 0) {
    numeros.push(i);
  }
}

console.log(numeros); /
// Salida: [0, 2, 4, 6, 8]

```

:monocle_face: **Yendo más allá:** :monocle_face:
				
En **lenguajes no tipados**, como javascript, no solemos darle importancia al tipo de datos. Pero al comienzo de la programación, cuando el software tenía menor potencia de procesamiento, el tipo de dato nos decía cuántos bytes de memoria iba a utilizar, lo que tenía un impacto brutal en computadoras de antaño. 
				
**Tabla ejemplo**
				
| Tipo de datos	| Tamaño en bytes |
| ------------- | ------------- |
| char   | 1 |
| short  | 2 |
| int	 | 4 |
| long	 | 8 |
| float	 | 4 | 
| double | 8 | 
| bool   | 1 |
				
				
Este **problema del tipado**, hoy en día, cuando una App es pequeña, no tiene mayor incidencia en la memoria. Pero sí tiene **incidencia, al detectar errores en el código y facilitar el mantenimiento**. En el caso de Javascript, un lenguaje que busca solucionar esto es **_TypeScript_**, el cual introduce "sintaxis de tipado estático" que permite definir tipos de datos para las variables. Y con esto, lo que quiero decir, es que :eyes::eyes: **entender la estructura de los datos, no sólo tiene que ver con cuestiones de eficiencia y almacenamiento, sino, que entender que los tipos de datos, en cada uno de los flujos, también tiene incidencia al momento de producirse errores o problemas de mantenimiento de la App** :eyes::eyes:. 

<a href="https://www.typescriptlang.org/" target="blank"><img align="center" src="https://github.com/devicons/devicon/blob/master/icons/typescript/typescript-plain.svg" alt="" height="40" width="40" /></a>


---

### Estructura de datos internos:
#### Estructuras estáticas

- :owl:**Array (Arreglo):** Objetos similares a una lista cuyo prototipo proporciona métodos para efectuar operaciones de recorrido y de mutación. 

**Lenguaje Tipado**
```c++
int numeros[5]; 
```
**Lenguaje No Tipado**
```js
const numeros = [1, 2, 3, 4, 5];
```
- :owl:**Matriz:** Es similar a un arreglo, pero con dos o más dimensiones.

**Lenguaje Tipado**
```c++
int matriz[3][3];
```
**Lenguaje No Tipado**
```js
const matriz = [[1, 2, 3], [4, 5, 6]];
```
- :owl:**Struct (Registro)**: Es una estructura de datos que permite agrupar varios elementos de diferentes tipos en una sola entidad.

**Lenguaje Tipado**
```c++
struct Persona {
  string nombre;
  int edad;
  float estatura;
};
```
**Lenguaje No Tipado**
```js
const persona = {
  nombre: "Juan",
  edad: 30,
  direccion: {
    calle: "Av. Principal",
    numero: 123,
    ciudad: "Ciudad de México"
  }
};
```
- :owl:**Enum (Enumaeración)**:  Es una estructura de datos que permite definir un conjunto de constantes enteras con nombres simbólicos. 

**Lenguaje Tipado**
```c++
enum DiaSemana {
  Lunes,
  Martes,
  Miercoles,
  Jueves,
  Viernes,
  Sabado,
  Domingo
};
```
**Lenguaje No Tipado**
```js
const colores = {
  ROJO: "rojo",
  VERDE: "verde",
  AZUL: "azul"
};
```
- :owl:**Const (Constante)**: No es una estructura de datos propiamente dicha, pero es una forma de definir valores constantes que pueden ser utilizados en el programa. 

**Lenguaje Tipado**
```c++
const double velocidad_luz = 299792458;
```
**Lenguaje No Tipado**
```js
const PI = 3.1416;
```

#### Estructuras dinámicas


**Lineales**

- Listas enlazadas (linked lists): una secuencia de elementos enlazados por punteros. Cada elemento (nodo) contiene un valor y un puntero al siguiente nodo.

- Colas (queues): una secuencia en la que el primer elemento en ser agregado es el primero en ser eliminado (FIFO, first-in-first-out). Se puede implementar utilizando una lista enlazada o un arreglo.

- Pilas (stacks): una secuencia en la que el último elemento en ser agregado es el primero en ser eliminado (LIFO, last-in-first-out). También se puede implementar utilizando una lista enlazada o un arreglo.

**No lineales**

- Árboles (trees): una estructura jerárquica en la que cada elemento tiene un padre y cero o más hijos. Los árboles pueden tener un nodo raíz, nodos hoja (sin hijos) y nodos internos (con hijos).

- Grafos (graphs): una estructura que consta de un conjunto de nodos (vértices) conectados por un conjunto de aristas (arcos). Los grafos pueden ser dirigidos o no dirigidos.

- Tablas hash (hash tables): una estructura que permite acceder a los datos a través de una clave en lugar de un índice. Se utiliza una función hash para convertir la clave en una posición en la tabla.

---

#### Estructura de datos externos:




---
### Recursos para profundizar:

- https://www.geeksforgeeks.org/data-structures/
- https://www.programiz.com/dsa/data-structure-types
- https://www.javatpoint.com/data-structure-tutorial
- https://towardsdatascience.com/8-common-data-structures-every-programmer-must-know-171acf6a1a42
- https://www.simplilearn.com/tutorials/data-structure-tutorial/what-is-data-structure