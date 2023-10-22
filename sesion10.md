<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 10 

## Ejercicios de Lógica de Programación

## 1

## Crear un programa en Java para calcular el interés de un CDT

Un CDT (Certificado de Depósito a Término) es un producto financiero en el que un inversor deposita una cantidad de dinero en un banco por un plazo determinado y a cambio recibe una tasa de interés fija. Al final del plazo, el inversor recupera su inversión inicial más los intereses generados. Aquí hay un ejemplo de cómo crear un programa en Java para calcular el interés de un CDT:

import java.util.Scanner;
import java.text.DecimalFormat;

public class Main {
    public static void main(String[] args) {
        DecimalFormat decimalFormat = new DecimalFormat("#,###");
        Scanner scanner = new Scanner(System.in);

        System.out.println("Bienvenido al calculador de CDT!");

        // Pedir al usuario que ingrese los datos del CDT
        System.out.print("Ingrese el monto del depósito: ");
        double montoDeposito = scanner.nextDouble();

        System.out.print("Ingrese la tasa de interés anual (%): ");
        double tasaInteresAnual = scanner.nextDouble();

        System.out.print("Ingrese el plazo en meses: ");
        int plazoMeses = scanner.nextInt();

        // Calcular el interés y el monto total al vencimiento
        double tasaInteresMensual = tasaInteresAnual / 12 / 100;
        double interesMensual = montoDeposito * tasaInteresMensual;
        double montoTotalVencimiento = montoDeposito + (interesMensual * plazoMeses);

        // Mostrar el resumen del CDT
        System.out.println("Resumen del CDT:");
        System.out.println("- Monto del depósito: $" + decimalFormat.format(montoDeposito));
        System.out.println("- Tasa de interés anual: " + tasaInteresAnual + "%");
        System.out.println("- Plazo en meses: " + plazoMeses);
        System.out.println("- Interés mensual: $" + interesMensual);
        System.out.println("- Monto total al vencimiento: $" + decimalFormat.format(montoTotalVencimiento));
    }
}


En este ejemplo, el programa solicita al usuario que ingrese el monto del depósito, la tasa de interés anual y el plazo en meses. Luego, el programa utiliza fórmulas matemáticas simples para calcular el interés mensual y el monto total al vencimiento. Finalmente, el programa muestra un resumen del CDT que incluye el monto del depósito, la tasa de interés anual, el plazo en meses, el interés mensual y el monto total al vencimiento. Este programa puede ser útil para las personas que desean invertir en un CDT y desean calcular los intereses que pueden generar. También puede ser utilizado por los profesionales financieros que deseen calcular los intereses de los CDTs de sus clientes.

## 2

 ## Calcular la desviación estándar

La desviación estándar es una medida estadística que indica cuánto varían los valores de un conjunto de datos respecto a la media aritmética. En otras palabras, mide la dispersión de los datos alrededor de la media.**

La desviación estándar se calcula tomando la raíz cuadrada de la varianza, donde la varianza es la suma de los cuadrados de las diferencias entre cada valor y la media aritmética, dividido entre el número de valores menos uno.

La fórmula para calcular la desviación estándar es la siguiente:

Desviación estándar = √(Σ(xi - x̄)² / (n - 1))
Donde:
xi: cada valor en el conjunto de datos.
x̄: la media aritmética del conjunto de datos.
n: el número de valores en el conjunto de datos.
Por ejemplo, si tenemos un conjunto de datos {10, 12, 15, 18, 20}, la media aritmética sería (10+12+15+18+20)/5 = 15. La varianza se calcularía de la siguiente manera:
Varianza = [(10 - 15)² + (12 - 15)² + (15 - 15)² + (18 - 15)² + (20 - 15)²] / 4
         = 20.5
Y la desviación estándar sería:
Desviación estándar = √(20.5) ≈ 4.53


La desviación estándar se utiliza a menudo en estadísticas para describir la variabilidad de un conjunto de datos. Una desviación estándar más grande indica que los valores están más dispersos alrededor de la media, mientras que una desviación estándar más pequeña indica que los valores están más concentrados alrededor de la media.

