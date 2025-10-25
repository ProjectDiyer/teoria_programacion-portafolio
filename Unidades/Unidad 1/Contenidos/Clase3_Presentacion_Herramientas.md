<div align="center">

<!-- Botón para volver a la Unidad 1 -->
<a href="../Unidad 1.md" style="
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
⬅️ Volver a Unidad 1
</a>

</div>

# 🧱 Clase 3 — Presentación Herramientas para programación y Lenguajes de alto nivel

---

## 📄 Descripción

En esta clase vimos los conceptos fundamentales de los **lenguajes de programación**, su relación con algoritmos y programas, y la importancia de las herramientas para desarrollar código eficiente.

Se explicó la diferencia entre:  
- **Algoritmo:** método o conjunto de pasos para resolver un problema.  
- **Programa:** implementación concreta del algoritmo en un lenguaje ejecutable.  

Se analizaron los tipos de lenguajes:  
- **Compilados:** requieren compilador (C, C++, Pascal). Más rápidos al ejecutar.  
- **Interpretados:** requieren intérprete (Python, JavaScript). Más flexibles, más lentos.  

También se abordaron **lenguajes de alto nivel**, que usan sintaxis cercana al lenguaje humano, y la importancia de traducirlos a lenguaje máquina para su ejecución.

### 🛠 Herramientas y Entornos

Para programar, vimos la importancia de **IDE** y otras herramientas:  

**Visual Studio Code (VS Code):** editor de código con múltiples extensiones para depuración y ejecución.  

**Instalación de VS Code en Windows:**  

```terminal
1. Descargar desde: https://code.visualstudio.com/
2. Ejecutar el instalador y seguir los pasos predeterminados.
3. Marcar la opción "Agregar a PATH" para poder ejecutar desde terminal.
4. Instalar extensiones recomendadas: PSeInt, C/C++ (Microsoft), Python.
```

**MSYS2 (para compilación de C/C++ en Windows):**  

```terminal
1. Descargar desde: https://www.msys2.org/
2. Instalar siguiendo los pasos predeterminados.
3. Abrir "MSYS2 MinGW 64-bit" y actualizar paquetes:
   pacman -Syu
4. Instalar compiladores:
   pacman -S mingw-w64-x86_64-gcc
5. Configurar PATH para usar gcc desde VS Code terminal.
```

Estas herramientas permiten codificar, compilar y ejecutar programas en distintos lenguajes de forma sencilla y eficiente.

Puedes revisar la [presentación completa de la clase](https://drive.google.com/file/d/1XrpTYheRlmSmuMyiv4wJWrsFAeOtctiz/view?usp=sharing) para más detalles.

---

## 🧩 Actividad

**Ejercicio práctico:**  
- Instalar VS Code y MSYS2.  
- Crear un archivo simple en C llamado `HolaMundo.c`:  

```c
#include <stdio.h>

int main() {
    printf("¡Hola, mundo!\n");
    return 0;
}
```

- Compilar con MSYS2:  

```terminal
gcc HolaMundo.c -o HolaMundo.exe
```

- Ejecutar desde terminal:  

```terminal
./HolaMundo.exe
```
- Salida en la terminal:

```terminal
¡Hola, mundo!
```
> Esta actividad permite familiarizarse con las herramientas y comprender la relación entre algoritmos, programas y lenguajes de programación.

---

<div align="center">

<!-- Botón para volver a la Unidad 1 -->
<a href="../Unidad 1.md" style="
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
⬅️ Volver a Unidad 1
</a>

</div>
