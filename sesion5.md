<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 5 


<!-- Su documentación aquí -->
# Estructuras repetitivas (bucles, ciclos, iteraciones):

Las estructuras repetitivas, también conocidas como bucles, ciclos o iteraciones, son mecanismos de programación que permiten ejecutar un bloque de código varias veces, dependiendo de una condición específica. Estas estructuras son especialmente útiles cuando se necesita realizar una tarea de forma repetida o iterar sobre una colección de elementos.

## Existen varios tipos de estructuras repetitivas en Java:

* Bucle while:
  
Se ejecuta mientras se cumpla una condición booleana. La condición se evalúa antes de ejecutar cada iteración.

Sintaxis:

while (condición) {
    // Código que se ejecutará mientras se cumpla la condición
}

Ejemplo:

int i = 1;

while (i <= 10) {
    System.out.println(i);
    i++;
}

En este ejemplo, el bucle while imprimirá los números del 1 al 10.

* Bucle do-while:
  
Similar al bucle while, pero la condición se evalúa después de ejecutar cada iteración. Esto garantiza que el bloque de código se ejecute al menos una vez.

Sintaxis:

do  {
    // Código que se ejecutará mientras se cumpla la condición
} while (condición)

Ejemplo:

int i = 1;

do {
    System.out.println(i);
    i++;
} while (i <= 10);

En este caso, el bucle do-while también imprimirá los números del 1 al 10.

* Bucle for:
* 
Se utiliza cuando se conoce el número exacto de iteraciones a realizar. Tiene una estructura más compacta y se compone de una inicialización, una condición y una expresión de incremento.

Sintaxis:

for (inicialización; condición; incremento) {
    // bloque de código a repetir
}

Ejemplo:

for (int i = 1; i <= 10; i++) {
    System.out.println(i);
}

Aquí, el bucle for imprimirá los números del 1 al 10 de manera similar a los ejemplos anteriores.

* Bucle for-each:
  
Es utilizado para iterar sobre los elementos de una colección, como arreglos o listas. No se requiere un contador explícito, ya que itera automáticamente sobre cada elemento.

Sintaxis:

for (type variableName : arrayName) {
  // code block to be executed
}

Ejemplo:

int[] numeros = {1, 2, 3, 4, 5};

for (int numero : numeros) {
    System.out.println(numero);
}

## Ejemplos de estructuras repetitivas:

while

1 Calcular la suma de los números enteros del 1 al 100:

public class SumaNumeros {
    public static void main(String[] args) {
        int i = 1;
        int suma = 0;

        while (i <= 100) {
            suma += i;
            i++;
        }

        System.out.println("La suma de los números del 1 al 100 es: " + suma);
    }
}


2 Pedir al usuario que ingrese un número y verificar si es primo o no:

import java.util.Scanner;

public class VerificarPrimo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Ingrese un número: ");
        int numero = sc.nextInt();

        int i = 2;
        boolean esPrimo = true;

        while (i <= numero / 2) {
            if (numero % i == 0) {
                esPrimo = false;
                break;
            }
            i++;
        }

        if (esPrimo) {
            System.out.println(numero + " es un número primo.");
        } else {
            System.out.println(numero + " no es un número primo.");
        }
    }
}

3 Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de vocales que contiene:

import java.util.Scanner;

public class ContarVocales {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Ingrese una cadena de caracteres: ");
        String cadena = sc.nextLine();

        int i = 0;
        int contadorVocales = 0;

        while (i < cadena.length()) {
            char caracter = cadena.charAt(i);
            if (caracter == 'a' || caracter == 'e' || caracter == 'i' || caracter == 'o' || caracter == 'u' ||
                caracter == 'A' || caracter == 'E' || caracter == 'I' || caracter == 'O' || caracter == 'U') {
                contadorVocales++;
            }
            i++;
        }

        System.out.println("La cadena ingresada contiene " + contadorVocales + " vocales.");
    }
}


## do while

1 Adivina el número:

import java.util.Scanner;

public class AdivinaNumero {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int numeroSecreto = 42;
        int intento;
        
        do {
            System.out.print("Adivina el número secreto: ");
            intento = scanner.nextInt();
            
            if (intento == numeroSecreto) {
                System.out.println("¡Felicidades! Adivinaste el número.");
            } else {
                System.out.println("Intenta nuevamente.");
            }
        } while (intento != numeroSecreto);
    }
}


2 Suma de números:

import java.util.Scanner;

public class SumaNumeros {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int suma = 0;
        int numero;
        
        do {
            System.out.print("Ingresa un número (0 para terminar): ");
            numero = scanner.nextInt();
            
            suma += numero;
        } while (numero != 0);
        
        System.out.println("La suma de los números ingresados es: " + suma);
    }
}


3 Menú de opciones:

import java.util.Scanner;

public class MenuOpciones {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int opcion;
        
        do {
            System.out.println("Menu:");
            System.out.println("1. Opción 1");
            System.out.println("2. Opción 2");
            System.out.println("3. Salir");
            System.out.print("Selecciona una opción: ");
            opcion = scanner.nextInt();
            
            switch (opcion) {
                case 1:
                    System.out.println("Seleccionaste la opción 1.");
                    break;
                case 2:
                    System.out.println("Seleccionaste la opción 2.");
                    break;
                case 3:
                    System.out.println("Saliendo del programa...");
                    break;
                default:
                    System.out.println("Opción inválida. Intenta nuevamente.");
            }
        } while (opcion != 3);
    }
}




## for

1 Impresión de números pares:

public class NumerosPares {
    public static void main(String[] args) {
        for (int i = 2; i <= 10; i += 2) {
            System.out.println(i);
        }
    }
}

2 Cálculo del factorial:

import java.util.Scanner;

public class Factorial {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Ingresa un número: ");
        int numero = scanner.nextInt();
        int factorial = 1;
        
        for (int i = 1; i <= numero; i++) {
            factorial *= i;
        }
        
        System.out.println("El factorial de " + numero + " es: " + factorial);
    }
}


3 Suma de elementos de un arreglo:

public class SumaArreglo {
    public static void main(String[] args) {
        int[] numeros = {5, 8, 3, 2, 9};
        int suma = 0;
        
        for (int numero : numeros) {
            suma += numero;
        }
        
        System.out.println("La suma de los elementos del arreglo es: " + suma);
    }
}



## for-each

1 Suma de elementos en un arreglo

public class SumaArreglo {
    public static void main(String[] args) {
        int[] numeros = { 10, 20, 30, 40, 50 };
        int suma = 0;

        for (int numero : numeros) {
            suma += numero;
        }

        System.out.println("La suma de los elementos del arreglo es: " + suma);
    }
}


2 Imprimir elementos de una lista de cadenas

import java.util.ArrayList;
import java.util.List;

public class ImprimirLista {
    public static void main(String[] args) {
        List<String> palabras = new ArrayList<>();
        palabras.add("Hola");
        palabras.add("Mundo");
        palabras.add("en");
        palabras.add("Java");

        for (String palabra : palabras) {
            System.out.println(palabra);
        }
    }
}

3 Calificaciones y promedio de un estudiante
   
public class PromedioCalificaciones {
    public static void main(String[] args) {
        double[] calificaciones = { 85.5, 90.0, 78.5, 95.5, 88.0 };
        double suma = 0;

        for (double calificacion : calificaciones) {
            suma += calificacion;
        }

        double promedio = suma / calificaciones.length;
        System.out.println("El promedio de calificaciones es: " + promedio);
    }
}

## DESARROLLO


