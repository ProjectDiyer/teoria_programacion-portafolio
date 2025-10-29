---
layout: default
title: Clase 1
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

# 🧮 Clase 1 — Presentación Conceptos fundamentales de Algoritmos

---

## 📄 Descripción

En esta clase vimos los fundamentos y etapas para resolver problemas mediante algoritmos y programas en computadoras.  
Puedes revisar la [presentación completa de la clase](https://drive.google.com/file/d/1aYV_ripCYtv78KewLJXzWIeQKpVe1JXl/view?usp=sharing) para más detalles.

Se explicó el proceso general de resolución de problemas mediante la interacción **hardware-software**, definiendo un algoritmo como un conjunto de pasos secuenciales que transforman datos de entrada en resultados útiles.  

Se destacaron las tres partes principales de un algoritmo:
- **Entradas:** datos necesarios para realizar la tarea.  
- **Procesos:** acciones o cálculos realizados.  
- **Salidas:** resultados obtenidos.  

Para representar algoritmos de manera clara y estandarizada se utilizaron:
- **Pseudocódigo:** descripción en lenguaje cercano al natural con estructura lógica.  
- **Diagramas de flujo:** símbolos gráficos que representan el flujo de procesos.  

El desarrollo de un programa paso a paso se explicó en cinco fases:
1. **Análisis del problema**: identificación de datos, requisitos y restricciones.  
2. **Diseño del algoritmo**: boceto del proceso usando pseudocódigo o diagramas de flujo.  
3. **Codificación**: traducción del diseño a un lenguaje de programación.  
4. **Pruebas**: verificación y corrección de errores.  
5. **Documentación y mantenimiento**: registro detallado del proceso y preparación para futuras modificaciones.  

Se mencionaron herramientas visuales como **PSeInt, Draw.io y Lucidchart**, así como tipos de algoritmos cualitativos y cuantitativos, enfatizando la estandarización de las instrucciones.

---

## 🧩 Actividad

**Ejemplo de pseudocódigo en PSeInt:**

> El algoritmo lee dos números enteros ingresados por el usuario, calcula su suma y muestra el resultado en pantalla.

**Pasos:**
1. Solicita el primer y segundo número.  
2. Realiza la operación: `suma ← num1 + num2`.  
3. Muestra el resultado: `La suma es: (suma)`.

```pseudocode
Algoritmo SumarNumeros
    Definir num1, num2, suma Como Entero;
    Escribir "Ingrese el primer número:";
    Leer num1;
    Escribir "Ingrese el segundo número:";
    Leer num2;
    suma <- num1 + num2;
    Escribir "La suma es:", suma;
FinAlgoritmo
```

**Prueba de escritoriot:**

| **Caso** | **Entrada (num1)** | **Entrada (num2)** | **Proceso**             | **Salida**        |
|-----------|--------------------|--------------------|--------------------------|-------------------|
| 1         | 5                  | 3                  | suma ← 5 + 3 = 8         | La suma es: 8     |
| 2         | 10                 | 15                 | suma ← 10 + 15 = 25      | La suma es: 25    |
| 3         | -2                 | 7                  | suma ← -2 + 7 = 5        | La suma es: 5     |
| 4         | 5                  | 7                  | suma ← 5 + 7 = 0         | La suma es: 12     |

**Terminal:**

```terminal
Ingrese el primer número:
> 5
Ingrese el segundo número:
> 7
La suma es: 12
```

**Diagrama de flujo:**

> El diagrama de flujo representa el proceso para sumar dos números ingresados por el usuario.  
Inicia con la definición de las variables `num1`, `num2` y `suma`. Luego solicita los dos valores, realiza la operación `suma ← num1 + num2` y finalmente muestra el resultado en pantalla.  
El proceso termina con el fin del algoritmo.

![Diagrama de flujo](../Imagenes/SumarNumeros.svg)

> Esta actividad permitió practicar la creación de algoritmos secuenciales y su representación en pseudocódigo antes de codificar en un lenguaje real.

---

<div align="center" style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; margin-bottom: 20px;">

<!-- Botón Clase siguiente -->
<a href="./Clase2_Presentacion_Elementos" style="
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
Clase 2 ➡️
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

