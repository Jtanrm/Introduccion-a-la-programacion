<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4


<!-- Su documentación aquí -->
## Estructuras de control en Java

Las estructuras de control en Java son construcciones del lenguaje que permiten controlar el flujo de ejecución de un programa. Los principales tipos de estructuras de control en Java son:

* Estructuras de selección: permiten elegir entre varias opciones. Incluyen la sentencia if, la sentencia switch.

* Estructuras repetitivas: permiten repetir un bloque de código mientras se cumpla una condición. Incluyen los bucles for, while, do-- while.

* Estructuras de salto: permiten cambiar el flujo de ejecución, saltando parte del código. Incluyen las sentencias break, continue, return.

## Estructuras condicionales:

Las estructuras condicionales en Java permiten tomar decisiones y ejecutar ciertas partes de código dependiendo si se cumple o no una determinada condición.

Las principales estructuras condicionales son:

1 if: Ejecuta un bloque de código si se cumple la condición.

Sintaxis:

if (condición) {
  // código a ejecutar 
}

2 if - else: Ejecuta un bloque si se cumple la condición, y otro bloque distinto si no se cumple.
Sintaxis:

if (condición) {
  // código si se cumple
} else {
  // código si no se cumple
}

3 if - else if - else: Permite evaluar múltiples condiciones. Se ejecuta el primer bloque donde se cumpla la condición.
Sintaxis:

if (condición 1) {
  // código si se cumple 1
} else if (condición 2) {
  // código si se cumple 2 
} else {
  // código si no se cumple ninguna
}

4 Operador ternario

El operador ternario en Java es una expresión que se utiliza para evaluar una condición y devolver uno de dos valores, dependiendo del resultado de la evaluación. La sintaxis del operador ternario es:

Sintaxis:

variable = (condicion) ? valor_si_verdadero : valor_si_falso;

5 switch: Evalúa una variable o expresión y ejecuta el código del case que coincida con el valor.
Sintaxis:

switch(expresión) {
  case valor1: 
    //código
    break;
  case valor2: 
   //código
   break;
  default:
   //código por defecto  
}

Estas estructuras permiten controlar el flujo del programa ejecutando código de manera condicional. Son muy útiles para realizar selecciones y tomar decisiones en la lógica de un programa.

## Ejemplos if:

Estos ejemplos muestran diferentes formas de utilizar estructuras condicionales en Java para tomar decisiones basadas en ciertas condiciones.

1- Comprobando si una variable es mayor que otra:

int x = 10;
int y = 5;

if (x > y) {
  System.out.println("x es mayor que y");
}

2- Comprobando si una variable es diferente de un valor específico:
 
int edad = 18;

if (edad != 18) {
  System.out.println("La edad no es 18");
}

3- Comprobando si una variable está dentro de un rango de valores:


int nota = 10;

if (nota >= 9 && nota <= 10) {
  System.out.println("La nota es excelente");
}

## Ejemplos if else:

1- Comprobando si una variable es mayor que otra y, si no, imprimiendo un mensaje diferente:

int x = 10;
int y = 5;

if (x > y) {
  System.out.println("x es mayor que y");
} else {
  System.out.println("x es menor o igual que y");
}

2- Comprobando si una variable es igual a un valor específico y, si no, imprimiendo un mensaje diferente:

String nombre = "Juan";

if (nombre.equals("Juan")) {
  System.out.println("El nombre es Juan");
} else {
  System.out.println("El nombre no es Juan");
}

3- Comprobando si una variable está dentro de un rango de valores y, si no, imprimiendo un mensaje diferente:

int nota = 10;

if (nota >= 9 && nota <= 10) {
  System.out.println("La nota es excelente");
} else {
  System.out.println("La nota no es excelente");
}

## Ejemplos else if:

1 Comprobando si una variable es mayor que otra, si no, si es igual y, si no, imprimiendo un mensaje diferente:
   
int x = 10;
int y = 5;

if (x > y) {
  System.out.println("x es mayor que y");
} else if (x == y) {
  System.out.println("x es igual a y");
} else {
  System.out.println("x es menor que y");
}

2 Comprobando si una variable está dentro de un rango de valores, si no, si es mayor o si es menor y, si no, imprimiendo un mensaje diferente:

int nota = 10;

if (nota >= 9 && nota <= 10) {
  System.out.println("La nota es excelente");
} else if (nota > 10) {
  System.out.println("La nota es sobresaliente");
} else if (nota < 0) {
  System.out.println("La nota es inválida");
} else {
  System.out.println("La nota es buena");
}

3 Comprobando si una variable está vacía o no, si no, si tiene una longitud específica y, si no, imprimiendo un mensaje diferente:

String cadena = "";

if (cadena.isEmpty()) {
  System.out.println("La cadena está vacía");
} else if (cadena.length() == 0) {
  System.out.println("La cadena es nula");
} else {
  System.out.println("La cadena no está vacía");
}

## Ejemplos operador ternario:

1 Devuelve el valor máximo de dos números
int max = (a > b) ? a : b;