Un ejemplo para entender la desviación estándar sería el siguiente:

Supongamos que tenemos un conjunto de datos que representan el número de horas que un grupo de estudiantes estudia por semana. El conjunto de datos es el siguiente:

{5, 10, 12, 15, 20}
Primero, calculamos la media aritmética del conjunto de datos:
Media aritmética = (5 + 10 + 12 + 15 + 20) / 5
                  = 12

La media aritmética nos indica que, en promedio, los estudiantes estudian 12 horas por semana.
A continuación, calculamos la varianza del conjunto de datos:
Varianza = [(5 - 12)² + (10 - 12)² + (12 - 12)² + (15 - 12)² + (20 - 12)²] / 4
         = 52.5


La varianza nos indica cuánto varían los datos con respecto a la media. En este caso, la varianza es relativamente grande, lo que sugiere que los datos están bastante dispersos alrededor de la media.

Finalmente, calculamos la desviación estándar del conjunto de datos:

Desviación estándar = √(52.5) ≈ 7.24

La desviación estándar nos indica cuánto se desvían los datos de la media. En este caso, la desviación estándar es relativamente grande, lo que confirma que los datos están bastante dispersos alrededor de la media.

En resumen, la desviación estándar es una medida estadística que indica cuánto varían los datos de la media. En el ejemplo anterior, la desviación estándar nos indica que los datos están bastante dispersos alrededor de la media, lo que sugiere que hay una gran variabilidad en el número de horas que los estudiantes estudian por semana.

Ejemplo en Java para calcular la desviación estándar de un conjunto de datos:

import java.util.Scanner;

class Main{
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);
    
    System.out.print("Ingresar datos separados por comas: "); 
    String input = scanner.nextLine();
    
    String[] dataStr = input.split(","); 
    double[] data = new double[dataStr.length];
    
    for (int i = 0; i < dataStr.length; i++) {
       data[i] = Double.parseDouble(dataStr[i]);
    }
      
    int n = data.length;  
    double mean = 0, sum = 0, standardDeviation = 0;
      
    // Calcula la media aritmética   
    for (double num : data) {   
       sum += num;
    } 
    mean = sum / n;
      
    // Calcula la varianza      
    for (double num : data) {
         standardDeviation += Math.pow(num - mean, 2);       
     }
     standardDeviation /= n - 1;    
     standardDeviation = Math.sqrt(standardDeviation);  
     
     System.out.println("Mean = " + mean);     
     System.out.println("Standard deviation = " + standardDeviation);
  }  
}

Este código primero calcula la media aritmética del conjunto de datos y luego calcula la desviación estándar utilizando la fórmula que se explicó anteriormente. Finalmente, muestra la media aritmética y la desviación estándar en la consola.

El resultado para el conjunto de datos {5, 10, 12, 15, 20} sería:
Media aritmética = 12.0
Desviación estándar = 7.236

## 3

 ## Cálculo del índice de masa corporal (IMC)

El índice de masa corporal (IMC) es una medida que se utiliza para evaluar si una persona tiene un peso saludable en relación con su altura. Se calcula dividiendo el peso de una persona en kilogramos entre el cuadrado de su altura en metros (kg/m²).**

El IMC es una herramienta útil para determinar si una persona tiene un peso saludable, está por debajo de su peso ideal o tiene sobrepeso o obesidad. Aunque el IMC no mide directamente la cantidad de grasa corporal, se ha encontrado que existe una relación entre el IMC y el porcentaje de grasa corporal. Por lo tanto, el IMC se utiliza como un indicador general de la salud y el riesgo de ciertas enfermedades relacionadas con el peso, como la diabetes, la hipertensión y las enfermedades cardiovasculares.

Los valores del IMC se interpretan según las siguientes categorías: Bajo peso: IMC menor a 18,5 Peso normal: IMC entre 18,5 y 24,9 Sobrepeso: IMC entre 25 y 29,9 Obesidad grado 1: IMC entre 30 y 34,9 Obesidad grado 2: IMC entre 35 y 39,9 Obesidad grado 3: IMC igual o mayor a 40

