<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 9 


## Actividad: Ejecicios de métodos en Java

Resolver en parejas el ejercicio asignado por el docente

Ejercicios de Lógica de Programación

 Calculadora de resistencias eléctricas
Una resistencia eléctrica es un componente electrónico que se utiliza para limitar el flujo de corriente eléctrica en un circuito. Es decir, su función es oponerse al paso de la corriente eléctrica y disminuir su intensidad.

Las resistencias se componen generalmente de un material conductor, como el carbono o el metal, que se coloca en un cuerpo cerámico o de vidrio. El valor de la resistencia (es decir, la cantidad de oposición que ofrece al paso de la corriente eléctrica) se mide en ohms, y depende de la composición del material y de su geometría.

Las resistencias se utilizan en una gran variedad de circuitos electrónicos, tanto en circuitos analógicos como digitales. Algunas de las aplicaciones más comunes de las resistencias incluyen la limitación de corriente en circuitos de alimentación, el ajuste de niveles de voltaje y corriente en circuitos de amplificación, y la medición de corriente y voltaje en circuitos de control y monitoreo.

Calculadora Código de colores - Online

[](https://www.digikey.com/es/resources/conversion-calculators/conversion-calculator-resistor-color-code)

![](image-9.png)

El objetivo de este ejercicio es crear un programa en Java que permita calcular el valor de una resistencia eléctrica a partir de los colores de sus bandas, y que tenga en cuenta la tolerancia.

Para ello, el programa debe solicitar al usuario que elija los colores de las tres bandas de la resistencia a través de un menú de opciones. Los colores disponibles son: negro, marrón, rojo, naranja, amarillo, verde, azul, violeta, gris y blanco.

Una vez que el usuario ha elegido los colores de las tres bandas, el programa debe pedir al usuario que seleccione la tolerancia de la resistencia a través de otro menú de opciones. Las opciones disponibles son: marrón (1%), rojo (2%), oro (5%) y plata (10%). Si el usuario no selecciona ninguna opción válida, se debe utilizar la tolerancia por defecto del 5%.

Con los colores y la tolerancia seleccionados, el programa debe calcular el valor de la resistencia y mostrarlo en la consola, junto con la tolerancia seleccionada.

Para calcular el valor de la resistencia, se debe utilizar la fórmula: valor = ((valor1 10) + valor2) multiplicador, donde valor1 y valor2 son los valores correspondientes a los dos primeros colores elegidos por el usuario (según la tabla de colores), y multiplicador es el valor correspondiente al tercer color elegido por el usuario (también según la tabla de colores). Finalmente, se debe mostrar el valor de la resistencia en ohms y la tolerancia seleccionada.

 Calculadora de la mediana
La mediana es un valor estadístico que se utiliza para describir el centro de un conjunto de datos. Es el valor que se encuentra justo en el medio de un conjunto de datos ordenados de menor a mayor. Es decir, la mediana divide el conjunto de datos en dos partes iguales, donde la mitad de los valores están por encima de la mediana y la otra mitad están por debajo de ella.

Mediana con números impares:

Supongamos este grupo de números: {3, 7, 4, 2, 8}

Ordenarlos de menor a mayor: {2, 3, 4, 7, 8} El número de elementos es impar (5 elementos), por lo que la mediana será el elemento central una vez ordenados. El elemento central es el número 4. Por lo tanto, la mediana de este grupo de números impares es 4.

Mediana con números pares:

Supongamos este otro grupo: {5, 12, 2, 11, 3, 9}

Ordenarlos de menor a mayor: {2, 3, 5, 9, 11, 12} El número de elementos es par (6 elementos), por lo que la mediana será el promedio de los 2 elementos centrales una vez ordenados. Los elementos centrales son el 5 y el 9. El promedio de 5 y 9 es (5 + 9) / 2 = 7 Por lo tanto, la mediana de este grupo de números pares es 7.

La mediana es el elemento central de un grupo ordenado cuando la cantidad de elementos es impar. Y es el promedio de los dos elementos centrales cuando la cantidad es par.

## DESARROLLO

String e2_color1 = "";
String e2_color2 = "";
String e2_color3 = "";
String e2_color4 = "";

class resistorInfo {
    public String value;
    public String Tolerance;
}

public HorizontalLayout algoritmo() {

    VerticalLayout vl1 = new VerticalLayout();
    vl1.setAlignItems(Alignment.CENTER);
    vl1.add(new Image(
            "https://f47ec6e8ca.cbaul-cdnwnd.com/b9a0fcea3766057deaebf52a7956b29e/200000057-e1c97e3bbe/codigo%20de%20colores.png",
            ""));

    VerticalLayout vl2 = new VerticalLayout();
    vl2.setAlignItems(Alignment.CENTER);

    VerticalLayout vl3 = new VerticalLayout();
    vl3.setAlignItems(Alignment.CENTER);

    HorizontalLayout hl = new HorizontalLayout();
    hl.setAlignItems(Alignment.CENTER);
    hl.setWidthFull();

    H2 t1R = new H2("Valor (Ohm)");
    H2 v1R = new H2("0");
    H2 t2R = new H2("Tolerancia (+-)");
    H2 v2R = new H2("0");

    ComboBox<String> comboBox1 = new ComboBox<>("Banda 1");
    comboBox1.setAllowCustomValue(true);
    add(comboBox1);
    comboBox1.setItems("Negro", "Cafe", "Rojo", "Naranja", "Amarillo", "Verde", "Azul", "Morado", "Gris", "Blanco");

    comboBox1.addValueChangeListener(event -> {
        e2_color1 = comboBox1.getValue();
        v1R.setText(calcularResitencia().get(0));
        v2R.setText(calcularResitencia().get(1));
    });

    ComboBox<String> comboBox2 = new ComboBox<>("Banda 2");
    comboBox2.setAllowCustomValue(true);
    add(comboBox2);
    comboBox2.setItems("Negro", "Cafe", "Rojo", "Naranja", "Amarillo", "Verde", "Azul", "Morado", "Gris", "Blanco");

    comboBox2.addValueChangeListener(event -> {
        e2_color2 = comboBox2.getValue();
        v1R.setText(calcularResitencia().get(0));
        v2R.setText(calcularResitencia().get(1));
    });

    ComboBox<String> comboBox3 = new ComboBox<>("Banda 3");
    comboBox3.setAllowCustomValue(true);
    add(comboBox3);
    comboBox3.setItems("Negro", "Cafe", "Rojo", "Naranja", "Amarillo", "Verde", "Azul", "Morado", "Gris", "Blanco");

    comboBox3.addValueChangeListener(event -> {
        e2_color3 = comboBox3.getValue();
        v1R.setText(calcularResitencia().get(0));
        v2R.setText(calcularResitencia().get(1));
    });

    ComboBox<String> comboBox4 = new ComboBox<>("Banda 3");
    comboBox4.setAllowCustomValue(true);
    add(comboBox4);
    comboBox4.setItems("Cafe", "Rojo", "Dorado", "Plateado");

    comboBox4.addValueChangeListener(event -> {
        e2_color4 = comboBox4.getValue();
        v1R.setText(calcularResitencia().get(0));
        v2R.setText(calcularResitencia().get(1));
    });

    vl2.add(comboBox1);
    vl2.add(comboBox2);
    vl2.add(comboBox3);
    vl2.add(comboBox4);
    vl3.add(t1R);
    vl3.add(v1R);
    vl3.add(t2R);
    vl3.add(v2R);
    hl.add(vl1);
    hl.add(vl2);
    hl.add(vl3);
    return hl;
}

private ArrayList<String> calcularResitencia() {

    ArrayList<String> result = new ArrayList<>();
    int c1 = convertirColor(e2_color1);
    int c2 = convertirColor(e2_color2);
    int c3 = convertirColor(e2_color3);
    int c4 = convertirColor(e2_color4);

    if (c1 == 10 || c2 == 10 || c3 == 10 || c4 == 10) {
        result.add("Null");
        result.add("Null");
        return result;
    }

    double rValue = (c1 * 10) + c2;

    switch (c3) {
        case 0:
            rValue *= 1;
            break;
        case 1:
            rValue *= 10;
            break;
        case 2:
            rValue *= 100;
            break;
        case 3:
            rValue *= 1000;
            break;
        case 4:
            rValue *= 10000;
            break;
        case 5:
            rValue *= 100000;
            break;
        case 6:
            rValue *= 1000000;
            break;
        case 7:
            rValue /= 10;
            break;
        case 8:
            rValue /= 100;
            break;
        default:
            break;
    }

    double rTolerance = 0;

    switch (c4) {
        case 0:
            rTolerance = rValue * 0.01;
            break;
        case 1:
            rTolerance = rValue * 0.02;
            break;
        case 2:
            rTolerance = rValue * 0.05;
            break;
        case 3:
            rTolerance = rValue * 0.1;
            break;
    }

    String string_rValue = "";
    if (rValue > 1000) {
        rValue /= 1000;
        DecimalFormat df1 = new DecimalFormat("0.0");
        string_rValue = df1.format(rValue);
        string_rValue += "K";
    } else {
        DecimalFormat df1 = new DecimalFormat("0");
        string_rValue = df1.format(rValue);
    }

    DecimalFormat df2 = new DecimalFormat("0.0");
    String string_rTolerance = df2.format(rTolerance);

    result.add(string_rValue);
    result.add(string_rTolerance);
    return result;

}

private int convertirColor(String color) {
    int res = 0;
    switch (color) {
        case "Negro":
            res = 0;
            break;
        case "Cafe":
            res = 1;
            break;
        case "Rojo":
            res = 2;
            break;
        case "Naranja":
        case "Dorado":
            res = 3;
            break;
        case "Amarillo":
        case "Plateado":
            res = 4;
            break;
        case "Verde":
            res = 5;
            break;
        case "Azul":
            res = 6;
            break;
        case "Morado":
            res = 7;
            break;
        case "Gris":
            res = 8;
            break;
        case "Blanco":
            res = 9;
            break;
        default:
            res = 10;
            break;
    }
    return res;
}

[Siguiente](./sesion10.md)
