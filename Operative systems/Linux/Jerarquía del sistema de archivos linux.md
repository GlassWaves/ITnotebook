---
tags:
  - Notes
  - OperativeSystems
  - Linux
---
El estándar de jerarquía de archivos que utiliza Linux es FHS

![[img.Jerarquia del sistema de archivos linux.png|Jerarquía de archivos en Linux]]

# Directorios

| Directorio | Descripción                                                                                                                                                                                                             |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `/`        | Contiene todos los archivos necesarios para arrancar el sistema operativo antes de que se monten otros sistemas de archivos, así como los archivos necesarios para arrancar los otros sistemas de archivos              |
| `/bin`     | Contiene binarios de comandos esenciales                                                                                                                                                                                |
| `/boot`    | Consta del cargador de arranque estático, el ejecutable del kernel y los archivos necesarios para arrancar el sistema operativo Linux                                                                                   |
| `/dev`     | Contiene archivos de dispositivo para facilitar el acceso a todos los dispositivos de hardware conectados al sistema                                                                                                    |
| `/etc`     | Archivos de configuración del sistema local. Los archivos de configuración de las aplicaciones instaladas también se pueden guardar aquí                                                                                |
| `/home`    | Cada usuario del sistema tiene un subdirectorio aquí para el almacenamiento                                                                                                                                             |
| `/lib`     | Archivos de biblioteca compartida que son necesarios para el arranque del sistema                                                                                                                                       |
| `/media`   | Aquí se montan dispositivos de medios extraíbles externos, como unidades USB                                                                                                                                            |
| `/mnt`     | Punto de montaje temporal para sistemas de archivos normales                                                                                                                                                            |
| `/opt`     | Aquí se pueden guardar archivos opcionales, como herramientas de terceros                                                                                                                                               |
| `/root`    | El directorio de inicio del usuario raíz                                                                                                                                                                                |
| `/sbin`    | Este directorio contiene ejecutables utilizados para la administración del sistema (archivos binarios del sistema)                                                                                                      |
| `/tmp`     | El sistema operativo y muchos programas utilizan este directorio para almacenar archivos temporales. Este directorio generalmente se borra al arrancar el sistema y puede eliminarse en otros momentos sin previo aviso |
| `/usr`     | Contiene ejecutables, bibliotecas, archivos man, etcétera                                                                                                                                                               |
| `/var`     | Este directorio contiene archivos de datos variables, como archivos de registro, bandejas de entrada de correo electrónico, archivos relacionados con aplicaciones web, archivos cron y más                             |