Es importante tener en cuenta que el IMC es una herramienta de evaluación general y que no tiene en cuenta otros factores importantes, como la edad, el género, la composición corporal y la distribución de la grasa corporal. Por lo tanto, es recomendable que una evaluación más completa sea realizada por un profesional de la salud.

Ejemplo en Java de cómo calcular el índice de masa corporal (IMC) de una persona:

import java.util.Scanner;

public class IMC {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      double weight, height, imc;
      
      // Solicita el peso y la altura
      System.out.print("Ingrese su peso en kilogramos: ");
      weight = input.nextDouble();
      System.out.print("Ingrese su altura en metros: ");
      height = input.nextDouble();

      // Calcula el IMC
      imc = weight / (height * height);

      // Muestra el resultado en la consola
      System.out.printf("Su IMC es %.2f", imc);
   }
}

En este programa, primero se solicita al usuario que ingrese su peso en kilogramos y su altura en metros. Luego se calcula el IMC dividiendo el peso entre la altura al cuadrado. Finalmente, se muestra el resultado en la consola con dos decimales utilizando el método printf de la clase System.out.

## 4

## Calcular la cantidad de materiales necesarios para construir una pared de ladrillos

Cálculo de la cantidad de materiales para la construcción: Este ejercicio consiste en calcular la cantidad de materiales necesarios para construir una estructura. Para ello, se debe tener en cuenta las dimensiones de la estructura y la cantidad de materiales necesarios por unidad de área o de volumen. Algunos ejemplos de cálculos de materiales son el cálculo de la cantidad de ladrillos necesarios para construir una pared, o el cálculo de la cantidad de concreto necesario para una losa o columna.**

Ejemplo en Java de cómo calcular la cantidad de materiales necesarios para construir una pared de ladrillos:

import java.util.Scanner;

public class CantidadLadrillos {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      double largo, alto, ancho, areaPared, cantidadLadrillos, largoLadrillo, altoLadrillo, anchoLadrillo;
      
      // Solicita las dimensiones de la pared
      System.out.print("Ingrese el largo de la pared en metros: ");
      largo = input.nextDouble();
      System.out.print("Ingrese el alto de la pared en metros: ");
      alto = input.nextDouble();
      System.out.print("Ingrese el ancho de la pared en metros: ");
      ancho = input.nextDouble();

      // Solicita las dimensiones del ladrillo
      System.out.print("Ingrese el largo del ladrillo en metros: ");
      largoLadrillo = input.nextDouble();
      System.out.print("Ingrese el alto del ladrillo en metros: ");
      altoLadrillo = input.nextDouble();
      System.out.print("Ingrese el ancho del ladrillo en metros: ");
      anchoLadrillo = input.nextDouble();

      // Calcula el área de la pared y del ladrillo
      areaPared = largo * alto;
      double areaLadrillo = largoLadrillo * altoLadrillo;

      // Calcula la cantidad de ladrillos necesarios
      cantidadLadrillos = Math.ceil(areaPared / (areaLadrillo * ancho / anchoLadrillo));

      // Muestra el resultado en la consola
      System.out.printf("Para construir la pared se necesitan %.0f ladrillos.", cantidadLadrillos);
   }
}


En este programa, además de solicitar las dimensiones de la pared, también se solicitan las dimensiones del ladrillo: largo, alto y ancho. Luego se calcula el área del ladrillo multiplicando el largo por el alto.

Para calcular la cantidad de ladrillos necesarios, se divide el área de la pared entre el área de un ladrillo (considerando las dimensiones del ladrillo ingresadas) y el ancho de la pared dividido por el ancho del ladrillo. El resultado se redondea hacia arriba con la función Math.ceil. Finalmente, se muestra el resultado en la consola utilizando el método printf de la clase System.out.

## 5 

## Calcular el movimiento rectilíneo uniforme

