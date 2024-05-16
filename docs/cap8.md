### Capítulo 8: Registros y Contadores

#### 8.1 Registros de Desplazamiento

**Definición y Aplicación**
- **Registro**: Circuito digital síncrono que almacena y desplaza un conjunto de n bits.
- Utilizan biestables D para almacenamiento de datos temporales, direcciones de memoria y datos relacionados con operaciones de lectura/escritura.

**Tipos de Registros**
1. **E/S en Paralelo**:
   - Almacenan y transfieren todos los bits de entrada/salida simultáneamente.
   - Implementación sencilla con biestables D, sincronizados por un reloj común.

2. **E/S en Serie (Shift Registers)**:
   - Los datos se desplazan de un biestable a otro con cada pulso de reloj.
   - Ejemplo: Registro de desplazamiento hacia la derecha de 4 bits.

3. **Serie a Paralelo (SIPO)**:
   - Los datos se ingresan en serie y se acceden en paralelo.
   - Proporciona acceso inmediato al contenido del registro.

4. **Paralelo a Serie (PISO)**:
   - Permite entrada en paralelo y salida en serie.
   - Funciona con una señal de control para alternar entre carga y desplazamiento.

5. **Bidireccionales y Universales**:
   - Permiten desplazamiento en ambas direcciones (izquierda y derecha).
   - Los registros universales permiten la carga en paralelo y tienen señales de habilitación para control avanzado.

#### 8.2 Contadores

**Definición y Aplicación**
- **Contador**: Circuito secuencial que genera una secuencia de valores únicos en su salida.
- Utilizados para divisores de frecuencia, temporizadores, contadores de eventos y generadores de secuencias cíclicas.

**Clasificación de Contadores**
1. **Sincronismo**:
   - **Síncrono**: Todos los biestables comparten la misma señal de reloj, asegurando cambios simultáneos.
   - **Asíncrono**: Cada biestable se sincroniza con la salida del anterior, introduciendo retardo de propagación.

2. **Codificación**:
   - Secuencia binaria, BCD, código Gray, etc.

3. **Ordenación de la Secuencia**:
   - Ascendente o descendente, dependiendo del orden de los valores generados.

4. **Módulo**:
   - **Completo**: Secuencia que usa todos los estados posibles.
   - **Incompleto**: Secuencia que omite algunos estados, como el contador MOD 10 (contador de décadas).

**Implementación de Contadores**
1. **Contador Asíncrono (Ripple Counter)**:
   - Ejemplo: Contador ascendente MOD 8 usando biestables T.
   - El cambio de estado en los biestables se propaga en cascada, causando rizado.

2. **Contador Síncrono**:
   - Todos los biestables cambian de estado simultáneamente con el reloj.
   - Ejemplo: Contador ascendente MOD 8 con biestables T.
   - Más rápido y preciso, sin retardo acumulado.

3. **Truncamiento**:
   - **Asíncrono**: Usa una puerta lógica para reiniciar el contador al alcanzar un valor específico.
   - **Síncrono**: Modifica las señales de excitación para evitar valores no deseados.

4. **Contadores Basados en Registros de Desplazamiento**:
   - **Contador en Anillo**: Realimenta la salida del último biestable a la entrada del primero.
   - **Contador Johnson**: Realimenta la salida negada del último biestable a la entrada del primero.
   - Utilizados para generar secuencias cíclicas con aplicaciones específicas como divisores de frecuencia.

**Aplicaciones de Contadores**
- **Contadores de Eventos**: Cuentan ocurrencias de eventos asíncronos como personas o vehículos.
- **Temporizadores**: Actúan como temporizadores para activar o desactivar señales después de un tiempo determinado.

### Conceptos Clave
- **Registros de Desplazamiento**: Diferentes tipos y su uso para almacenamiento y desplazamiento de datos.
- **Contadores**: Clasificación, implementación y aplicaciones prácticas.
- **Sincronismo vs. Asincronismo**: Impacto en el diseño y rendimiento de contadores.
- **Truncamiento**: Métodos para limitar secuencias en contadores.
- **Contadores Basados en Registros de Desplazamiento**: Contador en anillo y Johnson para aplicaciones específicas.

Este capítulo profundiza en el funcionamiento y diseño de registros y contadores, componentes esenciales en sistemas secuenciales digitales, abordando tanto sus implementaciones prácticas como sus aplicaciones en sistemas reales.

