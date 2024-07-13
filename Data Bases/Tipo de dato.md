---
tags:
  - Notes
  - DB
  - RDB
---
> Conjunto de valores -*todos los valores posibles del tipo en cuestión*
>  [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p112

Este conjunto de valores a su vez tiene `operadores` definidos exclusivamente para el mismo.
# Ejemplo
| Tipo          | Valores posibles                                 | operadores                                              |
| ------------- | ------------------------------------------------ | ------------------------------------------------------- |
| `INTEGER`     | Conjunto de todos los enteros posibles           | `=,<,>,*,+,-,÷`                                         |
| `idProveedor` | Conjunto de todos los id's de proveedor posibles | No tiene operadores definidos por que no son necesarios |
# Tipos fuertes
>Todo valor tiene un tipo y que siempre que tratemos de realizar una operación, el sistema comprueba que los operandos son del tipo correcto para la operación en cuestión
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p113

## Ejemplo
Siendo `P` la relación `Partes` y `VP` de `Envío` tenemos que :

`P.Peso + VP.Cantidad`
No tiene sentido por que a pesar de tener la misma`representació fisica` (numérica), es ilógico sumar el peso de un tornillo con la cantidad de tornillos del envío

`P.Peso * VP.Cantidad`
Tiene sentido por que se esta calculando el peso de un envío

Y de hecho, esta comprobación de operandos tiene que ver con el [[Modelado semántico]]
# No escalar
> Esta definido explícitamente para tener componentes visibles para el usuario
> [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p115

## Ejemplo
De la relación `Envio(idEnvio,proveedor,)`