El movimiento rectilíneo uniforme (MRU) es un tipo de movimiento en el cual un objeto se mueve en línea recta y a velocidad constante, es decir, su velocidad no cambia en el tiempo. En este tipo de movimiento, la trayectoria del objeto es una línea recta, por lo que su aceleración es cero.**

Un ejemplo común de MRU es un automóvil que se desplaza en una carretera recta y mantiene una velocidad constante durante todo el trayecto. Otro ejemplo es una pelota que cae verticalmente al suelo sin ser afectada por la resistencia del aire.

El MRU es un movimiento importante en la física, ya que permite entender conceptos básicos como la velocidad, la distancia recorrida y el tiempo de desplazamiento. Además, es utilizado como base para otros tipos de movimiento más complejos, como el movimiento rectilíneo uniformemente acelerado (MRUA) y el movimiento circular uniforme (MCU).

**Ejemplo en Java de cómo calcular el movimiento rectilíneo uniforme:**

import java.util.Scanner;

public class MRU {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      double velocidad, tiempo, distancia;
      
      // Solicita la velocidad y el tiempo
      System.out.print("Ingrese la velocidad en metros por segundo: ");
      velocidad = input.nextDouble();
      System.out.print("Ingrese el tiempo en segundos: ");
      tiempo = input.nextDouble();

      // Calcula la distancia recorrida
      distancia = velocidad * tiempo;

      // Muestra el resultado en la consola
      System.out.printf("La distancia recorrida es de %.2f metros.", distancia);
   }
}


En este programa, primero se solicita al usuario que ingrese la velocidad en metros por segundo y el tiempo en segundos.

A continuación, se calcula la distancia recorrida utilizando la fórmula distancia = velocidad x tiempo, donde la velocidad se mide en metros por segundo, el tiempo se mide en segundos y la distancia se mide en metros.

Finalmente, se muestra el resultado en la consola utilizando el método printf de la clase System.out.

## 6 Calcular el movimiento parabólico de un proyectil

El movimiento parabólico de un proyectil es un tipo de movimiento en el cual un objeto es lanzado con una velocidad inicial y se mueve siguiendo una trayectoria curva en forma de parábola debido a la influencia de la gravedad. Este tipo de movimiento se caracteriza por tener tanto una componente horizontal como una vertical.**

Durante el movimiento parabólico de un proyectil, la fuerza de la gravedad actúa sobre el objeto, lo que hace que la trayectoria del proyectil describa una curva en forma de parábola. La velocidad horizontal del proyectil se mantiene constante a lo largo de todo el recorrido, mientras que la velocidad vertical va disminuyendo debido a la fuerza de la gravedad.

Algunos ejemplos de movimiento parabólico de un proyectil son el lanzamiento de una pelota o de un objeto deportivo como un balón de fútbol o una pelota de béisbol. También este tipo de movimiento es muy común en el lanzamiento de cohetes y en otros procesos de lanzamiento de objetos en la industria espacial.

El movimiento parabólico de un proyectil es importante en la física ya que permite entender conceptos como la velocidad, la aceleración, la distancia recorrida y la altura máxima alcanzada por el proyectil. Además, es utilizado en diversas aplicaciones prácticas como en la industria aeroespacial, en la ingeniería de cohetes y en la física de las fuerzas del movimiento.

Espero que esta explicación te haya sido útil para entender qué es el movimiento parabólico de un proyectil.

El ángulo que produce la mayor distancia para un proyectil lanzado con una velocidad inicial dada es de 45 grados. Este ángulo se conoce como el ángulo de lanzamiento óptimo.

La razón por la cual el ángulo de lanzamiento óptimo es de 45 grados es que a este ángulo, la velocidad inicial del proyectil se descompone en dos componentes iguales, una horizontal y otra vertical. La componente horizontal de la velocidad se mantiene constante durante todo el vuelo del proyectil, mientras que la componente vertical disminuye debido a la fuerza de la gravedad.

A medida que el ángulo de lanzamiento se acerca a 0 grados (lanzamiento horizontal), la distancia recorrida por el proyectil disminuye debido a que la componente vertical de la velocidad se vuelve muy pequeña. Por otro lado, a medida que el ángulo de lanzamiento se acerca a 90 grados (lanzamiento vertical), la distancia recorrida también disminuye debido a que la componente horizontal de la velocidad se vuelve muy pequeña.