// Devuelve el texto "El número es positivo" si el número es mayor que 0,
// y el texto "El número es negativo" si el número es menor o igual a 0.
String texto = (numero > 0) ? "El número es positivo" : "El número es negativo";


2 Devuelve el valor máximo de tres números
int max = (a > b) ? (a > c ? a : c) : (b > c ? b : c);

// Devuelve el texto "El número es positivo" si el número es mayor que 0,
// el texto "El número es cero" si el número es igual a 0,
// y el texto "El número es negativo" si el número es menor que 0.
String texto = (numero > 0) ? "El número es positivo" : (numero == 0 ? "El número es cero" : "El número es negativo");


3 Devuelve el texto "El número es par" si el número es par, y el texto "El número es impar" si el número es impar.
String texto = (numero % 2 == 0) ? "El número es par" : "El número es impar";


## Otros ejemplos

1 Comprobación del número par o impar:
int numero = 7;

if (numero % 2 == 0) {
    System.out.println("El número es par.");
} else {
    System.out.println("El número es impar.");
}

2 Evaluación de la calificación de un estudiante:
int calificacion = 85;

if (calificacion >= 90) {
    System.out.println("Excelente");
} else if (calificacion >= 80) {
    System.out.println("Bueno");
} else if (calificacion >= 70) {
    System.out.println("Regular");
} else {
    System.out.println("Reprobado");
}

3 Verificación de la elegibilidad para votar:
int edad = 17;

if (edad >= 18) {
    System.out.println("Eres elegible para votar.");
} else {
    System.out.println("No eres elegible para votar.");
}

4 Determinar si un número es positivo, negativo o cero:
int numero = -3;

if (numero > 0) {
    System.out.println("El número es positivo.");
} else if (numero < 0) {
    System.out.println("El número es negativo.");
} else {
    System.out.println("El número es cero.");
}

5 Validación de una contraseña:
String contraseña = "secreta123";

if (contraseña.equals("secreta123")) {
    System.out.println("Contraseña correcta. Acceso concedido.");
} else {
    System.out.println("Contraseña incorrecta. Acceso denegado.");
}

## Ejemplos switch:

1 Escribe un programa que le pida al usuario que ingrese un día de la semana. El programa debe imprimir el número del día de la semana.
import java.util.Scanner;

public class DiaSemana {

  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);

    System.out.println("Ingrese un día de la semana: ");
    String dia = sc.nextLine();

    switch (dia) {
      case "lunes":
        System.out.println("1");
        break;
      case "martes":
        System.out.println("2");
        break;
      case "miércoles":
        System.out.println("3");
        break;
      case "jueves":
        System.out.println("4");
        break;
      case "viernes":
        System.out.println("5");
        break;
      case "sábado":
        System.out.println("6");
        break;
      case "domingo":
        System.out.println("7");
        break;
      default:
        System.out.println("Día no válido");
    }
  }
}

2 Escribe un programa que le pida al usuario que ingrese una calificación de 1 a 10. El programa debe imprimir la calificación en letras.
import java.util.Scanner;

public class Calificacion {

  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);

    System.out.println("Ingrese una calificación de 1 a 10: ");
    int calificacion = sc.nextInt();

    switch (calificacion) {
      case 1:
        System.out.println("Insuficiente");
        break;
      case 2:
        System.out.println("Insuficiente");
        break;
      case 3:
        System.out.println("Insuficiente");
        break;
      case 4:
        System.out.println("Suficiente");
        break;
      case 5:
        System.out.println("Bien");
        break;
      case 6:
        System.out.println("Notable");
        break;
      case 7:
        System.out.println("Sobresaliente");
        break;
      case 8:
        System.out.println("Sobresaliente");
        break;
      case 9:
        System.out.println("Sobresaliente");
        break;
      case 10:
        System.out.println("Excelente");
        break;
      default:
        System.out.println("Calificación no válida");
    }
  }
}

3 Escribe un programa que le pida al usuario que ingrese un número entero. El programa debe imprimir la estación del año correspondiente al número.
import java.util.Scanner;

public class Estacion {

  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);

    System.out.println("Ingrese un número entero: ");
    int numero = sc.nextInt();

    switch (numero) {
      case 1:
      case 2:
      case 3:
        System.out.println("Invierno");
        break;
      case 4:
      case 5:
      case 6:
        System.out.println("Primavera");
        break;
      case 7:
      case 8:
      case 9:
        System.out.println("Verano");
        break;
      case 10:
      case 11:
      case 12:
        System.out.println("Otoño");
        break;
      default:
        System.out.println("Número no válido");
    }
  }
}

# Actividad 4: 

Ejercicios de control de flujo con expresiones compuestas

// Variables de tipo String
String nombre = "Juan Pérez";
String apellido = "González";
String identificación = "1000000001";
String correo = "juan.perez@ejemplo.com";
String carrera = "Desarrollo de Software";
String universidad = "Cesde";
// Variable de tipo int
int edad = 20;
// Variable de tipo boolean
boolean esActivo = true;
boolean becado = false;
// Variable de tipo char
char género = 'M';
// Variable de tipo double
double promedio = 4.5;
// Variable de tipo int
int semestre = 2;

