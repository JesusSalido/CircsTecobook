### Capítulo 5: Módulos Combinacionales Básicos

#### 5.1 Decodificador Binario

**Definición y Características**
- **Decodificador $n \times 2^n$**: Módulo con $n$ entradas y $2^n$ salidas, que activa una única salida correspondiente al código binario en su entrada.
- **Función**: Realiza la decodificación del código de entrada, activando la salida correspondiente.

**Implementación**
- Un DEC con salidas activas a nivel alto actúa como un generador de minitérminos, mientras que uno con salidas activas a nivel bajo genera maxitérminos.
- Implementación típica incluye $2^n$ puertas AND y $n$ inversores, con una entrada adicional de habilitación.

**Aplicaciones**
- Utilizado para habilitación selectiva de subsistemas en sistemas digitales complejos, como en la habilitación de periféricos compartidos en un bus de datos de un computador.

**Redes Modulares**
- DEC más complejos pueden ser implementados mediante la conexión de DEC más simples en una red modular, gestionando la habilitación selectiva entre ellos.

#### 5.2 Multiplexor

**Definición y Características**
- **Multiplexor (MUX)**: Selecciona una de las varias líneas de datos de entrada para transmitir por una única salida basada en un código de entrada de n bits.
- **Función**: Facilita la transmisión de datos desde múltiples fuentes a través de un canal compartido.

**Implementación**
- Usando una red AND/OR para decodificar los productos canónicos de las entradas de selección y combinando las salidas con una puerta OR.
- Señal de habilitación ($E$) controla la activación de la salida.

**Teorema de Expansión de Shannon**
- Permite implementar cualquier función lógica con un MUX al conectar los valores de la tabla de verdad de la función a las entradas del MUX.

**Redes Modulares**
- MUX de orden superior pueden ser construidos conectando múltiples MUX más simples en una red modular, sin necesidad de señal de habilitación en configuraciones multinivel.

#### 5.3 Demultiplexor

**Definición y Características**
- **Demultiplexor (DEMUX)**: Distribuye datos desde una única entrada a múltiples salidas basadas en un código de selección.
- **Función**: Realiza la operación inversa del MUX, seleccionando una salida específica para los datos de entrada.

**Implementación**
- Similar al DEC, pero utilizando la señal de habilitación como entrada de datos.

#### 5.4 Codificador Binario

**Definición y Características**
- **Codificador (ENC)**: Convierte una de las $2^n$ entradas activas en un código binario de $n$ bits.
- **Función**: Realiza la operación inversa del DEC, generando el código binario correspondiente a la entrada activada.

**Implementación**
- Incluye la lógica para manejar múltiples entradas activas simultáneamente, aplicando criterios de prioridad para determinar la salida correcta.

**Codificador con Prioridad**
- Implementa un circuito de prioridad para activar únicamente la entrada de mayor prioridad cuando múltiples entradas están activas.
- Señales auxiliares como Enable input ($E_i$), Group select ($G_s$), y Enable output ($E_o$) facilitan la diferenciación de estados y la conexión en cadena de múltiples codificadores.

### Conceptos Clave

1. **Decodificadores**: Generan minitérminos o maxitérminos según el nivel de activación de sus salidas.
2. **Multiplexores**: Seleccionan y transmiten datos desde múltiples entradas a una salida.
3. **Demultiplexores**: Distribuyen datos desde una única entrada a múltiples salidas.
4. **Codificadores**: Convierten entradas activas a un código binario, con gestión de prioridad para múltiples entradas activas.
5. **Redes Modulares**: Permiten la implementación de módulos complejos mediante la conexión de módulos más simples.
6. **Teorema de Expansión de Shannon**: Facilita la implementación de funciones lógicas con MUX.

Este capítulo describe la funcionalidad y la implementación de varios módulos combinacionales básicos utilizados en sistemas digitales, destacando su importancia en el diseño jerarquizado de circuitos complejos.

