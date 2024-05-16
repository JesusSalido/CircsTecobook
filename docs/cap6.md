### Capítulo 6: Módulos Lógicos y Aritméticos

#### 6.1 El Comparador

**Definición y Funcionamiento**
- Un comparador es un circuito combinacional que compara dos entradas A y B y produce tres salidas: A<B, A=B y A>B.
- **Diseño de 1 bit**:
  - A=B: Se utiliza una puerta XNOR.
  - A>B: Se evalúa mediante una puerta AND.
  - A<B: Se logra mediante otra puerta AND.
- **Comparadores de N bits**:
  - Construidos modularmente usando comparadores de 1 bit y lógica adicional para manejar los resultados de bits menos significativos.
  - Comparadores más grandes se pueden construir en cascada, como se ilustra con el comparador de 4 bits y el circuito integrado 74HC85.

#### 6.2 Generador de Paridad

**Definición y Funcionamiento**
- El generador de paridad añade un bit de paridad a un bloque de datos para detectar errores en la transmisión.
- **Tipos de Paridad**:
  - Paridad par: Asegura un número par de unos en el bloque de datos.
  - Paridad impar: Asegura un número impar de unos.
- **Implementación**:
  - Utiliza puertas XOR para calcular el bit de paridad sumando todos los bits del bloque de datos.
  - El bit de paridad calculado se añade al bloque de datos para su transmisión y en el receptor se comprueba la paridad para detectar errores.

#### 6.3 Conversores de Código

**Definición y Funcionamiento**
- Transforman un código digital en otro diferente.
- **Implementación**:
  - Mediante puertas lógicas, decodificadores (DEC), codificadores (COD) y memorias ROM.
  - Ejemplos incluyen la conversión entre BCD y BCD-ex3, que puede ser implementada usando tablas de verdad y expresiones lógicas minimizadas.

#### 6.4 Módulos Aritméticos

**El Semisumador**
- **Definición**: Módulo aritmético más sencillo que suma dos bits y produce un bit de suma y un bit de acarreo.
- **Implementación**: Utiliza puertas XOR para la suma y puertas AND para el acarreo.

**El Sumador Completo**
- **Definición**: Suma dos bits considerando el acarreo de entrada y produce una suma y un acarreo de salida.
- **Implementación**: Utiliza dos semisumadores en cascada.
- **Análisis de Desbordamiento**:
  - Se produce cuando el resultado de la operación no puede ser representado con el número de bits disponibles.
  - Detectado mediante el análisis del bit de signo y los acarreos obtenidos.

**Sumador Paralelo con Acarreo Serie**
- **Definición**: Suma bit a bit con acarreo propagado entre sumadores completos.
- **Limitaciones**: El acarreo debe propagarse a través de todas las etapas, lo que introduce retardo.
- **Sumador con Acarreo Anticipado**: Utiliza lógica adicional para calcular acarreos más rápidamente.

**Sumador-Restador**
- **Definición**: Realiza sumas y restas considerando números negativos en complemento a dos.
- **Implementación**: Emplea puertas XOR para invertir el operando B en la operación de resta.

**Sumador BCD**
- **Definición**: Realiza sumas en código BCD, detectando y corrigiendo sumas que exceden el valor 9.
- **Implementación**: Utiliza sumadores completos y lógica adicional para detectar y corregir excedentes.

**Módulos de Multiplicación y División**
- **Definición**: Implementan multiplicación como sumas repetidas y división como restas repetidas.
- **Optimización**: Desplazamientos a la izquierda/derecha para multiplicaciones/divisiones por potencias de 2.

**Cálculo del Número de Entradas Activas**
- **Definición**: Determina cuántas entradas están en alto en un sistema digital.
- **Implementación**: Utiliza sumadores completos para sumar las entradas activas.

#### 6.5 Unidad Aritmética Lógica (UAL)

**Definición y Funcionamiento**
- Una ALU es un módulo combinacional capaz de realizar operaciones lógicas (AND, OR) y aritméticas (suma, resta).
- **Señales de la ALU**:
  - Datos: Operandos y resultados.
  - Control: Selección de la operación.
  - Auxiliares: Facilitan la interconexión con otros módulos.
- **Diseño de ALU Sencilla**:
  - Dos operandos de 4 bits.
  - Cuatro señales de control para seleccionar entre 16 posibles operaciones (12 implementadas).
  - Salida de 4 bits más un bit de acarreo.

### Conceptos Clave
- Comparadores y su implementación modular.
- Generación y detección de bits de paridad.
- Conversores de código y técnicas de minimización lógica.
- Diseño y optimización de sumadores y restadores.
- Detección de desbordamiento en operaciones aritméticas.
- Implementación de ALU para operaciones combinacionales complejas.

Este capítulo ofrece un panorama detallado sobre los módulos combinacionales empleados en operaciones lógicas y aritméticas, destacando su implementación y optimización en sistemas digitales.


