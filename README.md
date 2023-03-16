## Estructuras de datos :eye_speech_bubble: :eye_speech_bubble:



Cuando comenzamos en el mundo de la programación, y venimos de otras vertientes profesionales, nos pueden faltar algunas temáticas básicas del mundo de la programación, una de ellas es la **"Estructura de Datos"**. Tener claro qué es la estructura de datos es súper importante ya que nos permite tener un mejor panorama al momento de enfrentarse a las problemáticas de cada proyecto, porque nos da una dimensión y/o perspectiva sobre **qué, cómo y de qué forma vamos a organizar, almacenar y manipular la información (datos)**. La estructura de datos es esencial para la gestión eficiente de grandes volúmenes de data, y son la puerta de entrada para esbozar algoritmos y desarrollar aplicaciones. 

Existen dos grandes aristas en la estructura de datos, de **dimensiones internas o externas**. **La primera manera de ver esto**, es pensar qué tipo de almacenamiento va a utilizar el computador, si la **memoria principal propia (RAM)** o si va a utilizar un dispositivo externo, ya sea base de datos, disco duro u otros. **La capacidad interna, suele ser más eficiente y rápida**, y está determinada por una cantidad limitada de almacenamiento. Mientras que la **estructura de datos externa**, es más lenta, pero tiene **mayor capacidad de almacenamiento**. Entonces, de acuerdo a la primera visión, una es más eficiente, pero de menor volumen de capacidad de almacenamiento de datos, y la otra es menos eficiente, pero de mayor volumen. 
		
**_La segunda manera de ver esto_**, es más "acotada" y de carácter instrumental, _es pensar que la estructura de datos tiene dos líneas generales, en las cuales existe un set de herramientas, que dependen de las necesidades del proyecto por el **tipo de flujo, eficiencia y volumen en el manejo de datos.**_ 


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

### Estructura de datos internos: Estructuras estáticas :mount_fuji:

**Estático:** Se refiere a que tienen **un tamaño fijo y predefinido** y se utilizan para almacenar datos que no cambian de tamaño durante la ejecución de un programa


- :owl:**Array (Arreglo):** Objetos similares a una lista cuyo prototipo proporciona métodos para efectuar operaciones de recorrido y de mutación. En este caso, presentamos un Array "unidimensional". 

<sub> Lenguaje Tipado </sub>

```c++
int numeros[5]; 
```
<sub> Lenguaje no tipado </sub>

```js
const numeros = [1, 2, 3, 4, 5];
```
- :owl:**Matriz:** Es similar a un arreglo, pero con dos o más dimensiones.

<sub> Lenguaje Tipado </sub>

```c++
int matriz[3][3];
```
<sub> Lenguaje no tipado </sub>

```js
const matriz = [[1, 2, 3], [4, 5, 6]];
```
- :owl:**Struct (Registro)**: Es una estructura de datos que permite agrupar varios elementos de diferentes tipos en una sola entidad.

<sub> Lenguaje Tipado </sub>

```c++
struct Persona {
  string nombre;
  int edad;
  float estatura;
};
```
<sub> Lenguaje no tipado </sub>

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

<sub> Lenguaje Tipado </sub>

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
<sub> Lenguaje no tipado</sub>

```js
const colores = {
  ROJO: "rojo",
  VERDE: "verde",
  AZUL: "azul"
};
```
- :owl:**Const (Constante)**: No es una estructura de datos propiamente dicha, pero es una forma de definir valores constantes que pueden ser utilizados en el programa. 

<sub> Lenguaje Tipado </sub>

```c++
const double velocidad_luz = 299792458;
```
<sub> Lenguaje no tipado </sub>

```js
const PI = 3.1416;
```

---

### Estructura de datos internos: Estructuras dinámicas :volcano:

**Dinámico**: Se refiere a que **puede variar de tamaño** durante la ejecución del programa y se utilizan para almacenar datos que pueden crecer o disminuir en tamaño. 



### Lineales: :slot_machine: 

**_Son aquellas en las que los datos están organizados en una secuencia lineal, es decir, cada elemento está conectado con su sucesor y predecesor (si lo tiene)._**

- :woman_technologist:**Listas enlazadas (linked lists):** una secuencia de elementos enlazados por punteros. Cada elemento (nodo) contiene un valor y un puntero al siguiente nodo.

_<sub>Recurso de profundización:<sub>_ <sub>https://medium.com/@dcortes.net/listas-enlazadas-en-javascript-18d991f1d6fd</sub>

- :woman_technologist:**Tuplas:** es una estructura de datos que permite almacenar un conjunto de elementos heterogéneos (es decir, de diferentes tipos de datos) en una única variable. A diferencia de los arreglos o listas, donde todos los elementos tienen el mismo tipo de datos, las tuplas pueden contener diferentes tipos de datos en cada una de sus posiciones.

<sub> Tupla Array </sub>

```js
const mi_tupla = ("Juan", 25, True, 1.75)
```
<sub> Tupla Object </sub>

```js
const miTupla = { nombre: 'Juan', edad: 25, casado: false };
```

_<sub>Recurso de profundización:<sub>_

