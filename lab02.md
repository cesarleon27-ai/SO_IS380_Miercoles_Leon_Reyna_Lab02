# Laboratorio 02: Instalación y prueba de xv6

## Parte A: Ejecución de comandos en xv6

Llamada al comando ls para ver las carpetas existentes:

![Comando ls](img/ParteA_01.png)

Impresión de texto y validación de datos del estudiante:

![Comando echo](img/ParteA_02.png)

Creación de directorio nuevo y verificación en el sistema:

![Comando mkdir](img/ParteA_03.png)

Lectura del archivo de texto README incluido en el sistema:

![Comando cat README](img/ParteA_04.png)

Redirección de texto para creación de archivo nuevo y lectura de verificación:

![Redirección y cat](img/ParteA_05.png)

Conteo de líneas y palabras del archivo, finalizando con el cierre de QEMU:

![Comando wc](img/ParteA_06.png)

## Parte B: Ejecución de xv6 y QEMU

Arranque y funcionamiento del sistema operativo xv6 en el entorno QEMU:

![Parte B](img/ParteB.png)

## Parte C: Interfaz e implementación de llamadas al sistema

Resultados de búsqueda con grep para la llamada `fork`:
* Interfaz: `kernel/syscall.h:2:#define SYS_fork 1`
* Implementación: `kernel/sysproc.c:26:sys_fork(void)`

Resultados de búsqueda con grep para la llamada `read`:
* Interfaz: `kernel/syscall.h:6:#define SYS_read 5`
* Implementación: `kernel/sysfile.c:69:sys_read(void)`

![Parte C](img/ParteC.png)

## Parte D: Reflexión

**¿Qué diferencia se observa entre la interfaz de una llamada al sistema y su implementación interna?**

La interfaz (ubicada en los archivos de cabecera `.h`) opera únicamente como un identificador numérico o firma que expone y registra el servicio disponible para los programas de usuario. En contraste, la implementación (ubicada en los archivos de código fuente `.c`) contiene la lógica algorítmica completa, el manejo de estructuras y las instrucciones reales que el núcleo del sistema operativo ejecuta en el procesador.
