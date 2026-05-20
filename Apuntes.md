# Cuaderno Programacion 

## Clase 1

java --version:nos ayuda a comprobar la version de java.
Ctrl + j:levanto la consola.
mrdir:crea carpeta o directorio.(prj)abreviacion de el proyecto
exit:salir de terminal.
ls -a:muestra todos los archivos.

```java
public class Hi {
    public static void main(String[] args) {
        System.out.println("Hola Mundo");
        System.out.println("Andi");
    }
}
```
```java
public class Sumar {
    public static void main(String[] args) {
        int a = 5ls;
        int b = 10;
        int resultado = a + b;
        System.out.println("La suma de " + a + " y " + b + " es: " + resultado);
    }
}
```


## Clase 2:GITHUB

- pwd:mostrarme la direccion en donde estoy.
- ls:nos muestra que hay en el directorio actual.
- cd ,cd ..:nos permite movernos entre carpetas.
- mv :nos permite cambiar el nombre de el archivo o - directorio.
- code: nos permite abrir un proyecto o archivo.
- rm :noa permite borrar un archivo.
- rm -r:borra carpetas o directorios.
- history:nos permite ver los comandos que usamos.
- Crtl + X: eliminamos o borramos lineas de codigo o - texto.
- .gitignore:Ignora archivos en expecifico para que solo se suba los que queremos que se suba.
- cat:nos muestra que hay en el archivo.
  
## Comandos de Git

### Comandos locales 

- git init:crea un repositorio en la carpeta local,nos guarda el historial de el proyecto basicamente(Se ejecuta una vez por proyecto).
- git status:nos dice el estado de las cosas.
- git add: nos ayuda a guardar cambios ,basicamente los pasa - al area de preparacion,basicamente le dice al git estos son los cambios que quiero guardar,lo que hace es (prepara para guardar).
- git commit -m "MENSAJE QUE QUIERO DEJAR" -a:guarda los - cambios de forma permanente el el repositorio.

### Comandos para la nube 

- git push:envia lo que hice a la nube a mi repositorio de la nube.
- git pull:traeme guardado de mi repositorio en la nube a mi pc.

## Clase 3

- Ctrl+p:nos permite analizar los archivos que queremos usar ya sean repositorios o archivos.
- Ctrl+b:nos deja solo el esenario de trabajo.

terminal de el git personalizado



### Ramas
Nos sirve para trabajar en distintas versiones de mi proyecto sin afectar el proyecto principal (main).
 git branch:nos sirve tanto para crear como tambien para visualizar las ramas que tenemos.
 git switch:nos sirve para transladarnos de ramas una a la otra.
 git merch:nos sirve para unir la rama que estamos trabajando a la rama principal (main).
 ## Clase 4

Los archivos de java siempre su nombre empieza con mayuscula.
Al momento de hacer el git init nos crea una carpeta oculta en el proyecto actual.
git config --global user.name:nos sirve para ver que ususario esta registrado en el git bash.
git config --global user.email:nos da el correo que esta registrado.

## Clase 5

En la PRO,orientada a objetos se organiza el codigo usando objetos como si fueran objetos de la vida real.
git reset:borra el archivo de el area staging(area de preparacion)pero sin modificar los cambios que teniamos.

## Clase 

 * **Tipos de datos y Variables**: Se analiza la diferencia entre tipos primitivos y tipos por referencia, utilizando ejemplos como int, char, float, String e Integer. Se explican conceptos como la conversión de tipos (cast, implícita/explícita) y cómo se comportan las variables en memoria.
 * **Fundamentos de Java**: Se muestra material de apoyo sobre cómo funciona Java (compilación a bytecode, JVM, plataforma), diferencias entre programación estructurada y orientada a objetos, y la importancia de la práctica constante.
 * **Control de flujo y Sintaxis básica**: Se mencionan estructuras condicionales (if, else, switch case) y el uso de System.out.println o Scanner.
 * **Métodos**: Se explica cómo definir y estructurar métodos, incluyendo el uso de parámetros y valores de retorno, bajo el principio de "No repetirse" (DRY). Se ejemplifica la creación de un método como saltar().
 * **Estructura de Clases**: Se ilustra la relación entre atributos, métodos y la estructura general de una clase en Java.


