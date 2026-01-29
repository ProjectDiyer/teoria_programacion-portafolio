---
layout: default
title: Recurso 2
liquid: false
---

<div align="center">

<a href="../Unidad3" style="
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

# 📘 Recurso 2: Estructuras de Datos Estáticas en C

## 1. Contexto y Temática General
Este recurso corresponde a la asignatura de **Computación**, Unidad 3, enfocada en la **Programación Modular** y las **Estructuras de Datos Estáticas**.  
El objetivo es comprender cómo organizar y manipular la información utilizando arreglos y cadenas en el lenguaje C.

---

## 2. Estructuras de Datos Estáticas Básicas
Las estructuras de datos estáticas permiten almacenar información de forma ordenada y eficiente.  
En esta unidad se estudian principalmente:

- Arreglos (arrays)
- Cadenas de caracteres (strings)

---

## 3. Arreglos (Arrays)

- Un arreglo es una estructura que almacena varios elementos del mismo tipo.
- Cada elemento se identifica mediante un índice.
- Los índices comienzan siempre en cero (0).

---

## 4. Tipos de Arreglos

### 4.1 Arreglos Unidimensionales
- También llamados vectores o listas.
- Poseen una sola dimensión.
- Ejemplo en C:
  `int numeros[5];`

### 4.2 Arreglos Bidimensionales
- Conocidos como matrices.
- Se organizan en filas y columnas.
- Ejemplo en C:
  `int matriz[filas][columnas];`

### 4.3 Arreglos Tridimensionales
- Incluyen profundidad, filas y columnas.
- Ejemplo en C:
  `int cubo[x][y][z];`

---

## 5. Cadenas o Strings en C

- Son arreglos de caracteres.
- Finalizan con el carácter nulo `\0`.
- Se trabaja con la librería `string.h`.

Funciones comunes:
- `strcpy`
- `strlen`
- `strcmp`
- `strcat`

---

## 6. Ejemplo Práctico en Lenguaje C

A continuación se presenta un programa completo que utiliza:
- Arreglo unidimensional
- Arreglo bidimensional
- Arreglo tridimensional
- Manejo de cadenas

{% raw %}
```c
#include <stdio.h>
#include <string.h>

int main() {

    /* ARREGLO UNIDIMENSIONAL */
    int numeros[5] = {10, 20, 30, 40, 50};
    printf("Arreglo Unidimensional:\n");
    for (int i = 0; i < 5; i++) {
        printf("numeros[%d] = %d\n", i, numeros[i]);
    }

    /* ARREGLO BIDIMENSIONAL */
    int matriz[2][3] = {
        {1, 2, 3},
        {4, 5, 6}
    };

    printf("\nArreglo Bidimensional:\n");
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 3; j++) {
            printf("matriz[%d][%d] = %d  ", i, j, matriz[i][j]);
        }
        printf("\n");
    }

    /* ARREGLO TRIDIMENSIONAL */
    int cubo[2][2][2] = {
        {{1, 2}, {3, 4}},
        {{5, 6}, {7, 8}}
    };

    printf("\nArreglo Tridimensional:\n");
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 2; j++) {
            for (int k = 0; k < 2; k++) {
                printf("cubo[%d][%d][%d] = %d\n", i, j, k, cubo[i][j][k]);
            }
        }
    }


    return 0;
}
{% endraw %}
```
---

<div align="center" style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin-bottom: 20px;">

<!-- Botón Recurso  siguiente -->
<a href="./Recurso1" style="
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
⬅️ Recurso 1
</a>

</div>

<div align="center">
<!-- Botón para volver a la Unidad 3 -->
<a href="../Unidad3" style="
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

