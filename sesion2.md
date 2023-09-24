<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 2


<!-- Su documentación aquí -->
1035431495

# Instalación de Java y configuración del entorno de desarrollo

## Java JDK 

Java JDK (Java Development Kit) es un conjunto de herramientas de desarrollo de software que proporciona todo lo necesario para desarrollar, depurar y ejecutar aplicaciones Java. Incluye un conjunto de bibliotecas de clases predefinidas, compiladores, herramientas de depuración y otras utilidades necesarias para el desarrollo de aplicaciones Java. 

El JDK es esencial para cualquier desarrollador que quiera crear aplicaciones Java, ya que proporciona las herramientas necesarias para compilar el código fuente, crear archivos ejecutables y depurar el código en caso de errores. Además, el JDK se actualiza regularmente para incluir nuevas características y mejoras de rendimiento. 

 [Java JDK ](https://www.oracle.com/java/technologies/downloads/#jdk19-windows)  

## IntelliJ IDEA Community Edition

IntelliJ IDEA Community Edition es un entorno de desarrollo integrado (IDE) gratuito de JetBrains para la creación de aplicaciones Java y otros lenguajes de programación, como Kotlin, Groovy y Scala. Proporciona un conjunto de herramientas de desarrollo que incluyen un editor de código, un depurador, un compilador y una serie de características de refactorización y análisis de código.

La versión Community Edition de IntelliJ IDEA es gratuita y de código abierto, lo que significa que cualquier desarrollador puede descargar y utilizar la herramienta de forma gratuita. Además, cuenta con una gran comunidad de desarrolladores que contribuyen con complementos y soluciones para problemas comunes. La versión Community Edition es adecuada para proyectos pequeños y medianos, mientras que la versión Ultimate, de pago, ofrece características avanzadas para proyectos más grandes y complejos.

[IntelliJ IDEA Community Edition](https://www.jetbrains.com/es-es/idea/download/?section=windows#section=windows)

## NetBeans

NetBeans es un entorno de desarrollo integrado (IDE) de código abierto y gratuito, que proporciona un conjunto de herramientas para desarrollar software en diferentes lenguajes de programación, como Java, C, C++, HTML, CSS y JavaScript, entre otros.

NetBeans es una herramienta multiplataforma, lo que significa que se puede ejecutar en diferentes sistemas operativos como Windows, Mac OS y Linux. Proporciona un editor de código, depurador, compilador y otras características esenciales para la programación, como refactorización de código, autocompletado de código y soporte de control de versión.

Además, NetBeans cuenta con una comunidad activa de desarrolladores que contribuyen con complementos y soluciones a problemas comunes, lo que lo convierte en una herramienta muy versátil y adaptable a diferentes proyectos y necesidades de programación.

[NetBeans](https://netbeans.apache.org/download/nb18/)

## Estructura de un programa en Java

Ejemplo de la estructura de un programa en Java con comentarios documentados para cada sección:

![Imagen](image.png)

**En este ejemplo, se sigue la estructura básica de un programa en Java con comentarios documentados que explican cada sección:**

* package com.example.miproyecto;: Se declara el paquete al que pertenece el programa. En este caso, el paquete es "com.example.miproyecto".

* import java.util.Scanner;: Se importa el paquete java.util y la clase Scanner para poder utilizarla en el programa. El Scanner se utiliza para leer la entrada del usuario.

* public class MiPrograma {: Se declara la clase principal del programa llamada MiPrograma. La palabra clave public indica que la clase es accesible desde cualquier otro lugar.

* public static void main(String[] args) {: Se define el método principal main, que es el punto de entrada del programa. Recibe un array de cadenas args como argumento, que puede ser utilizado para pasar argumentos desde la línea de comandos.

* int edad = 25;: Se declara una variable edad de tipo entero y se le asigna el valor 25.

* String nombre = "Juan";: Se declara una variable nombre de tipo cadena y se le asigna el valor "Juan".

* System.out.println("Hola, " + nombre + ". Tienes " + edad + " años.");: Se utiliza System.out.println() para imprimir un mensaje de saludo en la consola. La cadena se forma concatenando las variables nombre y edad utilizando el operador de suma (+).

## Declaración variables.

En Java, la declaración y asignación de variables es una de las tareas más básicas y esenciales para escribir cualquier programa. En esencia, una variable es un espacio en la memoria del ordenador reservado para almacenar un valor específico. La declaración de una variable es simplemente la creación de un espacio en la memoria para almacenar el valor que se asignará a la variable más adelante.

- La sintaxis para declarar una variable en Java es la siguiente:
tipoDato nombreVariable;

Donde tipoDato es el tipo de dato que se almacenará en la variable y nombreVariable es el nombre que se le dará a la variable.
Por ejemplo, si quisiéramos declarar una variable de tipo entero llamada "edad", la sintaxis sería la siguiente:
int edad;

Una vez que se ha declarado una variable, se puede asignar un valor a la variable utilizando el operador de asignación "=".

Por ejemplo, para asignar un valor de 25 a la variable "edad", se utiliza la siguiente sintaxis:

- edad = 25;

También es posible declarar y asignar valores a una variable en la misma línea de código. Por ejemplo, para declarar y asignar un valor de 3.14 a una variable de tipo "double" llamada "pi", se utilizaría la siguiente sintaxis:

- double pi = 3.14;

Es importante tener en cuenta que los nombres de las variables deben seguir las reglas de identificación de Java y ser descriptivos del valor que se va a almacenar en ellas. Además, una vez que se ha declarado una variable, se puede utilizar en cualquier lugar del programa siempre y cuando se haya asignado un valor a ella. Si se intenta utilizar una variable que no ha sido declarada previamente, se generará un error de compilación.

## Identificadores

En Java, hay convenciones y buenas prácticas para crear identificadores de variables, constantes, métodos y clases con el fin de hacer que el código sea más fácil de leer y entender. Algunas de estas convenciones y buenas prácticas son las siguientes:

*	Los nombres de variables deben comenzar con una letra minúscula. Si el nombre está compuesto por varias palabras, la primera letra de cada palabra debe ser mayúscula, excepto la primera palabra. Por ejemplo, "nombreDeVariable".

*	Los nombres de las constantes deben estar completamente en mayúsculas. Si el nombre está compuesto por varias palabras, se deben separar con guiones bajos. Por ejemplo, "CONSTANTE_DE_EJEMPLO".

*	Los nombres de las clases deben comenzar con una letra mayúscula, y si el nombre está compuesto por varias palabras, la primera letra de cada palabra debe ser mayúscula. Por ejemplo, "ClaseDeEjemplo".

*	Los nombres de los métodos deben comenzar con una letra minúscula, y si el nombre está compuesto por varias palabras, la primera letra de cada palabra debe ser mayúscula. Por ejemplo, "metodoDeEjemplo()".

* Los nombres de las variables deben ser descriptivos y deben indicar el propósito de la variable. Por ejemplo, "nombre", "edad", "numeroDeEjemplo".

*	Los nombres de los métodos deben indicar claramente lo que hace el método. Por ejemplo, "calcularPromedio()", "imprimirMensaje()", "obtenerResultado()".

*	Los nombres de las clases deben ser sustantivos y deben reflejar el propósito de la clase. Por ejemplo, "Persona", "Libro", "Automovil".

*	Es recomendable evitar el uso de abreviaturas en los nombres de variables, constantes, métodos y clases, a menos que sean ampliamente conocidas y entendidas por otros programadores.

*	Es recomendable seguir un estilo consistente en todo el código, para que sea más fácil de leer y entender.

## Estilos de convención de codificación.

1.	CamelCase (lowerCamelCase o mixedCase)

* En CamelCase, la primera letra de la primera palabra se escribe en minúscula y las primeras letras de las palabras subsiguientes se escriben en mayúscula.

* No se utilizan espacios ni guiones.
  
**Ejemplo: miVariable, calcularSuma, nombreCompleto.**

1.	PascalCase (UpperCamelCase o StudlyCase)

•	En PascalCase, la primera letra de cada palabra se escribe en mayúscula, incluida la primera palabra.

•	No se utilizan espacios ni guiones.

**Ejemplo: MiClase, CalcularPromedio, MetodoPrincipal.**

3.	Snake_case

•	En Snake_case, las palabras se escriben en minúscula y se separan mediante guiones bajos.

**Ejemplo: mi_variable, calcular_suma, nombre_completo.**

Este estilo es comúnmente utilizado en lenguajes como Python.

4.	Kebab-case

•	En Kebab-case, las palabras se escriben en minúscula y se separan mediante guiones medios.

**Ejemplo: mi-variable, calcular-suma, nombre-completo.**

Este estilo es menos común en la convención de codificación, pero se utiliza en algunos lenguajes y sistemas.

## Tipos de datos primitivos.

En Java, existen cinco tipos de datos primitivos que se utilizan comúnmente en la programación. Estos tipos de datos son int, float, double, boolean y char, y se utilizan para almacenar diferentes tipos de información en una variable.

**int: Este tipo de dato se utiliza para almacenar números enteros (sin decimales) con un rango de -2147483648 a 2147483647.** 

Por ejemplo, se puede declarar una variable de tipo int llamada "edad" para almacenar la edad de una persona:

**int edad = 25;**

  float: Este tipo de dato se utiliza para almacenar números decimales con un rango menor que el tipo de datos double. El tamaño de este tipo de dato es de 4 bytes. Por ejemplo, se puede declarar una variable de tipo float llamada "altura" para almacenar la altura de una persona:

  **float altura = 1.75f;**

•	double: Este tipo de dato se utiliza para almacenar números decimales con una precisión mayor que el tipo de datos float. El tamaño de este tipo de dato es de 8 bytes. Por ejemplo, se puede declarar una variable de tipo double llamada "peso" para almacenar el peso de una persona:

**double peso = 80.5;**

•	boolean: Este tipo de dato se utiliza para almacenar valores verdadero o falso (true o false). Por ejemplo, se puede declarar una variable de tipo boolean llamada "esMayorDeEdad" para almacenar si una persona es mayor de edad o no:

**boolean esMayorDeEdad = true;**

•	char: Este tipo de dato se utiliza para almacenar caracteres individuales, como letras, números y símbolos. El tamaño de este tipo de dato es de 2 bytes. Por ejemplo, se puede declarar una variable de tipo char llamada "inicial" para almacenar la inicial del nombre de una persona:

**char inicial = 'J';**

Es importante tener en cuenta que los nombres de las variables deben seguir las reglas de identificación de Java y ser descriptivos del valor que se va a almacenar en ellas. Además, es importante seleccionar el tipo de dato adecuado para cada variable para evitar errores en el programa.

[3schools](https://www.w3schools.com/java/java_data_types.asp)
 
![Byte](image.png)


## Tipos de datos no primitivos.

Además de los tipos de datos primitivos en Java, existen también tipos de datos no primitivos que se utilizan para almacenar información más compleja. Algunos ejemplos de tipos de datos no primitivos son:

**String:** 
Este tipo de dato se utiliza para almacenar cadenas de texto. Es un tipo de datos que no es primitivo, pero se utiliza con mucha frecuencia en la programación. Se declara utilizando la palabra clave "String" seguida del nombre de la variable y su valor entre comillas dobles. Por ejemplo:

**String nombre = "Juan";**

•	Arrays: Este tipo de dato se utiliza para almacenar una colección de valores del mismo tipo de dato. Se puede declarar un array utilizando la sintaxis siguiente:

**tipoDato[] nombreArray = new tipoDato[tamaño];**

Donde tipoDato es el tipo de datos que se almacenará en el array, nombreArray es el nombre que se le dará al array y tamaño es el número de elementos que se almacenarán en el array. Por ejemplo, para declarar un array de tipo int llamado "edades" que contiene tres elementos, se utilizaría la siguiente sintaxis:

**nt[] edades = new int[3];**

•	Objetos:(POO) Los objetos son instancias de una clase y se utilizan para almacenar información más compleja. Una clase es un tipo de dato personalizado que define las propiedades y métodos de un objeto. Para declarar un objeto, primero se debe crear una instancia de la clase utilizando la palabra clave "new", seguida del nombre de la clase y sus argumentos (si los tiene). Por ejemplo, si se tiene una clase llamada "Persona" que tiene propiedades como nombre, edad y altura, se puede crear una instancia de esa clase de la siguiente manera:

**Persona persona1 = new Persona("Juan", 25, 1.75);**

Es importante tener en cuenta que los tipos de datos no primitivos son más complejos que los tipos de datos primitivos, y su uso puede requerir conocimientos avanzados de programación.

## Conversión de tipos en Java - Casting

La conversión de tipos de datos en Java es un proceso mediante el cual se convierte un valor de un tipo de dato en otro. Java tiene dos tipos de conversión de datos: la conversión implícita y la conversión explícita.

La conversión implícita se produce automáticamente cuando se asigna un valor de un tipo de dato a una variable de otro tipo de datos compatible. Por ejemplo, si se asigna un valor de tipo "int" a una variable de tipo "double", Java realiza la conversión automáticamente.

**int x = 5;**

**double y = x; // Conversión implícita de int a double**

La conversión explícita, también conocida como "casting", se utiliza cuando se desea convertir un valor de un tipo de dato a otro tipo de datos que no es compatible de forma implícita. Para hacer una conversión explícita, se debe utilizar una sintaxis especial que indica al compilador que se desea convertir el valor a otro tipo de datos.

**double x = 3.14;**

**int y = (int) x; // Conversión explícita de double a int**

En este ejemplo, se utiliza la sintaxis "(int)" para indicar que se desea convertir el valor "x" de tipo "double" a un valor de tipo "int". Es importante tener en cuenta que la conversión explícita puede provocar la pérdida de información si se intenta convertir un valor a un tipo de datos con menos precisión.

Además de las conversiones implícitas y explícitas, Java también proporciona métodos para convertir valores entre diferentes tipos de datos, como los métodos "valueOf()" y "parseXxx()" de la clase "String". Estos métodos se utilizan para convertir valores de tipo "String" a otros tipos de datos, como "int" o "double".

## Método parseXxx()

En Java, los métodos parseXxx() se utilizan para convertir una representación de cadena (String) en un valor de tipo primitivo o un objeto de clase envolvente. Aquí tienes algunos ejemplos de métodos parseXxx() para diferentes tipos de datos:

•	parseInt() - Convierte una cadena en un valor entero (int):
String numberStr = "123";
int number = Integer.parseInt(numberStr);
System.out.println(number); // Salida: 123

•	parseDouble() - Convierte una cadena en un valor de punto flotante (double):
String decimalStr = "3.14";
double decimal = Double.parseDouble(decimalStr);
System.out.println(decimal); // Salida: 3.14

•	parseBoolean() - Convierte una cadena en un valor booleano (boolean):
String boolStr = "true";
boolean boolValue = Boolean.parseBoolean(boolStr);
System.out.println(boolValue); // Salida: true

•	parseLong() - Convierte una cadena en un valor entero largo (long):
String floatStr = "2.71828";
float floatValue = Float.parseFloat(floatStr);
System.out.println(floatValue); // Salida: 2.71828

•	parseFloat() - Convierte una cadena en un valor de punto flotante de precisión simple (float):
String longStr = "9876543210";
long longValue = Long.parseLong(longStr);
System.out.println(longValue); // Salida: 9876543210

## Método valueOf()

El método valueOf() en Java se utiliza para convertir un tipo de dato primitivo o una cadena en un objeto de clase envolvente (wrapper class). Aquí tienes un ejemplo de cómo se puede utilizar el método valueOf():
// Ejemplo 1: Converting a String to Integer object
String numberStr = "123";
Integer numberObj = Integer.valueOf(numberStr);
System.out.println(numberObj); // Salida: 123

// Ejemplo 2: Converting a String to Double object
String decimalStr = "3.14";
Double decimalObj = Double.valueOf(decimalStr);
System.out.println(decimalObj); // Salida: 3.14

// Ejemplo 3: Converting an int to Integer object
int intValue = 42;
Integer intObj = Integer.valueOf(intValue);
System.out.println(intObj); // Salida: 42

// Ejemplo 4: Converting a boolean to Boolean object
boolean boolValue = true;
Boolean boolObj = Boolean.valueOf(boolValue);
System.out.println(boolObj); // Salida: true

## Imprimir datos por consola

Para imprimir datos por consola en Java, se utiliza la clase System y su método out.println(). Aquí tienes una explicación de cómo funciona:

•	La clase System: Es una clase integrada en Java que proporciona acceso a varios recursos y funcionalidades del sistema. Para imprimir datos por consola, utilizamos el atributo out de la clase System, que es una instancia de la clase PrintStream.

•	El método println(): Es un método de la clase PrintStream que se utiliza para imprimir una línea de texto en la consola. Toma como argumento el valor que deseas imprimir y lo muestra en la salida estándar.

A continuación, se muestra un ejemplo básico de cómo imprimir datos por consola en Java:
public class ImprimirDatos {
    public static void main(String[] args) {
        int edad = 25;
        String nombre = "Juan";

        System.out.println("Mi nombre es " + nombre);
        System.out.println("Tengo " + edad + " años");
    }
}

En este ejemplo, se utilizan dos llamadas al método println() para imprimir información en la consola. La primera línea imprime el texto "Mi nombre es " seguido del valor de la variable nombre. La segunda línea imprime el texto "Tengo ", seguido del valor de la variable edad, seguido del texto " años".

## Capturar datos por consola
Para capturar datos por consola en Java, se utiliza la clase Scanner. Aquí tienes una explicación de cómo funciona:

•	La clase Scanner: Es una clase integrada en Java que se utiliza para leer la entrada del usuario desde la consola. Proporciona métodos para leer diferentes tipos de datos, como enteros, números de punto flotante, cadenas, etc.

•	Crear un objeto Scanner: Para capturar datos por consola, primero debes crear un objeto Scanner y asociarlo con la entrada estándar (System.in). Esto se hace de la siguiente manera:
import java.util.Scanner;

public class CapturarDatos {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese su nombre: ");
        String nombre = scanner.nextLine();

        System.out.print("Ingrese su edad: ");
        int edad = scanner.nextInt();

        System.out.println("Hola, " + nombre + ". Tienes " + edad + " años.");

        scanner.close();
    }
}

## Concatenar cadenas de texto

En Java, puedes concatenar cadenas de texto utilizando el operador de suma (+) o el método concat(). Aquí tienes ejemplos de ambos enfoques:

•	Operador de suma (+):

String cadena1 = "Hola";
String cadena2 = "mundo";

String resultado = cadena1 + " " + cadena2;
System.out.println(resultado);

En este ejemplo, se utilizan el operador de suma (+) y espacios en blanco para concatenar las cadenas cadena1 y cadena2. El resultado se asigna a la variable resultado y se imprime en la consola. La salida será: "Hola mundo".

•	Método concat():

String cadena1 = "Hola";
String cadena2 = "mundo";

String resultado = cadena1.concat(" ").concat(cadena2);
System.out.println(resultado);

En este ejemplo, se utiliza el método concat() para concatenar las cadenas cadena1 y cadena2. El método concat() combina la cadena actual con la cadena especificada como argumento y devuelve una nueva cadena resultante. El resultado se asigna a la variable resultado y se imprime en la consola. La salida será: "Hola mundo".

Ambos enfoques producen el mismo resultado de concatenación. Puedes elegir el que te resulte más conveniente en tu código.

## Declaración de constantes

En Java se utilizan las constantes para declarar valores fijos que no cambian durante la ejecución de un programa.

Algunas características de las constantes en Java:

•	Se declaran con la palabra reservada final. Esto hace que su valor no pueda ser modificado después.

•	Por convención los nombres de las constantes se escriben en MAYÚSCULAS y separando palabras con guion bajo "_" . Por ejemplo:

final double PI = 3.1416;

final int DIAS_SEMANA = 7;

*	El tipo de dato de la constante debe ser el adecuado para el valor que almacena. Por ejemplo, 3.1416 es double y 7 es int.

*	Las constantes pueden ser locales a un método o declaradas a nivel de clase (estáticas) para ser accesibles por todos los métodos.

*	Se puede utilizar cualquier tipo de dato para una constante: numéricos, cadena de texto, booleanos, etc.

*	Las constantes hacen el código más legible y mantenible al evitar valores literales.


# DESARROLLO

## Actividad 2: Instalación de Entornos de Desarrollo para Java y ejercicios de programación básica.
**
*Instalación de Entornos de Desarrollo para Java*

Objetivo: Familiarizarse con la instalación de los entornos de desarrollo necesarios para programar en Java.

El proceso de instalación de los entornos de desarrollo para Java, NetBeans IDE e IntelliJ IDEA, se puede resumir en los siguientes pasos:

Descargar NetBeans IDE desde el sitio web oficial de NetBeans.

Ejecutar el archivo de instalación de NetBeans y seguir las instrucciones del asistente de instalación.

Descargar IntelliJ IDEA desde el sitio web oficial de IntelliJ IDEA.

Ejecutar el archivo de instalación de IntelliJ IDEA y seguir las instrucciones del asistente de instalación.

Verificar la instalación abriendo cada IDE y creando un proyecto de Java.

Explorar las características y funcionalidades de cada entorno de desarrollo.

## Prueba y ejecución de ejercicios de programación básica.

**En esta actividad, pondremos en práctica los conceptos aprendidos de programación básica mediante la ejecución y prueba de diversos ejercicios. Utilizaremos el lenguaje de programación Java para implementar los programas y comprobaremos su funcionamiento ingresando diferentes valores de entrada.**

1. 

 Programa para calcular la hipotenusa de un triángulo rectángulo:
 import java.util.Scanner;

 public class HipotenusaTriangulo {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese el valor del primer cateto: ");
        double cateto1 = scanner.nextDouble();

        System.out.print("Ingrese el valor del segundo cateto: ");
        double cateto2 = scanner.nextDouble();

        double hipotenusa = Math.sqrt(Math.pow(cateto1, 2) + Math.pow(cateto2, 2));
        System.out.println("La hipotenusa del triángulo es: " + hipotenusa);

        scanner.close();
    }
  }


2. 

  Programa para determinar si un número es par o impar:
  import java.util.Scanner;

  public class ParImpar {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese un número: ");
        int numero = scanner.nextInt();

        if (numero % 2 == 0) {
            System.out.println("El número es par.");
        } else {
            System.out.println("El número es impar.");
        }

        scanner.close();
    }
  }

3.
 Programa para calcular el tercer ángulo de un triángulo:

 import java.util.Scanner;

 public class TercerAnguloTriangulo {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese el valor del primer ángulo: ");
        int angulo1 = scanner.nextInt();

        System.out.print("Ingrese el valor del segundo ángulo: ");
        int angulo2 = scanner.nextInt();

        if (angulo1 > 0 && angulo1 < 180 && angulo2 > 0 && angulo2 < 180) {
            int tercerAngulo = 180 - (angulo1 + angulo2);
            System.out.println("El valor del tercer ángulo es: " + tercerAngulo);
        } else {
            System.out.println("Los valores ingresados no son ángulos válidos.");
        }

        scanner.close();
    }
 }


4. 

 Programa para calcular el promedio de tres números:
 import java.util.Scanner;

 public class PromedioTresNumeros {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese el primer número: ");
        double numero1 = scanner.nextDouble();

        System.out.print("Ingrese el segundo número: ");
        double numero2 = scanner.nextDouble();

        System.out.print("Ingrese el tercer número: ");
        double numero3 = scanner.nextDouble();

        double promedio = (numero1 + numero2 + numero3) / 3;
        System.out.println("El promedio de los tres números es: " + promedio);

        scanner.close();
    }
 }


5. 
 Programa para calcular la longitud de una cadena de texto:
 import java.util.Scanner;

 public class LongitudCadena {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese una cadena de texto: ");
        String texto = scanner.nextLine();

        int longitud = texto.length();
        System.out.println("La longitud de la cadena es: " + longitud);

        scanner.close();
    }
 }

