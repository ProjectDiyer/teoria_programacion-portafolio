
---
layout: default
title: Códigos en C — Unidad 3
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
    margin-top: 20px;
">
⬅️ Volver a Unidad 3
</a>
</div>

---

# 💻 Códigos en Lenguaje C — Unidad 3

En esta sección se presentan programas desarrollados en **lenguaje C**, aplicando los conceptos de **programación modular** y **estructuras de datos estáticas**, correspondientes a la **Unidad 3**.

---

## 🔹 1 — Programa modular para cálculo de promedio final

**Archivo:** `promedio_modular.c`  
**Descripción:** Calcula el promedio final del estudiante utilizando funciones para ACD, APE, AA y ES, aplicando programación modular.

**Código:**
```c
#include <stdio.h>

float calcularPromedioFinal(int nu);
float calcularACD();
float calcularAPE();
float calcularAA();
float calcularES();

int main() {

    int NUMEROUNIDADES = 3;
    float promedioFinal;
    char *Estado;

    promedioFinal = calcularPromedioFinal(NUMEROUNIDADES);

    if (promedioFinal >= 7)
        Estado = "Aprobado";
    else if (promedioFinal >= 2.5)
        Estado = "Supletorio";
    else
        Estado = "Reprobado";

    printf("-------------------------------------\n");
    printf("Promedio final: %.2f\n", promedioFinal);
    printf("Estado: %s\n", Estado);
    printf("-------------------------------------\n");

    return 0;
}

float calcularPromedioFinal(int nu) {
    float suma = 0;
    for (int i = 1; i <= nu; i++) {
        printf("\nUNIDAD %d\n", i);
        suma += calcularACD() + calcularAPE() + calcularAA() + calcularES();
    }
    return suma / nu;
}

float calcularACD() {
    int n;
    float nota, suma = 0;
    printf("NOTA ACD\nIngrese numero de actividades: ");
    scanf("%d", &n);

    for (int i = 1; i <= n; i++) {
        do {
            printf("Actividad %d: ", i);
            scanf("%f", &nota);
        } while (nota < 0 || nota > 10);
        suma += nota;
    }
    return (suma / n) * 0.20;
}

float calcularAPE() {
    int n;
    float nota, suma = 0;
    printf("NOTA APE\nIngrese numero de actividades: ");
    scanf("%d", &n);

    for (int i = 1; i <= n; i++) {
        do {
            printf("Actividad %d: ", i);
            scanf("%f", &nota);
        } while (nota < 0 || nota > 10);
        suma += nota;
    }
    return (suma / n) * 0.25;
}

float calcularAA() {
    int n;
    float nota, suma = 0;
    printf("NOTA AA\nIngrese numero de actividades: ");
    scanf("%d", &n);

    for (int i = 1; i <= n; i++) {
        do {
            printf("Actividad %d: ", i);
            scanf("%f", &nota);
        } while (nota < 0 || nota > 10);
        suma += nota;
    }
    return (suma / n) * 0.20;
}

float calcularES() {
    float portafolio, abp;

    do {
        printf("Nota Portafolio: ");
        scanf("%f", &portafolio);
    } while (portafolio < 0 || portafolio > 10);

    do {
        printf("Nota ABP: ");
        scanf("%f", &abp);
    } while (abp < 0 || abp > 10);

    return ((portafolio * 0.4) + (abp * 0.6)) * 0.35;
}
```

## 🔹 2 — Paso de parámetros por referencia (videojuegos)

**Archivo:** `videojuegos.c`  
**Descripción:** Calcula el total recaudado por alquiler de consolas utilizando funciones y paso de parámetros por referencia.

**Código:**
```c
#include <stdio.h>

void calcularValorCliente(float *total);
void calcularValorRecaudado(int numClientes, float *total);

int main() {
    int numClientes;
    float total = 0;

    printf("Ingrese el numero de clientes: ");
    scanf("%d", &numClientes);

    calcularValorRecaudado(numClientes, &total);

    printf("Total recaudado: %.2f\n", total);
    return 0;
}

void calcularValorRecaudado(int numClientes, float *total) {
    for (int i = 1; i <= numClientes; i++) {
        calcularValorCliente(total);
    }
}

void calcularValorCliente(float *total) {
    int consola;
    float horas, precio;

    do {
        printf("Consola (1=PlayStation, 2=Xbox, 3=Nintendo): ");
        scanf("%d", &consola);
    } while (consola < 1 || consola > 3);

    printf("Horas: ");
    scanf("%f", &horas);

    if (consola == 1) precio = horas * 2.5;
    else if (consola == 2) precio = horas * 2.0;
    else precio = horas * 1.5;

    printf("Valor a pagar: %.2f\n", precio);
    *total += precio;
}

```

## 🔹 3 — Arreglo unidimensional (vector)

**Código:**
```c
#include <stdio.h>

int main()
{
    int lista[5] = {8, 10, 7, 5, 3};

    printf("Arreglo unidimensional:\n");
    for (int i = 0; i < 5; i++)
    {
        printf("Elemento en la posicion %d: %d\n", i, lista[i]);
    }

    return 0;
}
```

## 🔹 4 — Arreglo bidimensional (matriz)

**Código:**
```c
#include <stdio.h>

int main()
{
    int matriz[3][4] = {
        {1, 5, 8, 3},
        {2, 3, 6, 8},
        {5, 7, 9, 4}
    };

    printf("Elementos de la matriz:\n");
    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 4; j++)
        {
            printf("Elemento en la posicion [%d][%d]: %d\n", i, j, matriz[i][j]);
        }
        printf("\n");
    }

    printf("Matriz completa:\n");
    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 4; j++)
        {
            printf("%d ", matriz[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```

## 🔹 5 — Arreglo tridimensional

**Código:**
```c
#include <stdio.h>

int main()
{
    int arreglotridimensional[2][3][2];

    // Asignar valores capa 1
    arreglotridimensional[0][0][0] = 1;
    arreglotridimensional[0][0][1] = 2;

    arreglotridimensional[0][1][0] = 3;
    arreglotridimensional[0][1][1] = 4;

    arreglotridimensional[0][2][0] = 5;
    arreglotridimensional[0][2][1] = 6;

    // Asignar valores capa 2
    arreglotridimensional[1][0][0] = 7;
    arreglotridimensional[1][0][1] = 8;

    arreglotridimensional[1][1][0] = 9;
    arreglotridimensional[1][1][1] = 10;

    arreglotridimensional[1][2][0] = 11;
    arreglotridimensional[1][2][1] = 12;

    // Mostrar valores
    printf("Arreglo tridimensional:\n");
    for (int i = 0; i < 2; i++)
    {
        printf("Capa %d:\n", i + 1);
        for (int j = 0; j < 3; j++)
        {
            for (int k = 0; k < 2; k++)
            {
                printf("Elemento en la posicion [%d][%d][%d]: %d\n",
                       i, j, k, arreglotridimensional[i][j][k]);
            }
            printf("\n");
        }
        printf("\n");
    }

    return 0;
}
```
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
  margin-top: 20px; "> 
  
  ⬅️ Volver
  
  </a> 
  
  </div>
