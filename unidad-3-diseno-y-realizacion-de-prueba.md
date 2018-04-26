# Unidad 3: Diseño y realización de prueba

### Introducción

En esta Unidad aprenderemos a:

* Identificar los diferentes tipos de pruebas.
* Definir casos de prueba.
* Efectuar pruebas unitarias de clases y funciones.
* Efectuar pruebas de integración, de sistema y de aceptación.
* Realizar medidas de calidad sobre el software desarrollado.

#### Objetivos de las pruebas

* Una buena prueba debe centrarse en dos objetivos:
  1. probar si el software no hace lo que debe hacer
  2. probar si el software hace lo que no debe hacer.
* Existen distintos **frameworks** para la realización de pruebas.

#### Framework

* En general, un framework \(marco de trabajo\) está compuesto por:
  * un conjunto de las mejores prácticas y suposiciones // o sea, una forma de trabajar
  * herramientas comunes // 
  * bibliotecas // software que permite invocar o realizar ciertas operaciones
* Permite unificar el proceso de desarrollo entre desarrolladores.

### Pruebas

#### Forma de las pruebas

* **Pruebas dinámicas:** Requieren la ejecución de la aplicación. Permiten medir el comportamiento de la aplicación desarrollada.
* **Pruebas estáticas:** Se realizan sin ejecutar el código de la aplicación. Se examina el código fuente. // Son pruebas para ver fallos en el mismo código, como fallos de escritura, etc.

#### Estrategias de prueba

* **Caja negra:** Se estudia el sistema desde fuera. Son pruebas funcionales. // Ejecutamos el código y vemos los resultados, sin necesidad de conocer cómo funciona el código, solo viendo la entrada y salida. Muchas pruebas funcionales son de caja negra.
* **Caja blanca:** Se examina el código fuente y su ejecución. Son pruebas estructurales. // Se ve la estructura del código y vemos los condicionales, bucles, etc, para ver como va funcionando el código y que caminos lleva.

#### Estrategias de prueba

