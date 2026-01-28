---
layout: default
title: Recurso 1
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

# 🧠 Recurso 1 — Programación Modular

---

## 📄 Contexto y Objetivo del Documento

Este recurso pertenece a la **Facultad de Energía, Industrias y Recursos Naturales No Renovables**, en la asignatura de **Computación**, correspondiente a la **Unidad 3**.

El objetivo principal es enseñar la **programación modular**, mostrando cómo dividir programas complejos en módulos pequeños, claros y reutilizables, facilitando su comprensión, mantenimiento y organización.

---

## 🔹 1. Programación Modular

La **programación modular** consiste en dividir un programa grande en subprogramas o módulos, reduciendo su complejidad.

Este proceso permite dividir el programa en:
- Procesos  
- Funciones  
- Rutinas  
- Subrutinas 

---

## 🔹 2. Funciones

Una **función** es un conjunto de sentencias que realiza una tarea específica.

- Pueden ser funciones del lenguaje o definidas por el programador.
- No se ejecutan de forma independiente.
- Siempre están relacionadas con el programa principal (`main`).
- Pueden llamarse entre sí aplicando diseño **top-down**.

---

## 🔹 3. Estructura de una Función

Una función se compone de:
- **Cabecera:** tipo de retorno, nombre y parámetros.
- **Cuerpo:** instrucciones encerradas entre llaves y la sentencia `return` si aplica.

---

## 🔹 4. Tipos de Funciones

- **Funciones sin retorno:** ejecutan tareas sin devolver valores.
- **Funciones con retorno:** devuelven un resultado al programa principal.

---

## 🔹 5. Parámetros en Funciones

- **Paso por valor:** no modifica la variable original.
- **Paso por referencia:** modifica la variable original usando punteros.

---

## 🔹 6. Ventajas de la Programación Modular

- Reduce la complejidad del programa.
- Permite reutilizar código.
- Facilita la detección de errores.
- Mejora la claridad del código.

---

## 🔹 7. Diseño Top-Down

El diseño **top-down** divide el problema desde lo general hacia lo específico, organizando el programa de manera estructurada.

---

## 🔹 8. Ejemplos Prácticos en C

### 📌 Ejemplo 1: Función sin retorno

```c
#include <stdio.h>

void mostrarMensaje() {
    printf("Bienvenido a la Programación Modular\n");
}

int main() {
    mostrarMensaje();
    return 0;
}
```
### 📌 Ejemplo 2: Función con retorno

```c
#include <stdio.h>

int sumar(int a, int b) {
    return a + b;
}

int main() {
    int resultado = sumar(5, 3);
    printf("La suma es: %d\n", resultado);
    return 0;
}
```
### 📌 Ejemplo 3: Paso por valor

```c
#include <stdio.h>

void incrementar(int x) {
    x = x + 1;
}

int main() {
    int numero = 5;
    incrementar(numero);
    printf("Valor final: %d\n", numero);
    return 0;
}
```
### 📌 Ejemplo 4: Paso por referencia

```c
#include <stdio.h>

void incrementar(int *x) {
    *x = *x + 1;
}

int main() {
    int numero = 5;
    incrementar(&numero);
    printf("Valor final: %d\n", numero);
    return 0;
}
```
### 📌 Ejemplo 5: Diseño Top-Down

```c
#include <stdio.h>

int suma(int a, int b) {
    return a + b;
}

int resta(int a, int b) {
    return a - b;
}

int multiplicacion(int a, int b) {
    return a * b;
}

float division(int a, int b) {
    return (float)a / b;
}

int main() {
    int x = 10, y = 5;

    printf("Suma: %d\n", suma(x, y));
    printf("Resta: %d\n", resta(x, y));
    printf("Multiplicacion: %d\n", multiplicacion(x, y));
    printf("Division: %.2f\n", division(x, y));

    return 0;
}
```
---

<div align="center" style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin-bottom: 20px;">

<!-- Botón Recurso  siguiente -->
<a href="./Recurso2" style="
    background: linear-gradient(90deg, #1E88E5, #42A5F5);
    color: white;
    padding: 12px 25px;
    text-decoration: none;
    font-size: 16px;
    font-weight: bold;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.2);
    display: inline-block;
">
Recurso 2 ➡️
</a>

</div>

<div align="center">
<!-- Botón para volver a la Unidad 2 -->
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