En resumen, el ángulo de lanzamiento óptimo para maximizar la distancia recorrida por un proyectil lanzado con una velocidad inicial dada es de 45 grados.

**A continuación te presento un ejemplo en Java de cómo calcular el movimiento parabólico de un proyectil:**

import java.util.Scanner;

public class MovimientoParabolico {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      double velocidadInicial, angulo, alturaInicial, tiempo;
      final double gravedad = 9.81;
      
      // Solicita la velocidad inicial, el ángulo y la altura inicial
      System.out.print("Ingrese la velocidad inicial en metros por segundo: ");
      velocidadInicial = input.nextDouble();
      System.out.print("Ingrese el ángulo de lanzamiento en grados: ");
      angulo = input.nextDouble();
      System.out.print("Ingrese la altura inicial en metros: ");
      alturaInicial = input.nextDouble();

      // Calcula la velocidad en los ejes x e y
      double velocidadX = velocidadInicial * Math.cos(Math.toRadians(angulo));
      double velocidadY = velocidadInicial * Math.sin(Math.toRadians(angulo));

      // Calcula el tiempo de vuelo
      tiempo = (2 * velocidadY) / gravedad;

      // Calcula la distancia recorrida
      double distancia = velocidadX * tiempo;

      // Calcula la altura máxima alcanzada
      double alturaMaxima = alturaInicial + (velocidadY * velocidadY) / (2 * gravedad);

      // Muestra los resultados en la consola
      System.out.printf("La distancia recorrida es de %.2f metros.", distancia);
      System.out.printf("La altura máxima alcanzada es de %.2f metros.", alturaMaxima);
      System.out.printf("El tiempo de vuelo es de %.2f segundos.", tiempo);
   }
}


En este programa, primero se solicita al usuario que ingrese la velocidad inicial en metros por segundo, el ángulo de lanzamiento en grados y la altura inicial en metros.

A continuación, se calcula la velocidad en los ejes x e y utilizando las fórmulas:

velocidadX = velocidadInicial * cos(angulo)
velocidadY = velocidadInicial * sin(angulo)

donde velocidadInicial es la velocidad inicial del proyectil, angulo es el ángulo de lanzamiento en grados, cos y sin son las funciones trigonométricas del coseno y el seno, respectivamente.

Luego, se calcula el tiempo de vuelo utilizando la fórmula:

tiempo = (2 * velocidadY) / gravedad
donde gravedad es la constante de la gravedad terrestre, que se toma como 9.81 m/s².
A continuación, se calcula la distancia recorrida utilizando la fórmula:
distancia = velocidadX * tiempo
Finalmente, se calcula la altura máxima alcanzada utilizando la fórmula:
alturaMaxima = alturaInicial + (velocidadY * velocidadY) / (2 * gravedad)
donde alturaInicial es la altura inicial del proyectil.


Se muestra el resultado de la distancia recorrida, la altura máxima alcanzada y el tiempo de vuelo en la consola utilizando el método printf de la clase System.out.

## 7 Cálculo del costo de energía eléctrica de un electrodoméstico

Para calcular el costo de energía eléctrica de un electrodoméstico, se deben seguir los siguientes pasos: Determinar la potencia del electrodoméstico en vatios. Esta información se puede encontrar en la etiqueta del electrodoméstico o en el manual del usuario.

Determinar el tiempo de uso diario del electrodoméstico en horas. Este valor puede variar dependiendo del usuario y del electrodoméstico. Determinar el precio por unidad de energía eléctrica. Este valor se encuentra en la factura de energía eléctrica o se puede consultar con el proveedor de energía eléctrica.

Calcular el consumo diario del electrodoméstico en kilovatios-hora (kWh) multiplicando la potencia del electrodoméstico por el tiempo de uso diario y dividiendo el resultado entre 1000. La fórmula es: consumo_diario = (potencia * tiempo_de_uso_diario) / 1000.

