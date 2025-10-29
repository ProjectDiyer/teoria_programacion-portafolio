---
layout: default
title: Códigos en C
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

---

# 💻 Códigos en Lenguaje C realizados

En esta sección se recopilan los programas desarrollados en **lenguaje C**, junto con su descripción, propósito y código fuente.

---

## 🔹 1 — Hola Mundo

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

## 🔹 2 — Suma de dos números

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

### 🧩 Tabla de prueba de escritorio

| **Caso** | **Entrada (numero1)** | **Entrada (numero2)** | **Proceso**               | **Salida**                                |
|-----------|----------------------:|----------------------:|---------------------------|-------------------------------------------|
| 1         | 5                    | 3                    | suma = 5 + 3 = 8          | La suma de 5.00 y 3.00 es: 8.00           |
| 2         | 10.5                 | 4.3                  | suma = 10.5 + 4.3 = 14.8  | La suma de 10.50 y 4.30 es: 14.80         |
| 3         | -2                   | 6                    | suma = -2 + 6 = 4         | La suma de -2.00 y 6.00 es: 4.00          |
| 4         | 0                    | 0                    | suma = 0 + 0 = 0          | La suma de 0.00 y 0.00 es: 0.00           |
| 5         | 150.25               | 349.75               | suma = 150.25 + 349.75 = 500.00 | La suma de 150.25 y 349.75 es: 500.00 |

---

## 🔹 3 — Doble y triple de un número

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

### 🧩 Tabla de prueba de escritorio

| **Caso** | **Entrada (numero)** | **Proceso**                             | **Salida**                                               |
|-----------|---------------------:|------------------------------------------|----------------------------------------------------------|
| 1         | 2                   | doble = 2 * 2 = 4<br>triple = 2 * 3 = 6  | El doble de 2.0 es: 4.0<br>El triple de 2.0 es: 6.0      |
| 2         | 5.5                 | doble = 5.5 * 2 = 11<br>triple = 5.5 * 3 = 16.5 | El doble de 5.5 es: 11.0<br>El triple de 5.5 es: 16.5   |
| 3         | -3                  | doble = -3 * 2 = -6<br>triple = -3 * 3 = -9 | El doble de -3.0 es: -6.0<br>El triple de -3.0 es: -9.0 |
| 4         | 0                   | doble = 0 * 2 = 0<br>triple = 0 * 3 = 0  | El doble de 0.0 es: 0.0<br>El triple de 0.0 es: 0.0      |
| 5         | 150                 | doble = 150 * 2 = 300<br>triple = 150 * 3 = 450 | El doble de 150.0 es: 300.0<br>El triple de 150.0 es: 450.0 |

---

## 🔹4 — Cálculo de aceleración

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

### 🧩 Tabla de prueba de escritorio

| **Caso** | **Velocidad Inicial (m/s)** | **Velocidad Final (m/s)** | **Tiempo (s)** | **Proceso**                                         | **Salida**                       |
|-----------|----------------------------|---------------------------|----------------|----------------------------------------------------|----------------------------------|
| 1         | 0                          | 10                        | 2              | aceleracion = (10 - 0) / 2 = 5                     | La aceleracion es: 5.00 m/s²    |
| 2         | 5                          | 15                        | 5              | aceleracion = (15 - 5) / 5 = 2                     | La aceleracion es: 2.00 m/s²    |
| 3         | 20                         | 0                         | 4              | aceleracion = (0 - 20) / 4 = -5                    | La aceleracion es: -5.00 m/s²   |
| 4         | 3                          | 3                         | 10             | aceleracion = (3 - 3) / 10 = 0                     | La aceleracion es: 0.00 m/s²    |
| 5         | 12                         | 24                        | 6              | aceleracion = (24 - 12) / 6 = 2                    | La aceleracion es: 2.00 m/s²    |


---

## 🔹 Ejemplo 5 — Separar parte entera y decimal

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

### 🧩 Tabla de prueba de escritorio

| **Caso** | **Entrada (numero)** | **Proceso**                                             | **Salida**                          |
|-----------|---------------------|--------------------------------------------------------|-------------------------------------|
| 1         | 12.34               | parte_entera = 12<br>parte_decimal = 0.34             | Parte entera: 12<br>Parte decimal: 0.34 |
| 2         | -5.78               | parte_entera = -5<br>parte_decimal = -0.78            | Parte entera: -5<br>Parte decimal: -0.78 |
| 3         | 0.99                | parte_entera = 0<br>parte_decimal = 0.99              | Parte entera: 0<br>Parte decimal: 0.99 |
| 4         | 100.0               | parte_entera = 100<br>parte_decimal = 0.00            | Parte entera: 100<br>Parte decimal: 0.00 |
| 5         | -0.25               | parte_entera = 0<br>parte_decimal = -0.25             | Parte entera: 0<br>Parte decimal: -0.25 |

---

## 🔹 Ejemplo 6 — Distancia entre dos puntos

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

### 🧩 Tabla de prueba de escritorio

| **Caso** | **Punto A (x1, y1)** | **Punto B (x2, y2)** | **Proceso**                                                        | **Salida**                         |
|-----------|---------------------|---------------------|-------------------------------------------------------------------|------------------------------------|
| 1         | (0, 0)              | (3, 4)              | distancia = sqrt((3-0)² + (4-0)²) = sqrt(9 + 16) = 5              | La distancia entre los puntos es: 5.00 |
| 2         | (1, 2)              | (4, 6)              | distancia = sqrt((4-1)² + (6-2)²) = sqrt(9 + 16) = 5              | La distancia entre los puntos es: 5.00 |
| 3         | (-2, -3)            | (1, 1)              | distancia = sqrt((1+2)² + (1+3)²) = sqrt(9 + 16) = 5              | La distancia entre los puntos es: 5.00 |
| 4         | (0, 0)              | (0, 0)              | distancia = sqrt((0-0)² + (0-0)²) = sqrt(0 + 0) = 0               | La distancia entre los puntos es: 0.00 |

---

## 🔹 7 — Conversión de metros a otras unidades

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

### 🧩 Tabla de prueba de escritorio

| **Caso** | **Entrada (metros)** | **Proceso**                                                        | **Salida**                                                        |
|-----------|--------------------:|-------------------------------------------------------------------|-------------------------------------------------------------------|
| 1         | 1                  | kilometros = 1 / 1000 = 0.001<br>centimetros = 1 * 100 = 100<br>milimetros = 1 * 1000 = 1000 | 1.00 metros son:<br>0.00 kilometros<br>100.00 centimetros<br>1000.00 milimetros |
| 2         | 0.5                | kilometros = 0.5 / 1000 = 0.0005<br>centimetros = 0.5 * 100 = 50<br>milimetros = 0.5 * 1000 = 500 | 0.50 metros son:<br>0.00 kilometros<br>50.00 centimetros<br>500.00 milimetros |
| 3         | 123                | kilometros = 123 / 1000 = 0.123<br>centimetros = 123 * 100 = 12300<br>milimetros = 123 * 1000 = 123000 | 123.00 metros son:<br>0.12 kilometros<br>12300.00 centimetros<br>123000.00 milimetros |
| 4         | 0                  | kilometros = 0 / 1000 = 0<br>centimetros = 0 * 100 = 0<br>milimetros = 0 * 1000 = 0 | 0.00 metros son:<br>0.00 kilometros<br>0.00 centimetros<br>0.00 milimetros |

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
