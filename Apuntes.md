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
