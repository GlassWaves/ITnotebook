> Conjunto de valores -*todos los valores posibles del tipo en cuestión*
>  [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p112

Este conjunto de valores a su vez tiene `operadores` definidos exclusivamente para el mismo.
# Ejemplo
`INTEGER` es el conjunto de todos los enteros posibles
`idProveedor` es el conjunto de todos los id's de proveedor posibles

`INTEGER` tiene los operadores `=,<,>,*,+,-,÷`
`idProveedor` no tiene operadores definidos por que no son necesarios

# Tipos fuertes
>Todo valor tiene un tipo y que siempre que tratemos de realizar una operación, el sistema comprueba que los operandos son del tipo correcto para la operación en cuestión
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p113

## Ejemplo
Siendo `P` la relación `Partes` y `VP` de `Envío` tenemos que :

`P.Peso + VP.Cantidad`
No tiene sentido por que a pesar de tener la misma`representació fisica` (numérica), es ilógico sumar el peso de un tornillo con la cantidad de tornillos del envió

`P.Peso * VP.Cantidad` : 
