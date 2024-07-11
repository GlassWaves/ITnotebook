---
tags:
  - Notes
  - "#DB"
---
>Unidad de trabajo lógica que involucra por lo regular a varias operaciones de [[Bases de datos]]
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p79

# Características
| Característica | Definición                                                                                                                                                                                  |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Atómica        | Se garantiza (desde un punto de vista lógico) que se ejecuten en su totalidad o que no se ejecuten en lo absoluto                                                                           |
| Durable        | Una vez que se ejecuta una transacción con éxito se debe de garantizar que sus actualizaciones sean aplicadas a la base de datos                                                            |
| Aislada        | Las actualizaciones hechas a la base de datos por una determinada transacción `T1` no son visibles para ninguna transacción distinta `T2`, por lo menos hasta que `T1` se ejecute con éxito |
Definiciones obtenidas de [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p75