## Clase 

### Manipulación de Cadenas y la Eficiencia de Memoria

El hecho de que tu IDE te sugiera usar StringBuilder en lugar de concatenación directa (+) no es un capricho, es una cuestión de **gestión de memoria en el Heap**.
 * **Inmutabilidad de String:** En Java, los objetos String son inmutables. Cada vez que haces cadena += "a", Java no está modificando el objeto original; está creando un objeto nuevo en memoria, copiando el contenido anterior y añadiendo el nuevo carácter. En un bucle, esto genera una cantidad masiva de objetos "basura" que el Garbage Collector debe limpiar.
 * **StringBuilder (Mutable):** Esta clase utiliza un buffer interno (un arreglo de caracteres redimensionable). Cuando agregas datos, simplemente se modifica el arreglo interno. Es órdenes de magnitud más rápido y eficiente para operaciones repetitivas (como invertir una cadena o construir estructuras complejas).

### Estructuras de Control y Lógica de Algoritmos

Los retos que mencionas (Series, Fibonacci, Matrices) son la base del **Pensamiento Computacional**.
 * **Series Numéricas:** El desafío aquí no es solo obtener el resultado, sino la **abstracción del patrón**. Al resolver un triángulo de números o Fibonacci, estás practicando el diseño de algoritmos con complejidad temporal controlada (preferiblemente O(n) en lugar de recursividad simple sin memoización, que sería exponencial).
 * **Manipulación de Matrices:** Al trabajar con matrices (coordenadas i, j), el concepto clave es el **mapeo de índices**. Muchos errores en ingeniería ocurren al intentar acceder a posiciones fuera de los límites del arreglo (ArrayIndexOutOfBoundsException). La clave es dominar las estructuras anidadas y cómo la lógica de los bucles afecta la visualización de los datos. 

### Diseño de Software: Arquitectura y Comunicación entre Clases

La discusión sobre la interacción entre Controlador, Serie, Figura y CadenaCaracter es, en esencia, **Programación Orientada a Objetos (POO)** aplicada a una arquitectura en capas.
 * **Principio de Responsabilidad Única (SRP):** Cada clase debe tener una única razón para cambiar.
   * CadenaCaracter debe encargarse únicamente de la lógica de procesamiento de texto.
   * Serie debe encargarse de la generación matemática.
   * Controlador actúa como el **Orquestador**: no debe contener la lógica de negocio, sino decidir cuándo llamar a los servicios de las otras clases para cumplir con una petición del usuario.
 * **Acoplamiento y Cohesión:** El objetivo de tu diagrama en *draw.io* es reducir el **acoplamiento** (que tus clases no dependan excesivamente de los detalles internos de las otras) y aumentar la **cohesión** (que los métodos dentro de una clase estén fuertemente relacionados entre sí).
### Ciclo de Vida del Software: Debugging y Refactorización
El proceso que viviste de intentar ejecutar, encontrar errores y corregir, es el corazón del **Desarrollo Iterativo**.
 * **Compilación vs. Tiempo de Ejecución:** Los errores que corregiste en Controlador.java suelen ser problemas de **tipado** o **visibilidad** (acceso a métodos public vs private). En sistemas más grandes, se usan *Unit Tests* (como JUnit) para asegurar que el método showStringReverse funcione independientemente del controlador, permitiéndote detectar el error antes de integrar todo el sistema.
 * **Debugging:** La depuración no es solo "quitar errores", es **observabilidad**. Aprender a usar los puntos de interrupción (*breakpoints*) te permite observar el estado de las variables en la pila de ejecución (*call stack*) y entender exactamente en qué línea la lógica deja de ser lo que esperabas.

## Clase 

