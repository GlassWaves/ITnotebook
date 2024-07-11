>Variables de relación; es decir, variables cuyos valores son valores de relación (diferentes valores de [[Relación]] en diferentes momentos)
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p64


# Ejemplo
Tenemos la tabla `Empleado` cuyo valor actual  es de cuatro filas :

| idEmpleado | nombre   | idDepartamento | salario |
| ---------- | -------- | -------------- | ------- |
| 1          | Lopez    | 1              | 40000   |
| 2          | Cheng    | 2              | 42000   |
| 3          | Smith    | 4              | 30000   |
| 4          | Vladimir | 4              | 15000   |
Si eliminamos la fila 4 entonces ahora `Empleado` tiene un valor de tres filas:

| idEmpleado | nombre | idDepartamento | salario |
| ---------- | ------ | -------------- | ------- |
| 1          | Lopez  | 1              | 40000   |
| 2          | Cheng  | 2              | 42000   |
| 3          | Smith  | 4              | 30000   |

> De manera conceptual, lo que sucedió aquí es que el valor de relación anterior de `Empleado` fue remplazado en bloque por un valor de relación completamente nuevo
> [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]]

```TutorialD
Empleado := Empleado MINUS (Empleado WHERE idEmpleado = 4) 
```
