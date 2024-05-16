### Capítulo 7: Biestables

#### 7.1 Circuitos Digitales Realimentados

**Definición**
- Los circuitos secuenciales son aquellos cuya salida depende no solo de las entradas actuales, sino también de su historia previa. Esto requiere elementos capaces de almacenar información, llamados biestables.

**Acciones Momentáneas vs. Memorizadas**
- **Momentáneas**: Se producen mientras la condición de activación se cumple.
- **Memorizadas**: Se inician con una condición de set y se mantienen hasta una condición de reset.

**Estado de un Sistema Digital**
- El estado se representa con la letra $Q$ y se mantiene hasta que un cambio lo modifique.

**Modos de Cambio de Estado**
- **Asíncrono**: Cambio inmediato tras la modificación de las entradas.
- **Síncrono**: Cambio de estado controlado por una señal de sincronismo (reloj).

#### 7.1.1 Biestable S-R Asíncrono
- **Latch S-R**: Mantiene su estado mientras  $S = R = 0$. Si $S = 1$ y $R = 0$, entonces $Q = 1$; si $S = 0$ y $R = 1$, entonces $Q = 0$.
- **Problema**: Situación prohibida cuando $S = R = 1$.

#### 7.1.2 Biestable S-R Activado por Nivel
- Añade una señal de habilitación ($en$) que permite cambiar el estado solo cuando está activa.
- **Circuito**: Puertas AND en las entradas del latch para controlar la habilitación.

#### 7.1.3 Biestable D
- Evita la condición prohibida del biestable S-R conectando las entradas $S$ y $R$ a través de un inversor.
- **Función**: Almacena el valor de la entrada $D$ cuando está habilitado.

#### 7.1.4 Biestables Disparados por Flanco
- Utilizan un pulso de activación generado en los flancos de la señal de sincronismo para cambiar de estado.
- **Biestable S-R Disparado por Flanco**: Cambia de estado solo en el flanco de sincronismo.
- **Biestable D Disparado por Flanco**: Captura el valor de la entrada $D$ en el flanco de sincronismo.

#### 7.1.5 Biestable J-K
- Modificación del S-R que evita el estado indeterminado con $J = K = 1$.
- **Función**: Si $J = K = 1$, conmuta el valor del estado del biestable.

#### 7.1.6 Biestable T
- Derivado del J-K, con las entradas $J$ y $K$ unidas. Conmuta su estado cuando $T = 1$.

#### 7.1.7 Ajuste Asíncrono del Estado
- **Preset (PRE) y Clear (CLR)**: Permiten ajustar el estado del biestable a 1 o 0 de manera asíncrona.

#### 7.2 Simulación de Circuitos con Biestables en Logisim
- Logisim permite la simulación de biestables mediante su librería de memoria.
- **Atributos**: El modo de sincronismo y las señales de preset, clear y enable.

#### 7.3 Caracterización de Biestables

**Tablas de Transición y Excitación**
- **Tabla de Transición**: Añade el estado inicial ($Q_t$) y el estado resultante ($Q_{t+1}$).
- **Tabla de Excitación**: Determina las entradas necesarias para cada cambio de estado.

**Ecuación Característica**
- Fórmula que relaciona el estado resultante ($Q_{t+1}$) con el estado de partida ($Q_t$) y las entradas.

**Intercambio de Biestables**
- Transformación de un tipo de biestable a otro mediante puertas lógicas adicionales.

**Características Operativas de Biestables Reales**
- **Tiempo de Establecimiento**: Tiempo mínimo antes del flanco de disparo.
- **Tiempo de Mantenimiento**: Tiempo mínimo después del flanco de disparo.
- **Retardo de Propagación**: Tiempo desde el flanco de disparo hasta el cambio de salida.
- **Frecuencia Máxima del Reloj**: Máxima velocidad de disparo fiable.
- **Anchura Mínima de Pulso**: Ancho mínimo del pulso de reloj, preset y clear.
- **Disipación de Potencia**: Potencia consumida durante el funcionamiento.

### Conceptos Clave
- **Circuitos Realimentados**: Necesitan elementos de memoria para almacenar estados.
- **Biestables**: Elementos básicos de memoria que pueden ser síncronos o asíncronos.
- **Simulación en Logisim**: Herramienta para visualizar y probar el comportamiento de biestables y otros circuitos secuenciales.
- **Caracterización y Ecuaciones**: Tablas y ecuaciones para describir y diseñar el comportamiento de biestables.

Este capítulo introduce los conceptos fundamentales de los circuitos secuenciales, enfocándose en los biestables y sus diversas configuraciones y aplicaciones en sistemas digitales.

