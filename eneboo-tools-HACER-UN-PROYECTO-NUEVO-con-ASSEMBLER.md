* CREADO POR: deavid - Gestiweb
* MODIFICADO POR: miguelajsmaps@gmail.com
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 10 de agosto de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/eneboo-tools-HACER-UN-PROYECTO-NUEVO-con-ASSEMBLER)

----


Proyecto NUEVO DE MEZCLA CON Eneboo-tools 
=================================================


INSTALACIÓN PREVIA (Dependencias): 
---------------------

PASO 1 A 4:  Visitar la página:

https://github.com/Miguel-J/eneboo/wiki/EnebooTools---Instalaci%C3%B3n-en-linux

##INDICE:

###PASO 1: HACERSE CON UN LINUX
* Por qué? ...pues porque parece ser que necesitamos unas "librerías" para el programa Python...y no hay versión "viable" en Windows...

###PASO 2: INSTALAR PYTHON:

#####2.c-PASO A-INSTALAR PYTHON: (Linux ya lo trae de fábrica) 

#####2.c-PASO B-INSTALAR LIBXML2 y LIBXSLT:

###PASO 3: CLONAR EL GITHUB DE ENEBOO-TOOLS (eneboo-modules y eneboo-features): 

###PASO 4: INSTALACIÓN DE ENEBOO-TOOLS

La instalaciÃ³n recomendada es enlazar los comandos en /usr/local/bin 

Hemos creado un Makefile que lo hace automÃ¡ticamente al lanzar el comando::
    
    $ sudo make install
    
Si se quiere realizar manualmente, se puede hacer del siguiente modo::

    $ sudo ln -s $HOME/git/eneboo-tools/eneboo-mergetool /usr/local/bin/eneboo-mergetool

###PASO 5: CONFIGURACIÓN DE ENEBOO-TOOLS (Esta página)

###PASO 5-A: CONFIGURACIÓN INICIAL DE ASSEMBLER: 

PASO 5-A-1.-Introducción-para qué sirve:

PASO 5-A-2.-Assembler: Configuración previa:

OPCIÓN: AÑADIR REPOSITORIOS PARTICULARES A LA MEZCLA: 

PASO 5-A-3.- ACTUALIZAR CAMBIOS DE RUTAS A LOS REPOSITORIOS:

### PASO 5-B : ASSEMBLER "NEW" - (ASISTENTE AUTOMÁTICO PARA CREAR PROYECTOS o EXTENSIONES o SET´s):

### PASO 5-C : ASSEMBLER "BUILD" - (COMPILAR/CREAR UN PROYECTO) :



--------------


###PASO 5-A: CONFIGURACIÓN INICIAL DE ASSEMBLER: 

PASO 5-A-1.-IntroducciÃ³n-para qué sirve:
------------------------
eneboo-assembler es una herramienta de "collage" de cÃ³digo fuente. Toma como base
unos mÃ³dulos y les aplica una serie de parches en un orden determinado para 
conseguir un proyecto modificado de cierta forma, que cumpla ciertas especificaciones.

Es una buena forma para mantener centenares de versiones distintas del mismo programa
al dÃ­a, gestionando correctamente los cambios propios que tiene cada versiÃ³n.


PASO 5-A-2.-Assembler: Configuración previa:
------------------------


Ir a la consola de linux: Ctrl+Alt+F1 (volver a entorno ventana: Ctrl+Alt+F7)


El comando "eneboo-assembler" es el que usaremos normalmente para realizar las 
mezclas desde consola. Es muy sencillo y prÃ¡ctico. 

Este comando tiene unas configuraciones y una base de datos de cachÃ©. Para que 
genere los primeros ficheros es conveniente lanzar la acciÃ³n "dbupdate"::

    $ eneboo-assembler dbupdate

Cabe destacar que eneboo-assembler no depende de en quÃ© carpeta lo ejecutes.


Para empezar, necesitaremos como mínimo 2 repositorios para empezar:

    * Módulos Oficiales
    * Extensiones Oficiales

...hay que COPIARLOS (descargados de Github "gestiweb" o "klo-manolo") en una CARPETA-SUBDIRECTORIO, por ejemplo "eneboo-proyecto1"...

Todas las acciones de ENEBOO-ASSEMBLER leen los directorios INDICADOS en los ARCHIVOS de las CONFIGURACIONES. Para que esto funcione como debe, es necesario revisar la configuraciÃ³n que nos crea en $HOME/.eneboo-tools/assembler-config.ini

