# osorio-post1-u3

Checkpoint 1: Inspección de Registros (Comando R)
Descripción técnica:
Se ejecutó el comando R (Registers) para realizar una captura del estado inicial del procesador x86 en el entorno DOSBox.
Se verificó que los registros de propósito general (AX, BX, CX, DX) se encuentran inicializados en 0000.
El registro IP (Instruction Pointer) se sitúa en la dirección 0100h, que representa la primera dirección de memoria ejecutable inmediatamente después del Program Segment Prefix (PSP).
Se documentó la modificación del registro AX mediante el comando R AX, asignándole el valor hexadecimal 1234.
Esta acción permite confirmar que el depurador puede manipular selectivamente el contenido de los registros sin afectar el resto del estado del procesador.

Checkpoint 2: Gestión de Memoria (Comandos F y D)
Análisis de la operación:
Se utilizó el comando F (Fill) para inicializar un bloque de 64 bytes (L40) a partir de la dirección DS:0200 con el patrón cíclico AB CD EF.
Posteriormente, se empleó el comando D (Dump) para volcar el contenido de dicha región y verificar la correcta escritura del patrón en la memoria RAM.
Análisis de columnas del volcado:
1. Dirección (Segmento:Offset): Indica la ubicación lógica de los datos, en este caso bajo el segmento de datos asignado por el DOS.
2. Contenido Hexadecimal: Muestra los valores AB, CD y EF en base 16, que es la representación cruda de los datos en memoria.
3. Contenido ASCII: Muestra puntos (.) debido a que los valores utilizados no corresponden al rango de caracteres imprimibles (0x20-0x7E).
Adicionalmente, se exploró el área del PSP (D 0 L20), identificando los bytes CD 20 en la dirección inicial, los cuales corresponden a la instrucción de terminación INT 20 colocada por el sistema operativo.

