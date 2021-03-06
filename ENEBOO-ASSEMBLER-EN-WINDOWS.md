* CREADO POR: miguelajsmaps@gmail.com
* MODIFICADO POR: miguelajsmaps@gmail.com
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ÚLTIMA ACTUALIZACIÓN: 13 de marzo de 2016
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/ENEBOO-ASSEMBLER-EN-WINDOWS)

----

# ENEBOO-ASSEMBLER EN WINDOWS

###INSTALACIÓN PREVIA (Dependencias): 

####PASO 1:  INSTALAR PYTHON. Visitar la página:

https://github.com/Miguel-J/eneboo/wiki/Eneboo-Tools-en-Windows

---

####PASO 2:  DESCARGAR eneboo-modules y eneboo-features. Visitar la página:

https://github.com/Miguel-J/eneboo/wiki/GITHUB-COMO-INSTALARLO-Y-USARLO

Abrir GIT-SHELL.

Recomiendo:

1. eneboo-modules: el de Eneboo-Oficial:

     git clone https://github.com/eneboo/eneboo-modules

2. ... y eneboo-features: el de KLO-MANOLO:

     git clone https://github.com/klo-manolo/eneboo-features

---

####PASO 3: PREPARAR ASSEMBLER (primer intento):

Eneboo-assembler es una herramienta de "collage" de código fuente. Toma como base unos módulos y les aplica una serie de parches en un orden determinado para conseguir un proyecto modificado de cierta forma, que cumpla ciertas especificaciones.

Este comando tiene unas configuraciones y una base de datos de caché. Para que genere los primeros ficheros es conveniente lanzar la acción "dbupdate":

    C:\eneboo-tools> python eneboo-assembler dbupdate

* **ERROR CONOCIDO** Si aparece esta respuesta:

         C:\eneboo-tools> python eneboo-assembler dbupdate

         Traceback (most recent call last):
           File "eneboo-assembler", line 3, in <module>
             from enebootools.assembler import config, AssemblerInterface
           File "C:\eneboo-tools\enebootools\assembler\__init__.py", line 4, in <module>
             from enebootools.assembler import database as asmdb
           File "C:\eneboo-tools\enebootools\assembler\database.py", line 6, in <module>
             import readline, fnmatch
         ImportError: No module named readline

....es que FALTA INSTALAR el paquete-librería "pyreadline 2.1". 

####PASO 4: INSTALAR EL paquete-librería "pyreadline 2.1". 

Descargarlo de:

     https://pypi.python.org/pypi/pyreadline

....yo "bajo" la versión "pyreadline-2.1.win-amd64.exe (md5) 64-bit" y se instala automáticamente en mi directorio "c\python27"...

---

####PASO 3: PREPARAR ASSEMBLER (segundo intento):

    C:\eneboo-tools> python eneboo-assembler dbupdate

Respuesta:

        INFO: agregando la seccion 'module'
        INFO: Escribiendo valor ['~/git/eneboo-modules'] para parametro 'modulefolders' (seccion 'module')
        INFO: Escribiendo valor ['~/git/eneboo-features'] para parametro 'featurefolders' (seccion 'module')
        INFO: Escribiendo valor '~/.eneboo-tools/buildcache' para parametro 'buildcache' (seccion 'module')
        INFO: agregando la seccion 'mergetool'
        INFO: Escribiendo valor 'warn' para parametro 'patch_qs_rewrite' (seccion 'mergetool')
        INFO: Escribiendo valor 'legacy' para parametro 'patch_qs_style_name' (seccion 'mergetool')
        INFO: Escribiendo valor 0 para parametro 'verbosity_delta' (seccion 'mergetool')
        INFO: Escribiendo valor 'legacy1' para parametro 'patch_xml_style_name' (seccion 'mergetool')
        INFO: Escribiendo valor False para parametro 'diff_xml_search_move' (seccion 'mergetool')
        CacheSqlite:: Se ha recreado la tabla knownobjects.