En ese fichero, que es muy sencillo de editar a mano (ATENCIÓN: ES UN FICHERO OCULTO, MOSTRARLO CON Ctrl+H o por Menú-Ver-Mostrar lo oculto) (está en un subdirectorio creado por eneboo-tools...fijarse en el "." antes del nombre o buscar por menu-Herramientas...), debemos incluir las RUTAS de la CARPETA-SUBDIRECTORIO (en este caso: "eneboo-proyecto1")...donde hemos puesto los mÃ³dulos ("eneboo-modules") y las funcionalidades o "extensiones("eneboo-features"), en mi caso:
"/home/linux/.eneboo-tools/assembler-config.ini"

OPCIÓN: AÑADIR REPOSITORIOS PARTICULARES A LA MEZCLA: 

Si tenemos repositorios privados, se pueden agregar tambiÃ©n.

Se deben modificar las rutas si el/los directorios de los módulos/extensiones particulares son distintos a los directorios donde están los oficiales.

Al añadir las rutas a "assembler-config.ini" hay que tener en cuenta que las lÃ­neas de abajo toman preferencia sobre las de arriba. Se recomienda poner
al final siempre los repositorios públicos para que tomen preferencia.

EJEMPLO: Este serÃ­a un ejemplo de configuraciÃ³n, en mi caso:

    [module]
    modulefolders = 
            /home/linux/eneboo-proyecto1/eneboo-modules
    featurefolders = 
            /home/linux/eneboo-proyecto1/eneboo-features
    buildcache = ~/.eneboo-tools/buildcache


PASO 5-A-3.- ACTUALIZAR CAMBIOS DE RUTAS A LOS REPOSITORIOS:
---------------------------------
Siempre que modificamos la ruta de una extensiÃ³n, o ponemos o quitamos alguna, es necesario ejecutar "dbupdate", que almacenarÃ¡ en cachÃ© dÃ³nde 
estÃ¡n los mÃ³dulos y extensiones. Si no lo hacÃ©is luego os darÃ¡ errores de que no encuentra las extensiones nuevas::

    $ eneboo-assembler dbupdate -v

Las extensiones si os fijÃ¡is son carpetas con ficheros de configuraciÃ³n y con los parches para aplicar dentro. Hay un proyecto de ejemplo creado que une 
cuatro extensiones muy bÃ¡sicas. 



### PASO 5-B : ASSEMBLER "NEW" - (ASISTENTE AUTOMÁTICO PARA CREAR PROYECTOS o EXTENSIONES o SET´s):
-----------------------------------------

UTILIDAD: Proceso automático de "listar" los módulos y extensiones ANTES de COMPILARLOS (paso 5-C)

Hasta hace poco para crear las extensiones nuevas que el assembler pueda leer habÃ­a que crear los ficheros y carpetas a mano. Como son unas cuantas, esto era un tanto costoso.

Para facilitar las cosas hemos creado una acciÃ³n "new" que contiene un asistente que realizarÃ¡ las preguntas necesarias y luego escribirÃ¡ en disco la extensiÃ³n.

Si se ejecuta sin argumentos, preguntarÃ¡ los datos mÃ­nimos para crear la plantilla::

    $ eneboo-assembler new

    QuÃ© tipo de funcionalidad va a crear?
        ext) extensiÃ³n
        prj) proyecto
        set) conjunto de extensiones
    Seleccione una opciÃ³n: ext

    CÃ³digo para la nueva funcionalidad: A002
(el valor debe seguir el formato A999 (A puede ser un número)).

    Nombre corto de funcionalidad: mifun02

    DescripciÃ³n de la funcionalidad: Funcionalidad 02 
    
Si se le pasa el nombre de la carpeta y la descripciÃ³n, omite los pasos 
iniciales y pasa directamente al menÃº::
    
    $ eneboo-assembler new extA003-mifun03 "Funcionalidad 03" 
    
AparecerÃ¡ el menÃº principal como se muestra a continuaciÃ³n::

    **** Asistente de creaciÃ³n de nueva funcionalidad ****

     : Carpeta destino : /home/david/git/eneboo-features/extA003-mifun03
     : Nombre          : extensiÃ³n - A003 - mifun03 
     : DescripciÃ³n     : Funcionalidad 03 

     : Dependencias    : 0 mÃ³dulos, 0 funcionalidades
     : Importar Parche : None

    --  MenÃº de opciones generales --
        c) Cambiar datos bÃ¡sicos
        d) Dependencias
        i) Importar parche
        e) Eliminar parche
        a) Aceptar y crear
        q) Cancelar y Salir
    Seleccione una opciÃ³n: 


