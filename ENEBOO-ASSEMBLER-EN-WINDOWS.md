* CREADO POR: miguelajsmaps@gmail.com
* MODIFICADO POR: miguelajsmaps@gmail.com
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ÚLTIMA ACTUALIZACIÓN: 13 de febrero de 2016
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/ENEBOO-ASSEMBLER-EN-WINDOWS)

----

# ENEBOO-ASSEMBLER EN WINDOWS

###INSTALACIÓN PREVIA (Dependencias): 

PASO 1:  INSTALAR PYTHON. Visitar la página:

https://github.com/Miguel-J/eneboo/wiki/Eneboo-Tools-en-Windows

---

PASO 2:  DESCARGAR eneboo-modules y eneboo-features. Visitar la página:

https://github.com/Miguel-J/eneboo/wiki/GITHUB-COMO-INSTALARLO-Y-USARLO

Abrir GIT-SHELL.

Recomiendo:

1. eneboo-modules: el de Eneboo-Oficial:

     git clone https://github.com/eneboo/eneboo-modules

2. ... y eneboo-features: el de KLO-MANOLO:

     git clone https://github.com/klo-manolo/eneboo-features

---

PASO 3: PREPARAR ASSEMBLER:

Eneboo-assembler es una herramienta de "collage" de código fuente. Toma como base unos módulos y les aplica una serie de parches en un orden determinado para conseguir un proyecto modificado de cierta forma, que cumpla ciertas especificaciones.

Este comando tiene unas configuraciones y una base de datos de caché. Para que genere los primeros ficheros es conveniente lanzar la acción "dbupdate":

    C:\eneboo-tools> python eneboo-assembler dbupdate

Respuesta:

       Traceback (most recent call last):
         File "eneboo-assembler", line 3, in <module>
           from enebootools.assembler import config, AssemblerInterface
         File "C:\eneboo-tools\enebootools\assembler\__init__.py", line 4, in <module>
           from enebootools.assembler import database as asmdb
         File "C:\eneboo-tools\enebootools\assembler\database.py", line 6, in <module>
           import readline, fnmatch
       ImportError: No module named readline

C:\eneboo-tools>

---

* PASO 5: CONFIGURACIÓN DE ENEBOO-TOOLS (Esta página)
     * PASO 5-A: CONFIGURACIÓN INICIAL DE ASSEMBLER: 
        * PASO 5-A-1.-Introducción-para qué sirve:
        * PASO 5-A-2.-Assembler: Configuración previa:
        * OPCIÓN: AÑADIR REPOSITORIOS PARTICULARES A LA MEZCLA: 
        * PASO 5-A-3.- ACTUALIZAR CAMBIOS DE RUTAS A LOS REPOSITORIOS:
     * PASO 5-B : ASSEMBLER "NEW" - (ASISTENTE AUTOMÁTICO PARA CREAR PROYECTOS o EXTENSIONES o SET´s):
     * PASO 5-C : ASSEMBLER "BUILD" - (COMPILAR/CREAR UN PROYECTO) :

--------------

###PASO 5-A: CONFIGURACIÓN INICIAL DE ASSEMBLER: 

