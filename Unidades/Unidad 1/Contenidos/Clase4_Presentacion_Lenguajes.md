---
layout: default
title: Clase 4
---

<div align="center">

<!-- Botón para volver a la Unidad 1 -->
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
    margin-bottom: 20px;
">
⬅️ Volver
</a>

</div>

# 💻 Clase 4 — Programación en Lenguaje C

---

## 📄 Descripción

En esta clase vimos la introducción a la programación en C, su relación con algoritmos y pseudocódigo, y la importancia de las buenas prácticas en la codificación.

Se abordaron los siguientes conceptos:

1. **Introducción a C**: Lenguaje fundamental para aprender programación. Transformación de algoritmos en código ejecutable.

2. **Algoritmo y Pseudocódigo**: Secuencia lógica de pasos para resolver problemas antes de codificar.

```pseudocode
Inicio
    Leer largo
    Leer ancho
    area <- largo * ancho
    Mostrar area
Fin
```

3. **Uso de librerías en C**: Funciones predefinidas para entrada/salida y operaciones matemáticas. Librería estándar `stdio.h`.

```c
#include <stdio.h>

int main() {
    int numero;
    printf("Ingrese un número: ");
    scanf("%d", &numero);
    printf("El número ingresado es %d\n", numero);
    return 0;
}
```

4. **Función principal main()**: Punto de entrada de todo programa en C.

```c
int main() {
    // Código de inicio
    return 0;
}
```

5. **Comentarios en C**:

```c
// Comentario de línea
/* Comentario
   de varias líneas */
```

6. **Palabras reservadas y declaración de variables**:

```c
int a, b;
float promedio;
char respuesta = 'S';
char nombre[20] = "Juan";
```

7. **Entrada y salida de datos**:

```c
int edad;
printf("Ingrese su edad: ");
scanf("%d", &edad);
printf("Tu edad es %d\n", edad);
```

8. **Cálculos y operaciones aritméticas**:

```c
int suma = a + b;
float resultado = (float) numerator / denominator;
```

---

## 🧩 Actividad

**Ejercicio práctico:**  
Realizar un programa que, tomando una cantidad expresada en metros, la transforme a kilómetros, centímetros y milímetros.

```pseudocode
Inicio
    Leer metros
    kilometros <- metros / 1000
    centimetros <- metros * 100
    milimetros <- metros * 1000
    Mostrar "Kilómetros: ", kilometros
    Mostrar "Centímetros: ", centimetros
    Mostrar "Milímetros: ", milimetros
Fin
```

```c
#include <stdio.h>

int main() {
    float metros, kilometros, centimetros, milimetros;

    printf("Ingrese cantidad en metros: ");
    scanf("%f", &metros);

    kilometros = metros / 1000;
    centimetros = metros * 100;
    milimetros = metros * 1000;

    printf("Kilómetros: %.2f\n", kilometros);
    printf("Centímetros: %.2f\n", centimetros);
    printf("Milímetros: %.2f\n", milimetros);

    return 0;
}
```

```terminal
Ingrese cantidad en metros:
> 150
Kilómetros: 0.15
Centímetros: 15000.00
Milímetros: 150000.00
```

> Esta actividad permite practicar entrada/salida de datos, conversiones y operaciones aritméticas en C.

---

<div align="center" style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin-bottom: 20px;">

<!-- Botón Clase anterior -->
<a href="./Clase3_Presentacion_Herramientas" style="
    background: linear-gradient(90deg, #F4511E, #FF7043);
    color: white;
    padding: 12px 25px;
    text-decoration: none;
    font-size: 16px;
    font-weight: bold;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.2);
    display: inline-block;
">
⬅️ Clase 3
</a>

</div>

<div align="center">

<!-- Botón para volver a la Unidad 1 -->
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
⬅️ Volver
</a>

</div>