La opciÃ³n *d) Dependencias* sirve para aÃ±adir mÃ³dulos y funcionalidades. Una vez dentro del menÃº de dependencias, para facilitar la tarea de agregado podemos utilizar caracteres comodÃ­n. Por ejemplo, si introducimos "flfact*" y pulsamos tabulador, pondrÃ¡ todos los mÃ³dulos que empiecen por "flfact".

En el caso de las rutas, tambiÃ©n existe autocompletado con el sistema de ficheros, que se activa con la tecla de tabulador.

Por defecto las extensiones se crean en la primera carpeta de extensiones que
haya en la configuraciÃ³n, se puede cambiar la carpeta de destino en una opciÃ³n del
menÃº.


---

### PASO 5-C : ASSEMBLER "BUILD" - (COMPILAR/CREAR UN PROYECTO) :

UTILIDAD: Sirve para que Eneboo-Tools "COPIE" los módulos y extensiones LISTADOS por Assembler NEW o MANUALMENTE.

 Para crear un proyecto (lo que llamamos "compilar") se lanza la acciÃ³n "build" seguida del proyecto y del target. El "target" es quÃ© es lo que se 
quiere crear, la idea es muy similar al make. El modo de empleo es::
    
    $ eneboo-assembler build [FEATURE] [TARGET]
    
*[FEATURE]* es el nombre corto (quitando la numeraciÃ³n) de la funcionalidad, es decir, para el proyecto *prj0002-standard* habrÃ­a que poner *standard*.

*[TARGET]* puede tomar los valores:

    * **base:** 
        compila las dependencias del proyecto (todo lo que 
        necesitamos para poder aplicar los parches luego)
    * **final:** 
        todo lo que lleva base, mas los parches que existen 
        para este proyecto. (esto es lo que se envÃ­a al cliente)
    * **src:** 
        una copia del target final, donde realizar los cambios 
        a la extensiÃ³n
    * **patch:** 
        calcula el parche de las diferencias entre src y final. (incremental)
    * **test-patch:** 
        el resultado de aplicar el parche "patch" sobre 
        "final", sirve para realizar las pruebas convenientes antes de 
        guardar el nuevo parche.
    * **fullpatch:** 
        calcula el parche de las diferencias entre src y base. (completo)
    * **revfullpatch:** 
        calcula el parche de las diferencias entre base y src. (completo)
    * **test-fullpatch:** 
        el resultado de aplicar el parche "fullpatch" sobre 
        "base", sirve para realizar las pruebas convenientes antes de 
        guardar el nuevo parche.

Novedad: Podemos usar "revfullpatch" para que nos calcule un parche inverso, lo
cual desaplicarÃ­a una extensiÃ³n a un proyecto dado.

Cuando compilamos algo, nos lo deja dentro de la carpeta build/ en la 
carpeta de la extensiÃ³n que habÃ­amos compilado.