Calcular el consumo mensual del electrodoméstico en kilovatios-hora multiplicando el consumo diario por el número de días del mes. La fórmula es: consumo_mensual = consumo_diario * días_del_mes.

Calcular el costo mensual de energía eléctrica del electrodoméstico multiplicando el consumo mensual por el precio por unidad de energía eléctrica. La fórmula es: costo_mensual = consumo_mensual * precio_por_unidad.

Por ejemplo, si un electrodoméstico tiene una potencia de 1200 vatios y se utiliza durante 4 horas al día, y el precio por unidad de energía eléctrica es de $0.12 por kWh, el cálculo del costo mensual de energía eléctrica sería:

consumo_diario = (1200 * 4) / 1000 = 4.8 kWh
consumo_mensual = 4.8 * 30 = 144 kWh
costo_mensual = 144 * 0.12 = 17.28 dólares

Por lo tanto, el costo mensual de energía eléctrica del electrodoméstico sería de 17.28 dólares.

Ejemplo en Java para calcular el costo de energía eléctrica de un electrodoméstico en base a los datos ingresados por el usuario:

import java.util.Scanner;

public class CalculoCostoEnergiaElectrica {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);

      // Solicitar datos al usuario
      System.out.print("Ingrese la potencia del electrodoméstico (en vatios): ");
      double potencia = input.nextDouble();
      
      System.out.print("Ingrese el tiempo de uso diario (en horas): ");
      double tiempoUsoDiario = input.nextDouble();
      
      System.out.print("Ingrese el precio por kilovatio-hora (en pesos): ");
      double precioKwh = input.nextDouble();
      
      System.out.print("Ingrese el número de días del mes: ");
      int diasDelMes = input.nextInt();
      
      // Cálculo del consumo mensual en kilovatios-hora
      double consumoDiarioKwh = (potencia * tiempoUsoDiario) / 1000;
      double consumoMensualKwh = consumoDiarioKwh * diasDelMes;
      
      // Cálculo del costo mensual de energía eléctrica
      double costoEnergiaElectrica = consumoMensualKwh * precioKwh / 1000; // se divide entre 1000 para convertir el precio por kilovatio-hora en pesos
      
      // Imprimir el resultado en pantalla
      System.out.printf("El costo mensual de energía eléctrica es de: $%,.2f pesos", costoEnergiaElectrica);
   }
}


En este ejemplo, se utiliza la clase Scanner para solicitar al usuario la potencia del electrodoméstico, el tiempo de uso diario, el precio por kilovatio-hora en pesos y el número de días del mes. Luego, se realiza el cálculo del consumo mensual de energía eléctrica en kilovatios-hora y se utiliza la fórmula del costo de energía eléctrica para calcular el costo mensual en pesos. Se divide entre 1000 para convertir el precio por kilovatio-hora en pesos. Finalmente, se imprime el resultado en pantalla con el formato de dos decimales y separador de miles.

## 8 

## Programa en Java para formar subgrupos con integrantes aleatorios de igual cantidad

Programa en Java para formar subgrupos con integrantes aleatorios de igual cantidad a partir de una lista de integrantes:**

import java.util.ArrayList;
import java.util.Collections;
import java.util.Scanner;

public class FormacionSubgrupos {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      ArrayList<String> integrantes = new ArrayList<String>();

      // Solicitar lista de integrantes
      System.out.print("Ingrese la lista de integrantes separados por coma: ");
      String inputIntegrantes = input.nextLine();
      String[] integrantesArray = inputIntegrantes.split(",");
      for (String integrante : integrantesArray) {
         integrantes.add(integrante.trim());
      }

      // Solicitar cantidad de subgrupos
      System.out.print("Ingrese la cantidad de subgrupos que desea formar: ");
      int cantidadSubgrupos = input.nextInt();

