>Variables de relación; es decir, variables cuyos valores son valores de relación (diferentes valores de [[Relación|relación]] en diferentes momentos)
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p64


# Ejemplo
Tenemos la [[Relación|relación]] ``Empleado`` cuyo valor actual  es de cuatro filas :

| idEmpleado | nombre   | departamento | salario |
| ---------- | -------- | ------------ | ------- |
| 1          | Lopez    | 1            | 40000   |
| 2          | Cheng    | 2            | 42000   |
| 3          | Smith    | 4            | 30000   |
| 4          | Vladimir | 4            | 15000   |
```Tutorial D
Empleado := Empleado MINUS ( Empleado WHERE idEmpleado = 1)
```