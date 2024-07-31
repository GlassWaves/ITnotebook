# ¡Hola!
Este cuaderno registra temas de TI que investigo en mis ratos libres :D

Está construido con la tecnología de [obsidian](https://obsidian.md/), el cual utiliza el lenguaje de marcado [markdown](https://es.wikipedia.org/wiki/Markdown). Sin embargo, tiene algunos ligeros cambios en la sintaxis que impiden leer al 100% el documento en Markdown simple, por lo que es recomendable que, al descargar este `vault`, lo leas mediante el editor de `Obsidian` con los correspondientes `plugins` habilitados.

# Tabla de contenido
- [Estructura](#estructura)
- [Tipos de notas](#tipos-de-notas)
  - [Notes](#notes)
  - [Sources](#sources)
- [Directorios especiales](#directorios-especiales)
  - [Annexes](#annexes)
  - [Templates](#templates)

# Estructura
El cuaderno está estructurado mediante notas atómicas agrupadas bajo temas genéricos (directorio/tag), por ejemplo: la nota *Conjunto abierto* pertenece al tema de *Teoría de conjuntos* pero su tema genérico es *Matemáticas*. Esto es para simplificar la jerarquía de los directorios y de las notas en sí.

# Tipos de notas
## Notes
Notas simples cuyo contenido sigue el `principio de atomicidad`, el cual a grandes rasgos trata sobre reducir al mínimo posible las temáticas que se desarrollan en una sola nota.

### Propiedades
- `tags`: Son los tags que identifican la temática de la nota.
  - Por defecto tienen los tags #Notes, /#TemaGenerico, sin embargo, se les puede complementar con algún tag extra.
- *`aliases`: A veces las notas tienen aliases (no todas tienen).
  - Ejemplo: el título de la nota es "World Wide Web", pero su alias es "WWW".

## Sources
Estas notas registran las fuentes que son utilizadas en las `Notes`. Las notas deben ser tituladas con la siguiente estructura:

"src." + "Título original de la fuente sin caracteres especiales".

### Propiedades
- `tags`: Son los tags que identifican la temática de la fuente.
  - Por defecto tienen los tags #Sources, /#TemaGenerico, sin embargo, se les puede complementar con algún tag extra.
- `reference`: Archivo, link web, ISBN-13 o DOI de la fuente consultada.
- `aliases`: Alias de las fuente.
  - Por defecto se debe de incluir al menos un alias, para evitar usar sus iniciales "src."

# Directorios especiales
## Annexes
En este directorio se almacenan imágenes, PDFs, hojas de cálculo o cualquier archivo (no Markdown) que se anexen en las notas. El nombre del archivo debe seguir la siguiente estructura:

"Tipo de archivo." + "Nombre de la primera nota en la que es anexado" + "Número".

`Tipo de archivo`
- img: Imágenes
- pdf: PDF
- exl: Hojas de cálculo
- cod: Código

`Número`
- Si una nota tiene más de un archivo anexado, se deben de enumerar los nombres de los anexos.

## Templates
Este directorio almacena los templates de las notas. El nombre del template debe seguir la siguiente estructura:

"tpl." + "Nombre genérico del template".
