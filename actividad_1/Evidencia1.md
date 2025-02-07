# INVESTIGACIÓN

## **CPU**
Es el componente principal de un sistema informático que se encarga de **interpretar y ejecutar instrucciones**, además de **procesar datos** y **controlar las operaciones del sistema**.

## **ALU (Unidad Aritmética Lógica)**
Subunidad de la CPU que realiza **operaciones aritméticas y lógicas**.

## **REGISTROS**
Unidades de **almacenamiento de alta velocidad** en la CPU que almacenan temporalmente datos, instrucciones o direcciones.

### **PROPÓSITO GENERAL**
Almacena temporalmente **datos durante cualquier operación**.

### Registros de Propósito Específico

- **Program Counter (PC):** Contiene la dirección de la próxima instrucción a ejecutar.
- **Stack Pointer (SP):** Apunta al último elemento en la pila de memoria.
- **Base Pointer (BP):** Señala la base de la pila de una función o subrutina.
- **Accumulator (AC):** Almacena resultados de operaciones aritméticas y lógicas.
- **Instruction Register (IR):** Contiene la instrucción actual en ejecución.


## **UNIDAD DE CONTROL**
Es la parte de la CPU que **dirige y sincroniza las operaciones**, enviando señales a otros componentes para ejecutar las instrucciones.

## **BUS DE DATOS**
Transporta **información** entre la CPU, la memoria y otros dispositivos.

## **BUS DE DIRECCIÓN**
Lleva las **ubicaciones de memoria** que se están leyendo o escribiendo.

## **MEMORIA**

### **RAM (Memoria Volátil)**
Memoria **volátil** usada para **almacenar temporalmente datos** e instrucciones durante la ejecución del programa.

### **ROM (Memoria No Volátil)**
Memoria **no volátil** que contiene **datos permanentes**, como el **firmware**.

> Aunque **ROM** sigue siendo vigente, ha evolucionado en tecnologías como **EEPROM** o **FLASH MEMORY**.

## **OPCODE**
Es la parte de una instrucción que **especifica la operación** que debe realizar la CPU, como **sumar**, **comparar** o **mover datos**.



## Simulación en Digital

Cada uno de los componentes interactúa entre sí para simular un computador de **16 bits**. La tarea principal de esta simulación es ejecutar un **programa previamente cargado**, que gestiona la interacción de la CPU, la ROM y la memoria para realizar tareas específicas.

![Circuito](images1/circuito.png)

El sistema está compuesto por las siguientes partes clave: **CPU**, **ROM** y **Memoria**.

- La **CPU** es responsable de **solicitar datos** desde la **ROM**, donde se encuentra el programa cargado. Su función es **decodificar las instrucciones** contenidas en el programa y procesarlas de acuerdo a lo que se requiere. Después, la CPU actualiza los valores en la memoria para reflejar los cambios y preparar la salida.
  
- La **Memoria** se utiliza para almacenar tanto los datos del programa como la información que se actualiza a lo largo de la ejecución. En ella también se encuentra el componente **HackDisplay**, que gestiona la salida visual en la pantalla.

- La **ROM** almacena el **programa** que se ejecuta en el computador simulado. Este programa contiene todas las instrucciones necesarias para que la CPU pueda procesar y llevar a cabo las tareas requeridas por el sistema.

![Pantalla](images1/pantalla.png)

El componente **HackDisplay** se encuentra en la memoria y es el responsable de mostrar la salida visual del programa en una pantalla de **512 px x 256 px**. Esta pantalla refleja lo que ocurre en el sistema, mostrando los cambios en tiempo real según las interacciones del usuario (por ejemplo, cuando se presionan las teclas `1`, `2`, `3` o `4`).

Ésta es una simulación básica de un computador de **16 bits** y refleja la **interacción** entre los componentes clave de una arquitectura de computadora.

---



### ¿Qué es un programa y dónde se almacena?
Un **programa** es un conjunto de instrucciones escritas en un lenguaje de programación que realiza una tarea específica cuando se ejecuta. Los programas se almacenan principalmente en la **ROM** (memoria de solo lectura) o en el **almacenamiento secundario** (como un disco duro o unidad SSD) antes de ser cargados en la **memoria RAM** durante la ejecución.

### Si pongo un comentario en un programa como: `//variable tipo contador`, ¿dónde se almacena dicho comentario?
Un **comentario** en un programa, como `//variable tipo contador`, no se almacena en la memoria de datos. Los comentarios son simplemente **anotaciones** dentro del código fuente y son ignorados durante la ejecución. Sin embargo, se almacenan en el archivo de código fuente y son parte del **código fuente** del programa.

### ¿Dónde se almacena una variable?
Las **variables** se almacenan en la **memoria RAM** durante la ejecución del programa. Dependiendo de la **localización** (local o global) y del tipo de variable, esta puede ser almacenada en diferentes **regiones de memoria**. En general, las variables locales suelen residir en la pila (stack), mientras que las globales se almacenan en el **segmento de datos**.


## Proceso Fetch-Decode-Execute

El proceso `Fetch-Decode-Execute` es como el ciclo que sigue la **CPU** para ejecutar un programa. Es una serie de pasos que se repiten una y otra vez para que el procesador haga su trabajo. Aquí te lo explico de forma sencilla:

**Fetch (Buscar)**: 
   - La **CPU** empieza buscando la **instrucción** que tiene que ejecutar. Esta instrucción está guardada en la **memoria**. La CPU sabe dónde buscar gracias a un contador que le indica la dirección de la siguiente instrucción.

**Decode (Decodificar)**: 
   - Cuando la CPU encuentra la instrucción, necesita entender qué debe hacer con ella. **Decodificar** significa que la CPU "lee" la instrucción y sabe qué operación tiene que hacer.

**Execute (Ejecutar)**: 
   - Después de entender qué hacer, la CPU realiza la **acción** que le dijo la instrucción. Esto puede ser hacer cálculos, mover información de un lugar a otro o modificar datos.

Este ciclo de `Fetch-Decode-Execute` se repite una y otra vez hasta que el programa haya terminado de ejecutarse. Cada vez que la CPU hace esto, avanza en el proceso y va completando las tareas que le pide el programa.


### Tipos de instrucciones del procesador

Las instrucciones del procesador se dividen en varios tipos, cada uno con una función específica para realizar diferentes operaciones:

 **Instrucciones de Aritmética y Lógica**  
   Realizan operaciones matemáticas o lógicas. Ejemplo: `ADD R1, R2` suma los valores de **R1** y **R2** y guarda el resultado en **R1**.  
   **Uso**: Cálculos y manipulación de datos.

 **Instrucciones de Movimiento de Datos**  
   Mueven datos entre registros o memoria. Ejemplo: `MOV R1, R2` mueve el valor de **R2** a **R1**.  
   **Uso**: Transferencia de datos.

 **Instrucciones de Control de Flujo**  
   Controlan la secuencia de ejecución. Ejemplo: `JMP 200` salta a la dirección de memoria 200.  
   **Uso**: Bucles y saltos condicionales.

 **Instrucciones de Entrada/Salida (E/S)**  
   Permiten que el procesador interactúe con dispositivos externos. Ejemplo: `IN R1` lee un valor de una entrada y lo guarda en **R1**.  
   **Uso**: Comunicación con el mundo exterior.

**Instrucciones de Comparación**  
   Comparan valores y actualizan registros de estado. Ejemplo: `CMP R1, R2` compara **R1** y **R2**.  
   **Uso**: Control de flujo condicional.