---
* PASO 5: CONFIGURACIÓN DE ENEBOO-TOOLS (Esta página)
     * PASO 5-A: CONFIGURACIÓN INICIAL DE ASSEMBLER: 
        * PASO 5-A-1.-Introducción-para qué sirve:
        * PASO 5-A-2.-Assembler: Configuración previa:
        * OPCIÓN: AÑADIR REPOSITORIOS PARTICULARES A LA MEZCLA: 

####PASO 5-A-3.- ACTUALIZAR CAMBIOS DE RUTAS A LOS REPOSITORIOS:

Para definir la ruta hacia los repositorios de extensiones (eneboo-features) y de módulos (eneboo-modules) hay que ir a:

En la carpeta home del usuario. 

 En Windows, c:/Users/tuusuario/. 

"/.eneboo-tools/assembler-config.ini"

Editarlo y modificar las rutas

Luego en la consola MSDOS ejecutar:

      Python eneboo-assembler dbupdate -v

     C:\eneboo-tools>python eneboo-assembler dbupdate -v

     Actualizando base de datos de módulos y funcionalidades . . .
     : Se encontraron 25 modulos en la carpeta 'C:\\Users\\(mi-usuario)\\gittas\\eneboo-modules\\'
     : Se encontraron 93 funcionalidades en la carpeta 'C:\\Users\\(mi-usuario)\\gittas\\eneboo-features\\'


####PASO 5-B : ASSEMBLER "NEW" - (ASISTENTE AUTOMÁTICO PARA CREAR PROYECTOS o EXTENSIONES o SET´s):
    
(ver los pasos de Linux, es todo igual...)

--

####OPCIÓN 1 : ASSEMBLER "BUILD BASE" - (COMPILAR/CREAR UN PROYECTO) :

--

####OPCIÓN 2 : ASSEMBLER "BUILD FULLPATCH" - (EXTRAER UNA EXTENSIÓN HECHA DE DIFERENCIAS ENTRE DOS MEZCLAS) :

fullpatch:

calcula el parche de las diferencias entre src y base. (completo)

--

####OPCIÓN 3 : ASSEMBLER "BUILD TEST-FULLPATCH" (PROBAR UN PARCHE-EXTENSIÓN) :

test-fullpatch:

el resultado de aplicar el parche "fullpatch" sobre "base", sirve para realizar las pruebas convenientes antes de guardar el nuevo parche.


----

* NOTA-1 : PARA MODIFICAR LA BASE DE DATOS SQLITE CON EL LISTADO DE MÓDULOS Y FUNCIONALIDADES (EXTENSIONES) CREADOS POR "dbupdate" en  "c:/Users/tuusuario/.eneboo-tools/assembler-database.sqlite" :

Para ver el archivo de:
     assembler-database.sqlite

hay que descargarse **SQLite Studio** de http://rafinguer.blogspot.com.es/2009/09/primeros-pasos-en-sqlite.html

http://sqlitestudio.pl/

...y lo abres/ver "datos"(arriba derecha)/botón derecho mouse en campo "Edit value in editor" luego grabar y "commit" (botón ok-verde arriba)

---

* NOTA-2: HABÍA UN PROBLEMA: LOCALIZABA LOS MÓDULOS PERO NO LOS APLICABA BIEN, pero ya se solucionó modificando la llamada al directorio "/" en vez de "\" (en Windows funcionan al revés que en Linux). 

     ...por ejemplo, si ejecutaba "python eneboo-assembler  build co_subarticulo base", salía:

     WARN: Modulo con nombre facturacion/almacen no encontrado
     WARN: Modulo con nombre facturacion/facturacion no encontrado
     WARN: Modulo con nombre facturacion/principal no encontrado
     WARN: Modulo con nombre facturacion/facturacion no encontrado
     WARN: Modulo con nombre facturacion/informes no encontrado
     ....y asi por unos 465 líneas totales...

     Copiando módulos . . .

     C:\eneboo-tools>
