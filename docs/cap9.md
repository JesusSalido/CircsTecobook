### Capítulo 9: Sistemas Secuenciales Síncronos

#### 9.1 Sistemas Asíncronos vs. Síncronos

**Definiciones y Diferencias**
- **Asíncronos**: Las salidas y estados reflejan cambios inmediatos en las entradas, sin una señal de reloj, lo que dificulta la coordinación.
- **Síncronos**: Las salidas y estados cambian en instantes determinados por una señal de reloj (CLK), facilitando el diseño y análisis mediante Autómatas de Estados Finitos (FSM).

#### 9.2 Estados de un Sistema Secuencial

**Definición del Estado**
- **Estado**: Valor instantáneo almacenado en los elementos de memoria (biestables) del sistema.
- Cada biestable puede almacenar un bit, por lo que con \(n\) biestables, un sistema puede tener hasta \(2^n\) estados diferentes.

**Codificación de Estados**
- Estados representados como combinaciones de bits almacenados en biestables.
- Ejemplo: Para un sistema con 3 biestables, el estado \(Q5\) se codifica como [101], lo que significa que \(q2 = 1\), \(q1 = 0\) y \(q0 = 1\).

#### 9.3 Autómatas Finitos

**Definición y Componentes**
- **Autómata Finito (FSM)**: Modelo matemático para sistemas secuenciales.
- Componentes:
  - Conjunto \(X\) de entradas.
  - Conjunto \(Y\) de salidas.
  - Conjunto \(Q\) de estados.
  - Función de transición: \(\delta : Q \times X \rightarrow Q\)
  - Función de salida: \(\lambda : Q \times X \rightarrow Y\)

**Tipos de Autómatas**
1. **Autómata de Moore**: La salida depende únicamente del estado actual.
2. **Autómata de Mealy**: La salida depende del estado y de las entradas actuales.

#### 9.4 Diagrama de Transición de Estado (DTE)

**Elementos del DTE**
- **Estados**: Representados por círculos o elipses.
- **Transiciones**: Arcos orientados que indican el cambio de estado debido a una entrada específica.
- **Estados de Partida y Destino**: Representan el comportamiento del sistema en diferentes instantes.

**Ejemplos de DTE**
- DTE de un autómata de Mealy para un sumador serie de un bit con acarreo, mostrando transiciones basadas en entradas y salidas.

#### 9.5 Tabla de Transición de Estado y Tabla de Salida

**Construcción y Uso**
- Tabla de Transición de Estado: Describe cómo las entradas afectan el estado y la salida.
- Tabla de Salida: Utilizada en autómatas de Moore, donde la salida depende únicamente del estado.

#### 9.6 Método de Análisis de Circuitos Secuenciales

**Pasos de Análisis**
1. Obtener funciones de excitación de los biestables.
2. Obtener la función de salida.
3. Construir la tabla de transición de estados.
4. Obtener los estados de evolución del sistema.
5. Obtener el valor de la salida del sistema.
6. Elaborar el DTE.

**Ejemplo de Análisis**
- Análisis de un circuito con biestables J-K, obteniendo funciones de excitación y la tabla de transición de estados.

#### 9.7 Diseño de Sistemas Secuenciales Síncronos

**Pasos de Diseño**
1. Identificar entradas, salidas y estados.
2. Transformar la especificación en un DTE.
3. Obtener la tabla de transición de estados.
4. Determinar entradas a los biestables.
5. Calcular la salida en cada transición.
6. Calcular funciones combinacionales para la excitación de los biestables.
7. Calcular la función de salida.
8. Implementar las funciones calculadas.

**Ejemplo de Diseño**
- Diseño de un reconocedor de secuencia que identifica la entrada de tres unos consecutivos, utilizando un autómata de Moore.

#### Aplicaciones y Ejemplos Prácticos

**Diseño de Contadores**
- Contadores de secuencia completa desordenada y de secuencia incompleta.
- Ejemplo: Diseño de un contador de código Gray de 3 bits.

**Diseño de Sistemas Temporizados**
- Generadores de secuencias con valores repetidos y control de dispositivos mediante temporización.
- Ejemplo: Diseño de un generador de secuencia que produce [0,3,2,1,2,1,3].

**Métodos Alternativos de Implementación**
- Uso de multiplexores y memorias ROM para generar secuencias.

Este capítulo aborda en profundidad el análisis y diseño de sistemas secuenciales síncronos, proporcionando las bases teóricas y prácticas para la creación de sistemas digitales complejos que dependen de una historia previa de entradas.
