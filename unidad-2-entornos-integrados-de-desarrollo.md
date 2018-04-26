# Unidad 2: Entornos integrados de desarrollo

## Introducción

En esta Unidad aprenderemos a:

* Instalar entornos de desarrollo, propietarios y libres.
* Personalizar y automatizar el entorno de desarrollo.
* Generar ejecutables a partir de código fuente.
* Identificar las características comunes y específicas de diversos entornos de desarrollo.

### Conceptos

* Codigo fuente  - El texto o archivo de texto legible escrito en lenguje de programacion
* Codigo intermedio u objeto - Codigo binario no ejecutable
* Codigo binario - Codigo binario ejecutable 
* Bibliotecas \(librerías\) - Una serie de archivos distribuible con codigo fuente y/o objeto.Amplían la funcionalidad del lenguaje.
* Compilar - Coge el codigo fuente y traduce a codigo objeto \(en el caso de java a bytecode\)
* Enlazar \(Link\) - Coger varios archivos objetos y unirlos todos para crear un ejecutable.
* Interpretar - Seria el equivalente a compilar. Lee el codigo fuente y se genera el codigo binario para ejecutarlo en el momento. No se genera ningún archivo.

## Herramientas básicas

### Lo básico

* Editor de texto: permite escribir código fuente -  con uno vale
* Compilador: genera código objeto a partir del código fuente
* Enlazador: agrupa varios archivos objeto en uno binario
* Interprete: lee código fuente y genera código binario para su ejecución - 

### Bibliotecas \(o librerías\) \(I\)

> Conjunto de archivos objeto que extienden la funcionalidad del lenguaje

* **Biblioteca estándar** del lenguaje - Todos los lenguajer tienen una 
* **Bibliotecas adicionales** - Hay muchas.

### Bibliotecas \(o librerías\) \(II\) - Varían de un lenguaje a otro

* **Biblioteca estándar del lenguaje C** - Es muy pequeña
  * Entrada y salida por terminal
  * Manejo de archivos
  * Funciones matemáticas
* **Biblioteca estándar del lenguaje Java** - 
  * Entrada y salida por terminal
  * Manejo de archivos
  * Funciones matemáticas
  * Interfaz gráfica 
  * Red
  * Bases de datos
  * Gráficos \(sólo 2D\)

### Bibliotecas \(o librerías\) \(III\)

* Cada biblioteca está compuesta por varios archivos objeto
* Tipos
  * bibliotecas dinámicas \(.DLL o .so\) \(.jar en Java\) Casi siempre se usan estas porque tienen ciertas ventajas frente a las estándar. No se juntan las bibliotecas con el ejecutable. Windows

    Ventajas:

    -Al tener la biblioteca separada se puede actualizar independientemente del programa

    -El ejecutable pesa menos

    -Se pueden compartir entre varios programas.

    Desventajas:

    -No es un programa autocontenido o independiente, depende de la biblioteca para funcionar.

    -

    * muy usadas

  * bibliotecas estáticas \(.LIB o .a\) lib para windows .a para windows cuando compilamos lo mete con el ejecutable 
    * menos usadas actualmente

      Ventaja:

      -Es autocontenido el ejecutable.

      -

      Desventaja:

      -El ejecutable pesa mas

      -Aumenta el espacio necesario en disco

      -No se puede compartir entre programas

      .Si se modifica la biblioteca hay que volver a recompilarlo todo.

### Bibliotecas \(o librerías\) \(IV\)

* Una biblioteca se compone de 2 partes:
  * Especificación \(ofrece una API\)
  * Implementación 

**API** = Interfaz de Programación de Aplicaciones - todas las bibliotecas tienen una. son la especificacion \(clases,metodos que podemos utilizar y cómo utilizarlas\) Se da en todos los lenguajes.

### Entorno necesario en java

* JRE: necesario para ejecutar programas
  * JVM \(inteprete java\)
  * Biblioteca estándar
* JDK: necesario para desarrollar programas
  * Herramientas: javac, jar, javadoc, ...

### Construir \(Build\) \(I\)

> Construir \(Build\) = Compilar + Enlazar

* Dos opciones:
  * Herramientas de construcción - vienen integrados para compilar, enlazar etc archivos.
  * Servidor de construcción

### Construir \(Build\) \(II\)

#### **Herramientas de construcción**

* make, ninja \(C, C++\)
* ant, maven, gradle \(Java\)
* grunt, gulp \(Javascript\)
* rake \(ruby\)

### Construir \(Build\) \(III\)

#### **Archivos de construcción \(buildfiles\)**

* make: **Makefile**
* ninja: **build.ninja**
* ant: **build.xml**
* maven: **pom.xml**
* gradle: **build.gradle**
* grunt: **Gruntfile.js**
* gulp: **gulpfile.js**
* rake: **Rakefile**

### Construir \(Build\) \(IV\)

* Generadores de archivos de construcción
  * CMake: CMakeLists.txt
  * Meson: meson.build  

### Construir \(Build\) \(V\)

* Servidores de construcción
  * Jenkins 
  * TravisCI
  * CircleCI
  * Bamboo
  * TeamCity

## Entornos integrados de desarrollo \(IDE\)

### Ejemplos

* Destinados principalmente a C++:
  * DevC++
  * Microsoft Visual Studio
  * QtCreator
* Destinados principalmente a Java:
  * Netbeans
  * Eclipse
  * IntelJ IDEA
  * Oracle JDeveloper

