### Capítulo 4: Circuitos Digitales Combinacionales

#### 4.1 Circuitos Combinacionales y Funciones Lógicas

**Definición y Características**
- **Circuito Combinacional**: Un circuito digital cuyas salidas dependen únicamente del valor actual de sus entradas, sin retroalimentación.
- **Funciones Lógicas**: Implementadas mediante puertas lógicas, se obtienen componiendo operaciones lógicas desde las entradas hasta las salidas.

**Implementación**
- Se describen mediante expresiones booleanas o tablas de verdad.
- **Ejemplo**: Para un circuito con entradas $A$, $B$, $C$ y salidas $f$ y $g$, se componen operaciones para obtener:
  - $f(A,B,C) = AB + (A+B)C$
  - $g(A,B,C) = (AB+(A+B)C)'(A+B+C)+ABC$

**Formas Canónicas**
- **SOP (Suma de Productos)**: Red AND/OR donde las puertas AND realizan productos y la puerta OR realiza la suma.
- **POS (Producto de Sumas)**: Red OR/AND donde las puertas OR realizan sumas y la puerta AND realiza el producto.

**Circuitos Equivalentes**
- Desde una tabla de verdad, las filas donde la función vale 1 definen minitérminos (SOP) y donde vale 0, maxitérminos (POS).

#### 4.2 Optimización de Circuitos Lógicos

**Simplificación**
- Técnicas como K-maps y el algoritmo de Quine-McCluskey se utilizan para obtener expresiones simplificadas de funciones lógicas.

**Puertas Universales**
- **NAND y NOR**: Permiten implementar cualquier función lógica.
- Ejemplo de transformación:
  - Red AND/OR puede ser implementada por puertas NAND.
  - Red OR/AND puede ser implementada por puertas NOR.

**Limitaciones**
- Uso de puertas con entradas limitadas (fan-in) ya que puertas con muchas entradas son más lentas.
- La propiedad asociativa no es válida para puertas NAND y NOR, lo que requiere métodos específicos para combinar estas puertas.

#### 4.3 Análisis de Circuitos Combinacionales

**Proceso de Análisis**
- Partir de un circuito de puertas lógicas para determinar las funciones lógicas equivalentes.
- Utilización de herramientas como Logisim para simular y obtener automáticamente las tablas de verdad y expresiones simplificadas.

**Logisim**
- Colores en Logisim indican el estado de las conexiones (verde oscuro = 0, verde claro = 1, azul = flotante, rojo = error).
- Errores comunes: puertas con entradas no conectadas y pines de E/S mal conectados.
- Uso de buses y buffers triestado para conexiones compartidas.
- Análisis multibit mediante el elemento splitter.

#### 4.4 Diseño de Sistemas Combinacionales

**Proceso de Diseño**
1. **Identificación de Variables de E/S**: Definir nombres y codificación binaria.
2. **Construcción de la Tabla de Verdad**: Basada en la especificación funcional.
3. **Optimización de Funciones de Salida**: Simplificación para obtener el circuito más óptimo.
4. **Implementación del Circuito**: Utilizando puertas lógicas y módulos combinacionales.

**Ejemplo**
- **Circuito de Cálculo de Mayoría**:
  - Entradas: $A$, $B$, $C$.
  - Salida: $f = BC + AC + AB$ (forma simplificada SOP).

**Minimización de Funciones**
- Uso de técnicas como K-maps para obtener las formas SOP y POS simplificadas.
- Implementación utilizando puertas NAND o NOR, según sea necesario.

**Diseño Automatizado**
- Herramientas como Logisim permiten obtener diagramas lógicos optimizados, aunque pueden generar redundancia en inversores que requiere revisión manual.

### Conceptos Clave
- **Circuitos Combinacionales**: Salidas dependen de entradas actuales.
- **Optimización**: Uso de técnicas algebraicas y puertas universales.
- **Herramientas de Simulación**: Logisim para diseño y análisis automatizado.
- **Proceso de Diseño**: Identificación, construcción, optimización e implementación.

Este capítulo ofrece una comprensión detallada de los circuitos digitales combinacionales, abarcando desde su definición y características hasta las técnicas de diseño y optimización empleadas para su implementación eficiente.

