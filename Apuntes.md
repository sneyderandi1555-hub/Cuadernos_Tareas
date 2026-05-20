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