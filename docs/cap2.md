### Capítulo 2: Sistemas de Numeración

#### 2.1 Sistema Decimal
El sistema decimal, de base 10, utiliza 10 dígitos (0-9) y es un sistema posicional aditivo. Cada posición en un número tiene un valor que es una potencia de 10, aumentando de derecha a izquierda. Los números con parte fraccionaria extienden este sistema con exponentes negativos.

#### 2.2 Sistema Binario Natural
El sistema binario, de base 2, utiliza los dígitos 0 y 1. Cada posición de un número binario representa una potencia de 2. El sistema binario se usa ampliamente en sistemas digitales por su facilidad de representación en dispositivos electrónicos.

#### 2.3 Rango de Representación y Otras Bases Numéricas
El rango de representación de un sistema numérico depende de su base y del número de dígitos utilizados. El total de números representables es (base)^n, donde n es el número de dígitos. Para bases mayores que 2, se utilizan sistemas como el octal (base 8) y hexadecimal (base 16) que son potencias de 2, lo que facilita la conversión entre ellos y el binario.

#### 2.4 Conversión entre Sistemas de Base Diferente
- **Conversión a Base Decimal**: Se calcula la suma del producto de cada dígito por la potencia de la base correspondiente.
- **Conversión desde Decimal**: Se divide sucesivamente para la parte entera y se multiplica sucesivamente para la parte fraccionaria.
- **Conversión entre Bases Potencias de 2**: Se agrupan bits según la base destino (ej., 3 bits para octal y 4 bits para hexadecimal).

#### 2.5 Otros Códigos Binarios
- **BCD (Binary Coded Decimal)**: Representa dígitos decimales usando 4 bits por dígito.
- **Código Gray**: Entre códigos consecutivos solo cambia un bit, útil para minimizar errores en sistemas digitales.
- **Códigos One-Hot y One-Cold**: Se utilizan en sistemas de control, donde solo un bit está encendido o apagado respectivamente.
- **Código ASCII**: Facilita la representación de caracteres y símbolos en sistemas informáticos, usando 7 o 8 bits por carácter.

#### 2.6 Aritmética en el Sistema Binario
- **Suma Binaria**: Sigue reglas simples, con acarreo cuando ambos bits son 1.
- **Resta Binaria**: Similar a la decimal, con acarreo negativo.
- **Multiplicación y División**: Operaciones de suma desplazada y restas sucesivas respectivamente.
- **Representación de Números Enteros con Signo**:
  - **Signo Magnitud (SM)**: Utiliza el bit más significativo para el signo.
  - **Complemento a 1 (C1)**: Inversión de todos los bits para representar números negativos.
  - **Complemento a 2 (C2)**: Se obtiene sumando 1 al complemento a 1 del número. Permite una aritmética más sencilla sin necesidad de tratar el acarreo final.
  - **Aritmética en C2**: Todas las operaciones se realizan como sumas, descartando el acarreo final.

### Conceptos Clave
1. **Sistemas Posicionales**: Utilización de bases como 10, 2, 8 y 16 para representar números.
2. **Conversión de Bases**: Métodos para convertir números entre diferentes bases.
3. **Codificación Binaria**: Incluye códigos como BCD, Gray, ASCII, y otros.
4. **Aritmética Binaria**: Reglas para suma, resta, multiplicación y división.
5. **Representación de Números con Signo**: Utilización de SM, C1 y C2 para representar números negativos.
6. **Desbordamiento**: Manejo del error cuando el resultado de una operación excede el rango representable.

Este capítulo proporciona una comprensión integral de cómo los números y códigos se representan y manipulan en sistemas digitales, sentando las bases para operaciones más complejas en computación y electrónica.

