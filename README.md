# osorio-post1-u3

Checkpoint 1: Inspección de Registros (Comando R)
Descripción técnica:
Se ejecutó el comando R (Registers) para realizar una captura del estado inicial del procesador x86 en el entorno DOSBox.
Se verificó que los registros de propósito general (AX, BX, CX, DX) se encuentran inicializados en 0000.
El registro IP (Instruction Pointer) se sitúa en la dirección 0100h, que representa la primera dirección de memoria ejecutable inmediatamente después del Program Segment Prefix (PSP).
Se documentó la modificación del registro AX mediante el comando R AX, asignándole el valor hexadecimal 1234.
Esta acción permite confirmar que el depurador puede manipular selectivamente el contenido de los registros sin afectar el resto del estado del procesador.