      // Formar subgrupos
      int integrantesPorSubgrupo = integrantes.size() / cantidadSubgrupos;
      int integrantesSobrantes = integrantes.size() % cantidadSubgrupos;
      Collections.shuffle(integrantes); // mezclar la lista de integrantes para formar subgrupos aleatorios
      int indiceInicial = 0;
      for (int i = 0; i < cantidadSubgrupos; i++) {
         int integrantesEnSubgrupo = integrantesPorSubgrupo;
         if (integrantesSobrantes > 0) {
            integrantesEnSubgrupo++;
            integrantesSobrantes--;
         }
         int indiceFinal = indiceInicial + integrantesEnSubgrupo;
         ArrayList<String> subgrupo = new ArrayList<String>(integrantes.subList(indiceInicial, indiceFinal));
         indiceInicial = indiceFinal;
         System.out.printf("Subgrupo %d: %s%n", i + 1, subgrupo);
      }
   }
}


En este programa, se utiliza la clase Scanner para solicitar al usuario la lista de integrantes separados por coma y la cantidad de subgrupos que desea formar. Luego, se divide la lista de integrantes en subgrupos de igual tamaño utilizando el operador de módulo para obtener la cantidad de integrantes sobrantes. Se mezcla la lista de integrantes para formar subgrupos aleatorios utilizando el método shuffle de la clase Collections. Finalmente, se imprimen los subgrupos formados en pantalla.

Por ejemplo, si la lista de integrantes es "Juan, Pedro, María, Ana, Luis, Carlos, Diana, Laura" y se desea formar 3 subgrupos, el programa podría imprimir:

Subgrupo 1: [Carlos, Ana, Pedro]
Subgrupo 2: [Diana, Luis, Juan]
Subgrupo 3: [María, Laura]

## 9  

## Programa en Java para asignar aleatoriamente ejercicios a un grupo de personas sin repetir
Programa en Java para asignar aleatoriamente ejercicios a un grupo de personas sin repetir y en igual cantidad, asumiendo que la cantidad de ejercicios es determinada por la lista de personas:


import java.util.ArrayList;
import java.util.Collections;
import java.util.Scanner;

public class AsignacionEjercicios {
   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      ArrayList<String> personas = new ArrayList<String>();

      // Solicitar lista de personas
      System.out.print("Ingrese la lista de personas separadas por coma: ");
      String inputPersonas = input.nextLine();
      String[] personasArray = inputPersonas.split(",");
      for (String persona : personasArray) {
         personas.add(persona.trim());
      }

      // Obtener cantidad de ejercicios
      int cantidadEjercicios = personas.size();

      // Generar lista de ejercicios aleatorios sin repetir
      ArrayList<Integer> numerosEjercicios = new ArrayList<Integer>();
      for (int i = 1; i <= cantidadEjercicios; i++) {
         numerosEjercicios.add(i);
      }
      Collections.shuffle(numerosEjercicios); // mezclar la lista de números de ejercicios para asignarlos aleatoriamente
      ArrayList<String> ejercicios = new ArrayList<String>();
      for (int i = 0; i < cantidadEjercicios; i++) {
         ejercicios.add("Ejercicio " + numerosEjercicios.get(i));
      }

      // Asignar ejercicios a personas
      Collections.shuffle(personas); // mezclar la lista de personas para asignarles ejercicios aleatorios
      for (int i = 0; i < cantidadEjercicios; i++) {
         System.out.printf("%s: %s%n", personas.get(i), ejercicios.get(i));
      }
   }
}



En este programa, se utiliza la clase Scanner para solicitar al usuario la lista de personas separadas por coma. Se obtiene la cantidad de ejercicios a partir de la longitud de la lista de personas y se genera una lista de ejercicios aleatorios sin repetir utilizando el método shuffle de la clase Collections. Luego, se mezcla la lista de personas para asignarles ejercicios aleatorios y se imprimen los resultados en pantalla. Por ejemplo, si se ingresan los siguientes datos:

Ingrese la lista de personas separadas por coma: Juan, Pedro, María, Ana, Luis, Carlos, Diana, Laura
El programa asignará los ejercicios aleatoriamente a las personas y mostrará el resultado en pantalla.






[Siguiente](./sesion11.md)
