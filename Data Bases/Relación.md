---
tags:
  - Notes
  - RDB
---
# Estructura
![[img.Relacion.png]]

| Termino relacional formal | Equivalente informal |
| ------------------------- | -------------------- |
| Relación                  |                      |
| Tupla                     |                      |
| Cardinalidad              |                      |
| Atributo                  |                      |
| Grado                     |                      |
| Clave primaria            |                      |
| Dominio                   |                      |

# Tipos y relaciones
> - Los `tipos` son (conjuntos de) cosas de las que podemos hablar
> - Las `relaciones` son (conjuntos de) cosas que decimos acerca de las cosas de las que podemos hablar
> [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p66

>Los `tipos` son a las `relaciones` lo que los `sustantivos` son a las `oraciones`.
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p66

>Los `tipos` y las `relaciones` son necesarios y suficientes para representar cualquier dato que queramos (esto es, al nivel lógico)
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p79

> Dada una relación `r` , el encabezado de `r` denota un cierto `predicado` o `función valuada` como `verdadera`
> [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p66

>Cada fila en el cuerpo de `r` denota una cierta `proposición verdadera`, obtenida del `predicado` por medio de la sustitución de ciertos valores de argumento
>[[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p66

# Elementos
| Elemento   | Descripción                                          |
| ---------- | ---------------------------------------------------- |
| Encabezado | Conjunto de parejas nombre_de_columna:nombre_de_tipo |
| Cuerpo     | Conjunto de filas que se apegan al encabezado        |
Definiciones obtenidas de [[src.Introduccion a Los Sistemas de Bases de Datos|C.J. Date]] - p79
## Interpretación semántica
Por ejemplo de la relación `Empleado`:

| idEmpleado | nombre   | idDepartamento | salario |
| ---------- | -------- | -------------- | ------- |
| 1          | Lopez    | 1              | 40000   |
| 2          | Cheng    | 2              | 42000   |
| 3          | Smith    | 4              | 30000   |
| 4          | Vladimir | 4              | 15000   |

### Predicado
El empleado `idEmpleado` se llama `nombre`, trabaja en el departamento `idDepartamento` y gana un salario de `salario`

Parámetros :
- idEmpleado
- nombre
- idDepartamento
- salario

### Proposición verdadera
El empleado `1` se llama `Lopez`, trabaja en el departamento `idDepartamento` y gana un salario de `40000`