<sub>https://ntgard.medium.com/tuples-in-javascript-cd33321e5277</sub>

<sub>https://medium.com/the-clever-dev/the-difference-between-a-tuple-and-an-array-in-typescript-e9fe9cc4a862</sub>


- :woman_technologist:**Colas (queues):** una secuencia en la que el primer elemento en ser agregado es el primero en ser eliminado (FIFO, first-in-first-out). Se puede implementar utilizando una lista enlazada o un arreglo.

_<sub>Recurso de profundización:<sub>_ <sub>https://medium.com/@dcortes.net/colas-en-javascript-queues-df85e43cd018</sub>

- :woman_technologist:**Pilas (stacks):** una secuencia en la que el último elemento en ser agregado es el primero en ser eliminado (LIFO, last-in-first-out). También se puede implementar utilizando una lista enlazada o un arreglo.

_<sub>Recurso de profundización:<sub>_ <sub>https://medium.com/@dcortes.net/pilas-en-javascript-stacks-e77fe6e4f7a5</sub>

### No lineales: :dna:

**_Son aquellas que no tienen una organización secuencial, y que por tanto, se pueden entender a veces dentro de lo que se denómina teoría de conjuntos y subconjuntos, que tiene que ver con la relación entre sus elementos_**

- :woman_technologist:**Árboles (trees):** una estructura jerárquica en la que cada elemento tiene un padre y cero o más hijos. Los árboles pueden tener un nodo raíz, nodos hoja (sin hijos) y nodos internos (con hijos).

_<sub>Recurso de profundización:<sub>_ <sub>https://medium.com/laboratoria-developers/%C3%A1rboles-trees-51783ba4ebe5</sub>

- :woman_technologist:**Grafos (graphs):** una estructura que consta de un conjunto de nodos (vértices) conectados por un conjunto de aristas (arcos). Los grafos pueden ser dirigidos o no dirigidos.

_<sub>Recurso de profundización:<sub>_ <sub>https://medium.com/laboratoria-developers/grafos-o-graphs-1e575c89f17</sub>

- :woman_technologist:**Tablas hash (hash tables):** una estructura que permite acceder a los datos a través de una clave en lugar de un índice. Se utiliza una función hash para convertir la clave en una posición en la tabla.

_<sub>Recurso de profundización:<sub>_ <sub>https://medium.com/@aliafsah1988/hash-tables-in-javascript-ff59b5f6d8d3</sub>

---

### Estructura de datos externos:

Las estructuras de datos externas son una clase especial de estructuras de datos que se utilizan para manejar **grandes cantidades de datos** que no caben completamente en la memoria principal de un sistema. Estas estructuras son esenciales en aplicaciones que procesan grandes conjuntos de datos, como bases de datos, sistemas de almacenamiento en disco y sistemas de archivos. El objetivo principal de las estructuras de datos externas es permitir un acceso eficiente a los datos almacenados en dispositivos externos, como discos duros, cintas magnéticas y memorias USB, lo que hace posible procesar conjuntos de datos que no caben completamente en la memoria principal del sistema.

_Estructuras generales_

- Base de datos
    - SQL
    - NoSQL
- JSON
- XML
- CSV 

### **Sobre las bases de datos":**

#### Qué es SQL?

SQL (Structured Query Language) es un lenguaje de programación utilizado para administrar y manipular bases de datos relacionales. Se utiliza para realizar una variedad de operaciones, como crear, actualizar y eliminar registros en una base de datos, así como para consultar y recuperar información específica de los datos almacenados en la base de datos.

**_Base de datos_**

- MySQL
- PostgreSQL
- Oracle
- Microsoft SQL Server
- SQLite

**Algunos conceptos importantes en SQL:**

Tables, Stored procedures, Indexes, Primary key, UUID, Foreign key, Join, Query, Transaction, View, Trigger, Aggregate function, Data type, Constraint, Normalization, Subquery, Cursor, Backup and restore, Replication, User-defined function (UDF) y ACID properties.

#### Qué es NoSQL?

NoSQL (Not Only SQL) se centra en tablas y relaciones predefinidas entre ellas, diseñadas para manejar datos no estructurados o semiestructurados, como documentos, gráficos o claves y valores. Son altamente escalables y se adaptan bien a entornos distribuidos y de alta velocidad


**_Base de datos_**

- MongoDB
- Cassandra
- CouchDB
- Redis

**Algunos conceptos importantes en SQL:**

Document database, Key-value store, Column-family database, Graph database, Sharding, Replication, CAP theorem, MapReduce, Consistency model, BSON, Query API, Indexing strategies, Distributed database, Eventual consistency, ACID vs. BASE y Document-oriented design


---
### Recursos para profundizar:

#### Estructura de datos

- https://www.geeksforgeeks.org/data-structures/
- https://www.programiz.com/dsa/data-structure-types
- https://www.javatpoint.com/data-structure-tutorial
- https://towardsdatascience.com/8-common-data-structures-every-programmer-must-know-171acf6a1a42
- https://www.simplilearn.com/tutorials/data-structure-tutorial/what-is-data-structure


#### Teoría de conjuntos

- http://www.matematicas.ciencias.uchile.cl/juaco/section-2.html