​Cadena de caracteres: Manipulación de strings (contar vocales, eliminar letras, invertir frases, usar mayúsculas/minúsculas, anagramas).
​Arrays y Matrices: Ejercicios más complejos sobre manejo de estructuras de datos, coordenadas y creación de matrices con nombres o caracteres.
​Desarrollo en Java:
​El equipo trabaja activamente en una clase llamada Cadena (dentro del paquete cadenaCaracter).
​Se enfocan en implementar el método showStringReverse, cuyo propósito es invertir una cadena de texto.
​Durante la codificación, enfrentan advertencias del IDE (sugerencias para usar StringBuilder en lugar de concatenación directa en bucles) y errores de sintaxis al intentar devolver valores o definir métodos dentro de la clase.
​Diagramación y Estructura:
​Utilizan una herramienta de diagramación (posiblemente draw.io dentro de VS Code) para visualizar la lógica de sus clases, conexiones entre objetos y el flujo de los métodos.
​Se observa una discusión sobre cómo estructurar la lógica entre las clases Controlador, Serie, Figura y CadenaCaracter.
​Depuración (Debugging):
​Hacia el final de la grabación, realizan intentos de ejecución y depuración del código, encontrando errores de compilación que intentan corregir en tiempo real en el Controlador.java al llamar a los métodos.

## Clase

## Modelado y Lógica del Autómata. 
 * ** Cuál es su objetivo? :** Se diseña y analiza el comportamiento de una máquina expendedora que acepta monedas de 5, 10 y 25 centavos para entregar un producto (chicle por 10 centavos, pan por 25 centavos).
 * **Estados del sistema (q_0 a q_5):** Representan el dinero acumulado en la máquina:
   * q_0: 0 centavos.
   * q_1: 5 centavos.
   * q_2: 10 centavos (**entrega chicle**).
   * q_3: 15 centavos.
   * q_4: 20 centavos.
   * q_5: 25 centavos (**entrega pan**).
 * **Pruebas de caminos:** Se evalúan diferentes secuencias de monedas ingresadas para ver si el sistema responde correctamente (por ejemplo, si metes 5, luego 10 y luego 5, el sistema calcula el estado final y determina qué producto o vuelto corresponde).
## Creación de la Matriz de Transición
 * **Estructura:** Se construye una tabla en la herramienta de diagramación para representar la lógica del autómata en código o datos estructurados.
 * **Filas y Columnas:** Las filas representan los estados actuales (q_0, q_1, \dots) y las columnas los estímulos o entradas (monedas de 5, 10, 25, y la acción de presionar Enter/Espacio).
 * **Llenado de datos:** Se completa celda por celda definiendo a qué estado salta la máquina. Por ejemplo:
   * Estando en q_0 (0 centavos), si ingresas una moneda de 5, pasas al estado 1 (equivalente a q_1).
   * Estando en q_1 (5 centavos), si ingresas otra de 5, pasas al estado 2 (q_2).
   * Si se intenta una acción no válida (como pedir producto sin saldo), se marca como error.
 * **Traducción formal:** Al lado de la tabla, se escriben las funciones de transición equivalentes en formato de matriz matemática (ej. matriz[0][0] -> 1), preparando la lógica para su posterior implementación en programación. 

## Clase

### Resumen del Video
**Programación Orientada a Objetos (P.O.O.) en Java**.
A lo largo de la clase, el instructor utiliza diapositivas de PowerPoint y el entorno de desarrollo **Visual Studio Code** para explicar de manera práctica y teórica los fundamentos del lenguaje, incluyendo:
 1. **Tipos de datos primitivos y de referencia.**
 2. **Estructura y sintaxis de variables** (reglas de nomenclatura y buenas prácticas).
 3. **Conversión de tipos de datos** (*Casting* y métodos de envoltura).
 4. **Operadores aritméticos, lógicos y relacionales.**
 5. **Entrada de datos** mediante el uso de la clase Scanner.
 6. **Uso de la clase String** y sus métodos principales.
 7. **Estructuras de control y datos** (menciones a *Arrays*, *Stacks*, *Queues*, etc.).
