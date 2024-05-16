### Capítulo 3: Puertas Lógicas y Álgebra de Boole

#### 3.1 Valor Lógico Asociado a las Señales Digitales
El capítulo comienza con la definición de señales, variables y funciones lógicas en sistemas digitales. Los sistemas lógicos digitales utilizan transistores para realizar operaciones lógicas básicas (AND, OR, NOT, etc.), asignando valores lógicos ‘0’ y ‘1’ a las señales eléctricas. Las señales de entrada se convierten en variables lógicas de salida mediante funciones lógicas implementadas por circuitos electrónicos.

#### 3.2 Simulación de Sistemas Digitales con Logisim
Logisim es una herramienta educativa que permite la simulación de sistemas digitales. Facilita el diseño y análisis de circuitos lógicos sin necesidad de detalles físicos del hardware, proporcionando un enfoque práctico a través de su interfaz intuitiva. Logisim incluye librerías de componentes como puertas lógicas, multiplexores, sumadores, biestables y elementos de entrada/salida, y permite la creación jerárquica de circuitos.

#### 3.3 Puertas Lógicas

**Puerta NOT**
- **Función**: Inversión lógica (salida es el complemento de la entrada).
- **Símbolo**: Triángulo seguido de una burbuja (◦).
- **Tabla de Verdad**: 
  \[
  \begin{array}{c|c}
  A & A' \\
  \hline
  0 & 1 \\
  1 & 0 \\
  \end{array}
  \]
- **Propiedad**: Involución por doble aplicación: \((A')' = A\).

**Puerta AND**
- **Función**: Producto lógico (salida es 1 si todas las entradas son 1).
- **Símbolo**: D con dos entradas.
- **Tabla de Verdad**: 
  \[
  \begin{array}{c|c|c}
  A & B & AB \\
  \hline
  0 & 0 & 0 \\
  0 & 1 & 0 \\
  1 & 0 & 0 \\
  1 & 1 & 1 \\
  \end{array}
  \]
- **Propiedades**: Conmutativa, asociativa, elemento neutro, idempotencia, complemento.

**Puerta OR**
- **Función**: Suma lógica (salida es 1 si alguna entrada es 1).
- **Símbolo**: Curva con dos entradas.
- **Tabla de Verdad**: 
  \[
  \begin{array}{c|c|c}
  A & B & A+B \\
  \hline
  0 & 0 & 0 \\
  0 & 1 & 1 \\
  1 & 0 & 1 \\
  1 & 1 & 1 \\
  \end{array}
  \]
- **Propiedades**: Conmutativa, asociativa, elemento neutro, idempotencia, complemento.

**Puerta NAND**
- **Función**: AND negado (salida es 0 si todas las entradas son 1).
- **Símbolo**: D con burbuja en la salida.
- **Tabla de Verdad**: 
  \[
  \begin{array}{c|c|c}
  A & B & (AB)' \\
  \hline
  0 & 0 & 1 \\
  0 & 1 & 1 \\
  1 & 0 & 1 \\
  1 & 1 & 0 \\
  \end{array}
  \]
- **Propiedades**: Conmutativa, no asociativa, complemento.

**Puerta NOR**
- **Función**: OR negado (salida es 1 si todas las entradas son 0).
- **Símbolo**: Curva con burbuja en la salida.
- **Tabla de Verdad**: 
  \[
  \begin{array}{c|c|c}
  A & B & (A+B)' \\
  \hline
  0 & 0 & 1 \\
  0 & 1 & 0 \\
  1 & 0 & 0 \\
  1 & 1 & 0 \\
  \end{array}
  \]
- **Propiedades**: Conmutativa, no asociativa, complemento.

**Puerta XOR**
- **Función**: OR exclusivo (salida es 1 si una y solo una entrada es 1).
- **Símbolo**: Curva con línea curva adicional.
- **Tabla de Verdad**: 
  \[
  \begin{array}{c|c|c}
  A & B & A \oplus B \\
  \hline
  0 & 0 & 0 \\
  0 & 1 & 1 \\
  1 & 0 & 1 \\
  1 & 1 & 0 \\
  \end{array}
  \]
- **Propiedades**: Conmutativa, asociativa, elemento neutro.

**Puerta XNOR**
- **Función**: OR exclusivo negado (salida es 1 si las entradas son iguales).
- **Símbolo**: Curva con línea curva adicional y burbuja.
- **Tabla de Verdad**: 
  \[
  \begin{array}{c|c|c}
  A & B & (A \oplus B)' \\
  \hline
  0 & 0 & 1 \\
  0 & 1 & 0 \\
  1 & 0 & 0 \\
  1 & 1 & 1 \\
  \end{array}
  \]
- **Propiedades**: Conmutativa, asociativa, elemento neutro.

#### 3.4 Álgebra de Boole Aplicada a los Sistemas Digitales
El álgebra de Boole formaliza el análisis y diseño de sistemas digitales. Shannon aplicó el álgebra de Boole a circuitos lógicos, demostrando que cualquier función lógica puede implementarse electrónicamente.

**Principio de Dualidad**: Permite derivar nuevas expresiones lógicas válidas a partir de expresiones existentes, intercambiando operaciones lógicas y negando variables y constantes.

#### 3.5 Expresiones Algebraicas Equivalentes de una Función Lógica
Las funciones lógicas pueden tener múltiples expresiones algebraicas equivalentes, lo que permite simplificar y optimizar el diseño de circuitos. Las equivalencias se demuestran mediante transformaciones algebraicas o comparación de tablas de verdad.

### Conceptos Clave
1. **Puertas Lógicas**: Elementos básicos (NOT, AND, OR, NAND, NOR, XOR, XNOR) para construir circuitos digitales.
2. **Álgebra de Boole**: Herramienta matemática para el análisis y diseño de sistemas digitales.
3. **Logisim**: Herramienta para simular y analizar el comportamiento de sistemas digitales.
4. **Principio de Dualidad**: Método para derivar nuevas propiedades y teoremas en álgebra de Boole.
5. **Equivalencia de Expresiones**: Varias expresiones pueden representar la misma función lógica, facilitando la simplificación de circuitos.

Este capítulo proporciona una base sólida para entender cómo se diseñan y analizan los sistemas digitales utilizando puertas lógicas y álgebra de Boole, facilitando el aprendizaje práctico a través de herramientas como Logisim.