![Caja blanca vs Caja negra](https://github.com/Diegocd/APUNTES_ED/tree/8039364e1bfcd130be6d3e2fdf5cc47543d05501/assets/caja_blanca-caja_negra.png)

#### Estrategias de prueba de caja negra

* Se estudia el sistema desde fuera. // 
* Se trabaja sobre la interfaz. // Puede ser una interfaz de red o de programación, no necesariamente gráfica.
* No se tienen en cuenta los detalles internos de funcionamiento. // Si funciona bien, con eso basta.
* Se proporcionan entradas y se estudian las salidas. // Normalmente pasamos parámetros a un métodos y estudiamos el resultado.
* Principales técnicas: // Se pueden ejecutar una de las dos o ambas juntas.
  * Particiones de equivalencia // Agrupar los casos de prueba en clases homogéneas, para no tener que probar infinitos casos, 

    sólo unos pocos de cada uno.

  * Valores límite // Se comprueban los límites del rango de los códigos/métodos. 

#### Estrategias de prueba de caja blanca

* Se examina el código fuente y su ejecución. //
* Se comprueban los flujos de ejecución dentro de cada unidad \(función, clase, módulo, etc.\) //
* También pueden comprobarse los flujos entre unidades durante la integración. // Podemos comprobar si el envio de mensajes,

  parámetros, etc son correctos

* E incluso entre subsistemas, durante las pruebas de sistema.
* Principales técnicas:
  * Cobertura lógica // o de código, la cual sirve para comprobar que todos los caminos del código se ejecuten, para 

    cubrir todo. Por ejemplo, los diversos caminos que hay en un if/else, etc.

  * Prueba de bucles // Es una prueba específica, normalmente manual.

#### Tipos de pruebas

* **Funcionales:** Evaluan el cumplimiento de los requisitos. // Se evalúa lo que se pide y punto, sin mirar nada más.
* **No funcionales:** Evaluan aspectos adicionales como rendimiento, seguridad, ... // No estan relacionadas con los requisitos específicos, pero ayudan a que se cumplan \(rendimiento, seguridad, etc\).

#### Pruebas funcionales

* Pruebas unitarias \(o de unidad\)// Son las pruebas principales, donde se prueban las clases y sus respectivos métodos.
* Pruebas de regresión // Como a medida de que para el tiempo se reutilizan o cambian códigos antiguos, a veces se producen errores regresivos, para ello estan las pruebas de regresión, para ver que lo que funcionaba sigue haciéndolo.
* Pruebas de integración // Es la comprobación de que el conjunto de códigos, clases y metodos funcionan bien juntas. Son mas difíciles de automatizar.
* Pruebas del sistema // Son pruebas manuales, normalmente no funcionales, que son pruebas de conjunto.
* Pruebas de humo \(smoke test\) // Comprueba la funcionalidad imprescindible o básica de una aplicación.
* Pruebas alfa y beta // Las pruebas beta son pruebas del producto por un usuario en un entorno no controlado, las alfa siempre 

  son en un entorno controlado por personal cualificado, con cierto conocimiento de la aplicación.

* Pruebas de aceptación \(validación por parte del cliente\) // Las pruebas finales que se hacen de cara a validar que se cumplen los requisitos especificados.

#### Pruebas no funcionales

* Pruebas de usabilidad // apariencia de la interfaz
* Pruebas de rendimiento // 
* Pruebas de stress // Prueba para ver los límites 
* Pruebas de seguridad // Prueba para ver que no hay errores de acceso
* Pruebas de compatibilidad //  pruebas para comprobar hasta que punto es compatible con otros programas, etc.
* Pruebas de portabilidad // pruebas de que sean portables entre sistemas operativos, que nivel de portabilidad tiene
* ...

#### Mecanismos de prueba

* Manual
  * Mediante pruebas realizadas por personal de la empresa o externo.
* Automático
  * Mediante software que ejecuta código de forma automatizada y compara los resultados obtenidos y los resultados esperados.

#### Soporte del depurador

* Puntos de ruptura
* Ejecución paso a paso
* Análisis de variables

#### Automatización de pruebas

* Frameworks de pruebas \(xUnit\)
* Aserciones

[https://en.wikipedia.org/wiki/XUnit](https://en.wikipedia.org/wiki/XUnit)

#### Frameworks para pruebas

* Java: JUnit, TestNG
* C++: CppUnit, Google Test
* PHP: PHPUnit
* Javascript: Mocha

[https://en.wikipedia.org/wiki/List\_of\_unit\_testing\_frameworks](https://en.wikipedia.org/wiki/List_of_unit_testing_frameworks)

#### Caso de prueba

* precondición --&gt; postcondición
* Una entrada conocida  --&gt; Una salida esperada 

[http://www.jtech.ua.es/j2ee/publico/lja-2012-13/sesion04-apuntes.html](http://www.jtech.ua.es/j2ee/publico/lja-2012-13/sesion04-apuntes.html)

#### JUnit4/5 - Anotaciones

* @BeforeClass / @BeforeAll
* @Before / @BeforeEach
* @Test
* @After / @AfterEach
* @AfterClass / @AfterAll
* @Ignore

#### JUnit - Aserciones

```java
import org.junit.Test;
import static org.junit.Assert.*;

// ... 
fail()                         // el test termina con fallo
assertTrue(expresión)          // expresión es true ?
assertFalse(expresión)         // expresión es false ?
assertEquals(esperado,real)    // esperado es igual a real ?
assertNotEquals(esperado,real) // esperado es distinto de real ?
assertNull(objeto)             // objeto es null ?
assertNotNull(objeto)          // objeto es distinto de null ?

// objeto_esperado es igual a objeto_real ?
assertSame(objeto_esperado,objeto_real)
// objeto_esperado es distinto de objeto_real ?
assertNotSame(objeto_esperado,objeto_real)
```

[http://junit.org/junit4/javadoc/4.12/org/junit/Assert.html](http://junit.org/junit4/javadoc/4.12/org/junit/Assert.html)

#### TDD

* Desarrollo guiado por pruebas de software, o Test-Driven Development \(TDD\) 
  * Escribir las pruebas primero \(Test First Development\).
  * Refactorización \(Refactoring\).

### Integración

#### Formas de integración

* Integración Big bang
* Integración Descendente
* Integración Ascendente
* Integración Continua \(CI\)

#### Servidores de integración continua

> CI : Integración continua  
> CD : Despliegue continuo

* Jenkins
* Bamboo
* TravisCI
* CircleCI

Note: CI=Continuous Integration / CD=Continuous Delivery.

## Calidad

### Control de calidad

Control de calidad = medición de la calidad de un producto --&gt; Pruebas

### Calidad del proceso/producto \(QA/QC\)

* QA es un conjunto de actividades para garantizar la **calidad en los procesos** mediante los cuales se desarrollan los productos. 
* QC es un conjunto de actividades para garantizar **la calidad de los productos**. Las actividades se centran en identificar defectos en los productos reales producidos.

Note: QA = Quality Assurance / QC = Quality Control

### Factores de calidad

* Corrección
* Fiabilidad
* Eficiencia
* Seguridad
* Facilidad de uso
* Mantenibilidad
* Flexibilidad
* Facilidad de prueba
* Transportabilidad
* Reusabilidad
* Interoperatividad