### Ampliación de la Información Más Importante
A continuación, se profundiza en los pilares conceptuales clave explicados en la sesión:
#### 1. Tipos de Datos en Java (P.O.O.)
Java es un lenguaje fuertemente tipado, lo que significa que cada variable debe declararse con un tipo de dato específico. Se dividen en dos grandes grupos:
 * **Tipos Primitivos:** Son tipos de datos básicos incorporados en el lenguaje que almacenan valores directamente.
   * **Enteros:** byte (1 byte, de -128 a 127), short (2 bytes), int (4 bytes, el estándar para enteros) y long (8 bytes, para números muy grandes).
   * **Punto Flotante (Decimales):** float (4 bytes, precisión simple, requiere sufijo 'f') y double (8 bytes, precisión doble, estándar para decimales).
   * **Caracteres:** char (2 bytes, almacena un único carácter Unicode entre comillas simples, ej. 'A').
   * **Lógico:** boolean (almacena únicamente true o false).
 * **Tipos de Referencia (No primitivos):** No almacenan el valor en sí, sino una referencia (dirección de memoria) al objeto. Ejemplos de esto son las clases, las interfaces, los Arrays y la clase String.
#### 2. Reglas para Nombrar Variables
El instructor enfatiza las convenciones de nomenclatura (buenas prácticas) para mantener el código limpio y legible:
 * **Camel Case:** Los nombres de las variables deben comenzar con una letra minúscula y, si contienen múltiples palabras, la primera letra de las palabras siguientes debe ir en mayúscula (ej. int minutosPorHora = 60;).
 * **Caracteres permitidos:** Pueden contener letras, dígitos, guiones bajos (_) y el signo de dólar ($), pero **nunca** deben comenzar con un número.
 * **Sensibilidad a mayúsculas:** Java es *case-sensitive* (sensible a mayúsculas y minúsculas); la variable myVar es completamente distinta a myvar.
 * **Palabras reservadas:** No se pueden utilizar palabras clave del lenguaje (como int, class, public, void) como nombres de variables.
#### 3. Conversión de Tipos de Datos (Type Casting)
Ocurre cuando se asigna un valor de un tipo de datos primitivo a otro. Se divide en dos métodos:
 * **Widening Casting (Automático):** Pasa de un tipo de menor tamaño a uno de mayor tamaño sin pérdida de información (ej. de int a double). Java lo hace por sí solo.
 * **Narrowing Casting (Manual):** Pasa de un tipo de mayor tamaño a uno más pequeño (ej. de double a int). Requiere colocar el tipo de dato destino entre paréntesis antes del valor debido al riesgo de pérdida de precisión decimal:
   ```java
   double myDouble = 9.78;
   int myInt = (int) myDouble; // myInt valdrá 9
   
   ```
 * **Conversión de Strings a Números:** Para convertir una cadena de texto a un número entero o decimal, se utilizan los métodos de las clases de envoltura (*Wrapper Classes*):
   * Integer.parseInt("10");
   * Double.parseDouble("10.5");
#### 4. Operadores de Java
Son símbolos utilizados para realizar operaciones sobre variables y valores. Los más importantes expuestos son:
 * **Operadores Aritméticos:** Adición (+), Sustracción (-), Multiplicación (*), División (/) y Residuo o Módulo (%, que devuelve el resto de una división entera).
 * **Operadores de Asignación Compuesta:** Simplifican el código aplicando una operación y asignando el resultado inmediatamente (ej. x += 5; es equivalente a x = x + 5;).
 * **Operadores Lógicos:** Utilizados para determinar la lógica entre variables o valores:
   * && (**Logical AND**): Devuelve true si ambas condiciones son verdaderas.
   * || (**Logical OR**): Devuelve true si al menos una de las condiciones es verdadera.
   * ! (**Logical NOT**): Invierte el resultado (ej. si es true lo vuelve false).
#### 5. Lectura de Datos con la Clase Scanner
Para interactuar con el usuario a través de la consola, Java utiliza la clase Scanner (perteneciente al paquete java.util). Se debe instanciar un objeto de la siguiente manera:
```java
Scanner scan = new Scanner(System.in);

```
El objeto permite capturar diferentes tipos de datos según el método invocado:
 * scan.nextInt(): Salta espacios en blanco y captura el próximo entero.
 * scan.nextDouble(): Captura el próximo valor decimal.
 * scan.next(): Captura la siguiente palabra (delimitada por espacios).
 * scan.nextLine(): Lee una línea completa de texto, incluidos los espacios.


 