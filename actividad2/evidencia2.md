# Respuestas a las preguntas

## 1. ¿Qué es y para qué sirve el mapa de memoria de un microprocesador?

El **mapa de memoria** de un microprocesador es una representación que muestra cómo se organiza la memoria del sistema. Indica cómo las diferentes áreas de la memoria se asignan para almacenar **programas**, **datos**, y otras **instrucciones**. Sirve para saber qué parte de la memoria está destinada a cada tipo de información, lo que ayuda a gestionar eficientemente los recursos del sistema.

## 2. Basándote en la figura 3, responde:

### 2.1. ¿Cuántos pines del bus de direcciones del MC6802 se utilizan en esta conexión? ¿Cuáles son los nombres utilizados para representarlos?

El **MC6802** utiliza **16 pines** en el bus de direcciones. Estos pines son los que se usan para direccionar la memoria y otros periféricos. Los nombres que se utilizan son `A0` hasta `A15`, donde cada uno representa una línea de dirección.

### 2.2. ¿De qué valor es la memoria total de almacenamiento del MC6846? Incluye los cálculos que realizaste.

La **memoria total** del **MC6846** es de **16 Kbytes** (kilobytes). Esto lo calculamos con la fórmula:



```math
Memoria total = Número de direcciones * Tamaño de cada palabra
```


El **MC6846** tiene un bus de direcciones de **14 bits**, lo que significa que puede direccionar **2^14 = 16,384** ubicaciones de memoria. Como cada ubicación tiene **1 byte** de capacidad, la memoria total es:



```math
16,384 ubicaciones * 1 byte = 16 Kbytes
```



### 2.3. ¿Cuántos bits ocupa cada dato al que se puede acceder en la memoria MC6846? ¿Cómo lo dedujiste?

Cada dato en la memoria del **MC6846** ocupa **8 bits**. Esto lo deduzco porque el **MC6846** tiene un **bus de datos de 8 bits**, lo que significa que puede leer o escribir **1 byte** de información por cada acceso.

## 3. ¿Cuáles son las características más relevantes de la arquitectura von Neumann y Harvard?

### Arquitectura **von Neumann**:
- Usa **una sola memoria** para **datos** e **instrucciones**.
- Las instrucciones y los datos se transmiten por el **mismo bus**.
- Tiene un solo espacio de **direcciones**, lo que puede generar cuellos de botella cuando se accede tanto a datos como a instrucciones.

### Arquitectura **Harvard**:
- Usa **memorias separadas** para **datos** e **instrucciones**.
- Cada tipo de memoria tiene su propio **bus de datos**.
- Permite un **acceso simultáneo** a instrucciones y datos, lo que mejora el rendimiento.

## 4. ¿Cuáles son las características más relevantes de la arquitectura CISC y RISC?

### Arquitectura **CISC** (Complex Instruction Set Computing):
- Tiene un conjunto de instrucciones más **grande** y **complejo**.
- Permite realizar tareas más complejas con **una sola instrucción**.
- Requiere más **ciclos de reloj** para ejecutar las instrucciones.

### Arquitectura **RISC** (Reduced Instruction Set Computing):
- Tiene un conjunto de instrucciones más **reducido** y **simple**.
- Cada instrucción suele ejecutarse en **un solo ciclo de reloj**.
- Requiere más instrucciones para realizar tareas complejas, pero generalmente es **más rápida**.

## 5. ¿Cuál es tu opinión sobre los tipos de arquitecturas que se observan en los microprocesadores?

En mi opinión, las arquitecturas **CISC** y **RISC** tienen sus ventajas dependiendo del tipo de aplicación. **CISC** es más útil en sistemas donde las tareas son más complejas y el **ahorro de espacio** es crucial, ya que las instrucciones son más potentes. Por otro lado, **RISC** es ideal para aplicaciones que requieren **velocidad** y **eficiencia**, ya que las instrucciones simples permiten que el procesador ejecute más rápido. La elección de la arquitectura depende mucho del **uso específico** que se le quiera dar al microprocesador.
