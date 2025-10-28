---
layout: default
title: Códigos en C
---

<div align="center">

# 💻 Códigos en Lenguaje C realizados

En esta sección se recopilan los programas desarrollados en **lenguaje C**, junto con su descripción, propósito y código fuente.

---

## 🔹 Ejemplo 1 — Hola Mundo

**Archivo:** `hola_mundo.c`  
**Descripción:** Programa sencillo que muestra en pantalla el mensaje "Hola Mundo".

**Código:**
```c
#include <stdio.h>

int main() {
    printf("Hola Mundo\n");
    return 0;
}
```

---

## 🔹 Ejemplo 2 — Lectura de nombres completos

**Archivo:** `nombres.c`  
**Descripción:** Programa que muestra tres formas de manejar cadenas en C para ingresar y mostrar nombres completos:  
1. Uso de un arreglo de caracteres estático.  
2. Uso de memoria dinámica con puntero y `malloc`.  
3. Uso de un puntero a cadena de solo lectura.

**Código:**
```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>

int main(){

    char nombresCompletos[50];

    //Opcion 1, arreglo de caracteres
    printf("Ingrese sus nombres completos:\n ");
    scanf("%[^\n]s", nombresCompletos);
    getchar(); // Limpiar el buffer de entrada
    printf("Sus nombres completos ingresados son: %s\n", nombresCompletos);

    //Opcion 2, puntero al inicio de una cadena
    char * nombresCompletos = malloc(50 * sizeof(char)); //Reserva memoria dinamica

    printf("Ingrese sus nombres completos:\n ");
    scanf("%[^\n]s", nombresCompletos);
    getchar();
    printf("Sus nombres completos ingresados son: %s\n", nombresCompletos);

    //Opcion 3, solo lectura
    char * nombresCompletos = "Diyer Torres";
    printf("Ingrese sus nombres completos:\n ");
    scanf("%[^\n]s", nombresCompletos);
    getchar();
    printf("Sus nombres completos ingresados son: %s\n", nombresCompletos);

    return 0;
}
```

---

## 🔹 Ejemplo 3 — Suma de dos números con decimales

**Archivo:** `suma_float.c`  
**Descripción:** Programa que solicita al usuario dos números decimales (tipo `float`) y muestra su suma con dos cifras decimales.

**Código:**
```c
#include <stdio.h>
#include <string.h>

int main(){

    float numero1, numero2, suma;

    printf("Ingrese el primer numero:\n");
    scanf("%f", &numero1);
    printf("Ingrese el segundo numero:\n");
    scanf("%f", &numero2);
    suma = numero1 + numero2;
    printf("La suma de %.2f y %.2f es: %.2f\n", numero1, numero2, suma);

    return 0;
}
```

---

## 🔹 Ejemplo 4 — Doble y triple de un número

**Archivo:** `doble_triple.c`  
**Descripción:** Programa que solicita un número al usuario y calcula su doble y su triple, mostrando ambos resultados.

**Código:**
```c
#include <stdio.h>

int main() {
    
    float numero,doble,triple;

    printf("Ingtresa un numero: ");
    scanf("%f", &numero);

    doble = numero * 2;
    triple = numero * 3;

    printf("El doble de %.1f es: %.1f\n", numero, doble);
    printf("El tripre de %.1f es: %.1f\n", numero, triple);

    return 0;
}
```

---

## 🔹 Ejemplo 5 — Conversión de pies a otras unidades

**Archivo:** `conversion_pies.c`  
**Descripción:** Programa que convierte una cantidad dada en pies a yardas, pulgadas, centímetros y metros, mostrando los resultados equivalentes.

**Código:**
```c
#include <stdio.h>

int main() { 

    float pies, yardas, pulgadas, centimetros, metros;

    printf("Ingresa la cantidad en pies: ");
    scanf("%f", &pies);

    yardas = pies / 3.0;
    pulgadas = pies * 12.0;
    centimetros = pulgadas * 2.54;
    metros = centimetros/100;

    printf("%.2f pies son equivalentes a:\n", pies);
    printf("%.2f yardas\n", yardas);
    printf("%.2f pulgadas\n", pulgadas);
    printf("%.2f centimetros\n", centimetros);
    printf("%.2f metros\n", metros);
    
    return 0;

}
```

---

## 🔹 Ejemplo 6 — Cálculo de aceleración

**Archivo:** `aceleracion.c`  
**Descripción:** Programa que calcula la aceleración de un objeto utilizando la fórmula física \( a = \frac{v_f - v_i}{t} \), donde se ingresan la velocidad inicial, la velocidad final y el tiempo.