Por ejemplo::

    deavid:~$ eneboo-assembler build basic base
    Borrando carpeta /home/deavid/git/eneboo-features/prj001-basic/build/base . . . 
    Copiando facturacion/principal . . . 
    Copiando facturacion/facturacion . . . 
    Copiando contabilidad/informes . . . 
    Copiando contabilidad/principal . . . 
    Copiando facturacion/informes . . . 
    Copiando facturacion/tesoreria . . . 
    Copiando facturacion/almacen . . . 
    Aplicando parche (...)oo-features/ext0224-pgc2008/patches/pgc2008 . . .
    Aplicando parche (...)res/ext0014-recibosprov/patches/recibosprov . . .
    WARN: No hemos encontrado el bloque de cÃ³digo para las definiciones de la clase ifaceCtx, pondremos las nuevas al final del fichero.
    Aplicando parche (...)/ext0020-co_renumasiento/patches/co_renumasiento . . .
    WARN: No hemos encontrado el bloque de cÃ³digo para las definiciones de la clase ifaceCtx, pondremos las nuevas al final del fichero.
    Aplicando parche (...)/ext0048-listadoscliprov/patches/listadoscliprov . . .

    deavid:~$ cd /home/deavid/git/eneboo-features/prj001-basic/build/
    deavid:~/git/eneboo-features/prj001-basic/build$ ls
    base  base.build.xml

    deavid:~/git/eneboo-features/prj001-basic/build$ cat base.build.xml 
    <BuildInstructions feature="prj001-basic" target="base" path="/home/deavid/git/eneboo-features/prj001-basic" dstfolder="build/base">
      <CopyFolderAction src="/home/deavid/git/eneboo-modules/facturacion/principal" dst="facturacion/principal" create_dst="yes"/>
      <CopyFolderAction src="/home/deavid/git/eneboo-modules/facturacion/facturacion" dst="facturacion/facturacion" create_dst="yes"/>
      <CopyFolderAction src="/home/deavid/git/eneboo-modules/contabilidad/informes" dst="contabilidad/informes" create_dst="yes"/>
      <CopyFolderAction src="/home/deavid/git/eneboo-modules/contabilidad/principal" dst="contabilidad/principal" create_dst="yes"/>
      <CopyFolderAction src="/home/deavid/git/eneboo-modules/facturacion/informes" dst="facturacion/informes" create_dst="yes"/>
      <CopyFolderAction src="/home/deavid/git/eneboo-modules/facturacion/tesoreria" dst="facturacion/tesoreria" create_dst="yes"/>
      <CopyFolderAction src="/home/deavid/git/eneboo-modules/facturacion/almacen" dst="facturacion/almacen" create_dst="yes"/>
      <ApplyPatchAction src="/home/deavid/git/eneboo-features/ext0224-pgc2008/patches/pgc2008"/>
      <ApplyPatchAction src="/home/deavid/git/eneboo-features/ext0014-recibosprov/patches/recibosprov"/>
      <ApplyPatchAction src="/home/deavid/git/eneboo-features/ext0020-co_renumasiento/patches/co_renumasiento"/>
      <ApplyPatchAction src="/home/deavid/git/eneboo-features/ext0048-listadoscliprov/patches/listadoscliprov"/>
    </BuildInstructions>

    deavid:~/git/eneboo-features/prj001-basic/build$ find base -maxdepth 2 -type d
    base/facturacion
    base/facturacion/principal
    base/facturacion/facturacion
    base/facturacion/informes
    base/facturacion/tesoreria
    base/facturacion/almacen
    base/contabilidad
    base/contabilidad/informes
    base/contabilidad/principal


Si os fijÃ¡is, la idea es en el futuro, "apilar" parches, es decir, que cuando modificamos una 
extensiÃ³n creamos otro parche **distinto**, que tiene que ser aplicado **despuÃ©s** 
del original. Esto ayudarÃ¡ a que si dos personas trabajan a la vez sobre el 
mismo parche, sea mucho mÃ¡s fÃ¡cil mezclarlo. 

De momento, no hay soporte para parche incremental, pues casi todos los diff y 
patch contextuales son incapaces de realizar un patch incremental (la Ãºnica
excepciÃ³n es el de XML). AsÃ­ que de momento sÃ³lo se pueden guardar cambios 
reemplazando todos los anteriores (con fullpatch).

Para guardar un cambio, despuÃ©s de haberlo probado con test-fullpatch y habiendo
comprobado que no hemos perdido nada, se usa la acciÃ³n "save-fullpatch" del siguiente
modo::

    $ eneboo-assembler save-fullpatch prj001-basic
    
Eso sÃ­, la operaciÃ³n **ES DESTRUCTIVA** y reemplazarÃ¡ lo que habÃ­a antes sin que
se pueda recuperar. No recomiento usar esto si no tenemos la carpeta bajo control
de versiones (GIT, SVN, etc), porque en un descuido nos podemos quedar sin parche.


AÃºn faltan cosas bÃ¡sicas por desarrollar, como por ejemplo:

    * Comando "save-patch" para guardar los cambios realizados en un parche incremental
    * Comando "blend-patches" para unir todos los parches en uno solo. (excepto los N Ãºltimos) 
    * Comando "export" para generar un tar.gz de los mÃ³dulos (del target final)


------------------------------------------------------------------    

Packager
-----------------------------

Esta herramienta permite empaquetar cÃ³digo eneboo en un sÃ³lo fichero .eneboopkg. Este tipo de ficheros presentan varias ventajas frente al cÃ³digo tradicional ordenado en carpetas de mÃ³dulos, a saber:

- Se pueden importar de forma cÃ³moda desde la opciÃ³n *Sistema > AdministraciÃ³n > Cargar Paquete de MÃ³dulos* de eneboo.
- Ocupan menos, ya que el cÃ³digo estÃ¡ comprimido.
- Son mÃ¡s fÃ¡ciles de trasladar y descargar.

Para empaquetar un directorio que contenga cÃ³digo eneboo podemos usar::

    $ eneboo-packager create ruta_directorio_codigo -v
    
Para conocer todas las opciones de la herramienta::
    
    $ eneboo-packager --help