**Con la información anterior, implementa los siguientes ejercicios:**

Determinar si el estudiante es mayor de edad y tiene un estado activo.

Determinar si el estudiante tiene una beca o una carrera relacionada con el desarrollo de software.

Determinar si el estudiante está en el último semestre de su carrera y tiene un estado activo.

Determinar si el estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0.

Mostrar toda la información del estudiante si está matriculado en el Cesde.

Asignar una beca del 50% si el estudiante está matriculado en el Cesde, tiene un promedio superior a 4.0 y está activo.

Determinar la cantidad de beca que recibe el estudiante según su promedio:

0.0 - 3.4: El estudiante no recibe beca.

3.5 - 3.9: El estudiante recibe una beca parcial del 25%.

4.0 - 4.4: El estudiante recibe una beca parcial del 50%.

4.5 - 5.0: El estudiante recibe una beca completa.


## DESARROLLO

package com.mycompany.mavenproject2;

/**
 * import java.util.Scanner;
 *
 * @author JHONATAN
 */
public class Mavenproject2 {

    public static void main(String[] args) {
       
        // Variables de tipo String
        String nombre = "Jhonatan";
        String apellido = "Rodriguez";
        String identificación = "1035431495";
        String correo = "jtan.rm@gmail.com";
        String carrera = "Desarrollo de Software";
        String universidad = "Cesde";
// Variable de tipo int
        int edad = 28;
// Variable de tipo boolean
        boolean esActivo = true;
        boolean becado = false;
// Variable de tipo char
        char género = 'M';
// Variable de tipo double
        double promedio = 4.5;
// Variable de tipo int
        int semestre = 2;

        System.out.println("");
        System.out.println(" el estudiante es mayor de edad y tiene un estado activo. ");
        if (edad >= 18 && esActivo) {
            System.out.println("el estudiante es mayor de edad y esta activo");
        } else {
            System.out.println("el estudiante es menor de edad o no esta activo");
        }
        System.out.println("-------------------------------------------------------");
        System.out.println("El estudiante tiene una beca o una carrera relacionada con el desarrollo de software");

        if (becado == true || carrera.equals("Desarrollo de Software")) {
            System.out.println("el estudiante tiene una beca o estudia dsarrollo de software");
        } else {
            System.out.println("el estudiante no es becado y no estudia desarrollo de software");
        }
        System.out.println("-------------------------------------------------------");
        System.out.println("determinar si e estudiante esta en el ultimo semestre de su carrera y tiene un esado activo");

        if (semestre == 3 && esActivo) {
            System.out.println("el estudiante esta en el ultimo semestre y esta activo");
        } else {
            System.out.println("el estudiante no esta en ultimo semestre o no esta activo");
        }
        System.out.println("-------------------------------------------------------");
        System.out.println("determinar si e estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4");

        if (carrera.equals("Desarrollo de Software") && promedio > 4.0) {
            System.out.println("esta en desarrollo de software y un promedio mayor a 4");
        } else {
            System.out.println("el estudiante no esta en desarrollo de software o no tiene promedio mayor a 4");
        }
        System.out.println("-------------------------------------------------------");
        System.out.println("Mostrar toda la información del estudiante si está matriculado en el Cesde.");

        if (universidad.equals("Cesde")) {
            System.out.println("Nombre: " + nombre);
            System.out.println("Apellido: " + apellido);
            System.out.println("Identificacion: " + identificación);Actividad Sesión 5

            System.out.println("Edad: " + edad);
            System.out.println("Genero: " + género);
            System.out.println("Coreo: " + correo);
            System.out.println("Carrera: " + carrera);
            System.out.println("Universidad: " + universidad);
            System.out.println("Activo: " + esActivo);
            System.out.println("Becado: " + becado);
            System.out.println("Promedio: " + promedio);
            System.out.println("Semestre: " + semestre);
        } else {
            System.out.println("el estudiante no esta matriculado en cesde");
        }
        System.out.println("-------------------------------------------------------");
        System.out.println("Asignar una beca del 50% si el estudiante está matriculado en el Cesde, tiene un promedio superior a 4.0 y está activo.");

        if (universidad.equals("Cesde") && promedio > 4.0 && esActivo) {
            System.out.println("asignar beca");
        } else {
            System.out.println("no asignar beca");
        }
        System.out.println("-------------------------------------------------------");
        System.out.println("Determinar la cantidad de beca que recibe el estudiante según su promedio.");

        if (promedio >= 0.0 && promedio <= 3.4) {
            System.out.println("El estudiante no recibe beca");
        } else if (promedio >= 3.5 && promedio <= 3.9) {
            System.out.println("el estudiante recibe 25% de beca");
        } else if (promedio >= 4.0 && promedio <= 4.4) {
            System.out.println("el estudiante recibe 50% de beca");
        } else if (promedio >= 4.5 && promedio <= 5.0) {
            System.out.println("el estudiante recibe 100% de beca");
        } else {
            System.out.println("Nota no valida");

        }
    }
}