6. 
 Programa para calcular el área de un triángulo:
 import java.util.Scanner;

 public class AreaTriangulo {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese la base del triángulo: ");
        double base = scanner.nextDouble();

        System.out.print("Ingrese la altura del triángulo: ");
        double altura = scanner.nextDouble();

        double area = (base * altura) / 2;
        System.out.println("El área del triángulo es: " + area);

        scanner.close();
    }
 }

7. 
 Programa para calcular la raíz cuadrada de un número:
 import java.util.Scanner;

 public class RaizCuadrada {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese un número: ");
        double numero = scanner.nextDouble();

        double raizCuadrada = Math.sqrt(numero);
        System.out.println("La raíz cuadrada del número es: " + raizCuadrada);

        scanner.close();
    }
 }


8. 
 Programa para calcular el máximo común divisor (MCD) de dos números:
 import java.util.Scanner;

 publicclass MaximoComunDivisor {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese el primer número: ");
        int numero1 = scanner.nextInt();

        System.out.print("Ingrese el segundo número: ");
        int numero2 = scanner.nextInt();

        int mcd = calcularMCD(numero1, numero2);
        System.out.println("El máximo común divisor de los dos números es: " + mcd);

        scanner.close();
    }

    public static int calcularMCD(int a, int b) {
        while (b != 0) {
            int temp = b;
            b = a % b;
            a = temp;
        }
        return a;
    }
 }


9. 
 Programa para imprimir una cadena de texto en orden inverso:
 import java.util.Scanner;

 public class CadenaInversa {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese una cadena de texto: ");
        String texto = scanner.nextLine();

        String textoInverso = "";
        for (int i = texto.length() - 1; i >= 0; i--) {
            textoInverso += texto.charAt(i);
        }

        System.out.println("La cadena en orden inverso es: " + textoInverso);

        scanner.close();
    }
 }


10. 
 Programa para calcular el área de un rectángulo:
 import java.util.Scanner;

 public class AreaRectangulo {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese la base del rectángulo: ");
        double base = scanner.nextDouble();

        System.out.print("Ingrese la altura del rectángulo: ");
        double altura = scanner.nextDouble();

        double area = base * altura;
        System.out.println("El área del rectángulo es: " + area);

        scanner.close();
    }
 }

