---
tags:
  - Notes
  - OperativeSystems
  - Linux
---
# Símbolo del sistema
>Cadena de caracteres que se muestra en la pantalla del terminal y que indica que el sistema está listo para nuestra entrada
>[[src.Linux Fundamentals|HackTheBox : Linux Fundamentals]]

# Estructura
```Bash
<username>@<hostname><directorio actual>$
```
## Información por default
- Usuario
- Nombre de host
- Directorio actual
## Simbolos

| Simbolo | Descripción                        |
| ------- | ---------------------------------- |
| `~`     | Directorio de inicio de un usuario |
| `$`     | Usuario                            |
# Configuración
La configuración de la información que se muestra en el prompt se encuentra en `.bashrc`, este se puede configurar con `caractacteres especiales` para personalizar la información por ejemplo con :

```Bash
.bashrc\u\h\w
```
Se muestra el usuario actual, nombre del host y directorio actual.

## Caracteres especiales
|**Carácter especial**|**Descripción**|
|---|---|
|`\d`|Fecha (lun 6 de febrero)|
|`\D{%Y-%m-%d}`|Fecha (AAAA-MM-DD)|
|`\H`|Nombre de host completo|
|`\j`|Número de trabajos gestionados por el shell|
|`\n`|Newline|
|`\r`|Retorno de carro|
|`\s`|Nombre de la cáscara|
|`\t`|Hora actual 24 horas (HH:MM:SS)|
|`\T`|Hora actual 12 horas (HH:MM:SS)|
|`\@`|Hora actual|
|`\u`|Nombre de usuario actual|
|`\w`|Ruta completa del directorio de trabajo actual|
## Herramientas externas
[Bash Prompt Generator](https://bash-prompt-generator.org/) : Te ayuda generar el prompt para configurar el bash