**Código:**
```c
#include <stdio.h>
int main(){
    float velocidadI, velocidadF, tiempo, aceleracion;

    printf("Ingrese la velocidad inicial (m/s): ");
    scanf("%f", &velocidadI);

    printf("Ingrese la velocidad final (m/s): ");
    scanf("%f", &velocidadF);

    printf("Ingrese el tiempo (s):");
    scanf("%f", &tiempo);

    aceleracion = (velocidadF-velocidadI)/tiempo;

    printf("La aceleracion es: %.2f m/s^2\n", aceleracion);

    return 0;
}
```

---

## 🔹 Ejemplo 7 — Separar parte entera y decimal

**Archivo:** `parte_entera_decimal.c`  
**Descripción:** Programa que separa la parte entera y la parte decimal de un número ingresado por el usuario utilizando la función `modf()` de la biblioteca `<math.h>`.

**Código:**
```c
#include <stdio.h>
#include <math.h>

int main() {
    double numero, parte_entera, parte_decimal;

    printf("Ingrese un numero decimal: ");
    scanf("%lf", &numero);

    parte_decimal = modf(numero, &parte_entera);

    printf("Parte entera: %.0f\n", parte_entera);
    printf("Parte decimal: %.2f\n", parte_decimal);

    return 0;
}
```

---

## 🔹 Ejemplo 8 — Distancia entre dos puntos

**Archivo:** `distancia_puntos.c`  
**Descripción:** Programa que calcula la distancia entre dos puntos en el plano cartesiano utilizando la fórmula de distancia y la función `sqrt()` de la biblioteca `<math.h>`.

**Código:**
```c
#include <stdio.h>
#include <math.h>

int main(){

    float x1, y1, x2, y2, distancia;

    printf("Ingrese los datos del punto A (x1, y1):\n");
    scanf("%f %f", &x1, &y1);

    printf("Ingrese los datos del punto B (x2, y2):\n");
    scanf("%f %f", &x2, &y2);

    distancia = sqrt((x2-x1)*(x2-x1) + (y2-y1)*(y2-y1));

    printf("La distancia entre los puntos es: %.2f\n", distancia);

    return 0;
}
```

---

## 🔹 Ejemplo 9 — Conversión de metros a otras unidades

**Archivo:** `conversion_metros.c`  
**Descripción:** Programa que convierte una cantidad en metros a kilómetros, centímetros y milímetros, mostrando los resultados con dos decimales.

**Código:**
```c
#include <stdio.h>

int main(){
    float metros, kilometros, centimetros, milimetros;

    printf("Ingrese la cantidad en metros: ");
    scanf("%f", &metros);

    kilometros = metros / 1000;
    centimetros = metros * 100;
    milimetros = metros * 1000;

    printf("%.2f metros son:\n", metros);
    printf("%.2f kilometros\n", kilometros);
    printf("%.2f centimetros\n", centimetros);
    printf("%.2f milimetros\n", milimetros);

    return 0;
}
```

---

## 🔹 Ejemplo 10 — Cálculo de la nota necesaria para aprobar

**Archivo:** `nota_final.c`  
**Descripción:** Programa que calcula la nota necesaria en el tercer certamen para aprobar una asignatura, considerando el promedio ponderado entre certámenes y laboratorio.

**Código:**
```c
#include <stdio.h> // Incluye la librería estándar de entrada y salida

int main() {
    float C1, C2, C3, NL, NC, NF; // Declaración de variables para las notas

    // Obtención de datos
    printf("Ingrese la nota del primer certamen:\n ");
    scanf("%f", &C1);

    printf("Ingrese la nota del segundo certamen:\n ");
    scanf("%f", &C2); 

    printf("Ingrese la nota del laboratorio:\n");
    scanf("%f", &NL); 

    NF = 60; // Se define la nota final deseada
	
    // Se despeja NC de la fórmula:
    NC = (NF - (NL * 0.3)) / 0.7; 

    // Se calcula la nota necesaria en el tercer certamen:
    C3 = 3 * NC - C1 - C2;
   
    // Muestra la nota que se necesita obtener en el tercer certamen
    printf("La nota necesaria en el tercer certamen es: %.2f\n", C3);
    printf("Nota: Si el resultado es negativo, significa que ya aprueba con las notas actuales.\n");

    return 0; // Fin del programa
}
```

---

<div align="center">

<a href="../Unidad1" style="
    background: linear-gradient(90deg, #2E7D32, #66BB6A);
    color: white;
    padding: 12px 30px;
    text-decoration: none;
    font-size: 18px;
    font-weight: bold;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.2);
    display: inline-block;
    margin-top: 20px;
">
⬅️ Volver al Índice
</a>

</div>
