* CREADO POR: miguelajsmaps@gmail.com
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 9 de febrero de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/EnebooTools---Instalaci%C3%B3n-en-linux)

----

....en construcción...paciencia.

##PASOS DE INSTALACIÓN:

###PASO 1: HACERSE CON UN LINUX
* Por qué? ...pues porque parece ser que necesitamos unas "librerías" para el programa Python...y no hay versión "viable" en Windows...

#####OPCIÓN A: INSTALAR VIRTUALBOX CON UBUNTU 

Para hacerlo hay que seguir estos pasos:
https://github.com/Miguel-J/eneboo/wiki/Eneboo-Tools-en-Windows

...pero la velocidad es muy lenta...

#####OPCIÓN B: INSTALAR UBUNTU COMO PARTICIÓN JUNTO A WINDOWS:

######INTENTO 1 - DESASTRE:
1.  Descargar el ejecutable de Ubuntu, visitando desde Windows:

www.ubuntu.com

1. ir a "download" y descargar el archivo ISO de la más reciente (OJO!: NO INSTALAR LA LTS, NO SE INSTALÓ BIEN....luego descomprimir en "mis documentos"....luego ejecutar "wubi.exe"...

1. añadir usuario y contraseña...dejar el resto como sugiere: 18Gb instalación (para 14.04 LTS en 32bits en Windows XP; entorno "Ubuntu"; idioma "spanish")
* NOTA: desactivar el firewall o permitir accesos...
* NOTA: NO INSTALAR LA LTS: (para 14.04 LTS en 32bits en Windows XP; entorno "Ubuntu"; idioma "spanish") error: PERMISSION DENIED ...VER LOG...????...resulta que no podía instalar desde la ISO y el tio va y se conecta para descargar lo q necesita de vete-a-saber-dónde???...y quién le ha dado permiso?....borro todo y PRUEBO LA OTRA: ver.14.10

######INTENTO 2: PARECE QUE FUNCIONA...

* Después de perder dos días enteros intentando instalar mi "maldecido hasta el aburrimiento" Linux-distro-Ubuntu-14.10 renuncio por su incapacidad de gestionar más de una partición primaria en un acer netbook aspire one de 1Gb (con sistema Windows-xp pregrabado en fábrica)

* Usando algo llamado Netboot y formateando un USB, instalo Linux-distro-Lubuntu-14.04 para 32b, dando prioridad de arranque por BIOS al USB y con la opción de sobre-escribir la instalación windows-XP. También aplico la opción de descargar actualizaciones.

#####OPCIÓN B: INSTALAR UBUNTU DESDE CERO FORMATEANDO EL DISCO:

* Esto no lo he probado (o si...espero no haber perdido la partición de fábrica...) 
* Ejecuto desde consola "df -h" ....y si, ya puedo decir adiós Windows-xp: no aparece la partición por ningún lado...

####CONSEJOS DE USO DE UBUNTU:

...parece que para acceder al "símbolo de sistema" hay que darle a "Ctrl" + "Alt" +  "F1" a "F6"...y para volver al entorno gráfico es:  "Ctrl" + "Alt" +  "F7"

###PASO 2: INSTALAR PYTHON:

#####Y QUE DEMONIOS ES PYTHON?


https://www.python.org/

http://es.wikipedia.org/wiki/Python

Se trata de un lenguaje de programación multiparadigma, ya que soporta orientación a objetos, programación imperativa y, en menor medida, programación funcional.Es administrado por la Python Software Foundation. Posee una licencia de código abierto.

eN 1995, van Rossum lanzó la iniciativa Computer Programming for Everybody (CP4E), con el fin de hacer la programación más accesible a más gente, con un nivel de 'alfabetización' básico en lenguajes de programación, similar a la alfabetización básica en inglés.

Python fue diseñado para ser leído con facilidad. Una de sus características es el uso de palabras donde otros lenguajes utilizarían símbolos. Por ejemplo, los operadores lógicos !, || y && en Python se escriben not, or y and, respectivamente.


##### REQUISITOS MÍNIMOS (Dependencias)

https://github.com/gestiweb/eneboo-tools/blob/master/README.rst

---------
Como mínimo, se necesita:

    * python 2.5 
        * sqlite3
    * lxml (python-lxml)
        * libxml2
        * libxslt
    
Para tener el programa funcionando, se recomienda:

    * python 2.6 o superior. (no es compatible con Python 3.X)
    * lxml (python-lxml) (Parser de XML)
    * psycopg (python-psycopg) (Driver de base de datos PostgreSQL)
    * pyqt4 (python-pyqt4) (Enlace de Qt4 para GUI)

#####PASOS:

1. Desde el navegador Firefox de Linux voy a www.python.org/downloads y descargo la 2.7.9.....12 megas solo?...descomprime....entro en carpeta...ejecuto setup.py?....nada....y install-sh?....nada

1. Leer instrucciones: https://wiki.python.org/moin/BegginersGuide

1. Verificar la instalación: ir a consola (Ctrl+Alt+F1) y teclear "Python"...sale:

      $python
      Python 2.7.6 (default, Mar 22 2014)
      >>>

* NOTA ...y la 2.7.9 ???

1. Verificar las librerias

      $pydoc modules |more

* lxml.de/installation.html

--------

###PASO 3: CLONAR EL GITHUB DE ENEBOO-TOOLS:

https://github.com/Miguel-J/eneboo/wiki/GITHUB-COMO-INSTALARLO-Y-USARLO

* 4.Una vez instalado vas a PROGRAMAS-GITHUB y le das a "GITHUB"....se abre una pantalla en blanco....
* 5.Vas ARRIBA-DERECHA a la rueda dentada y le das a "OPEN IN GIT SHELL", entonces se abre una ventana parecida al MSDOS de windows con unas letras en colores entre corchetes...

git clone https://github.com/gestiweb/eneboo-tools

* ...y al darle a ENTER lo pone como subdirectorio en el directorio desde donde ejecutas el "git clone"
* para cambiar de directorio usar "cd .." o "cd subdirectorio"


###PASO 4: Instalación



La instalación recomendada es enlazar los comandos en /usr/local/bin 

Hemos creado un Makefile que lo hace automáticamente al lanzar el comando::
    
    $ sudo make install
    
Si se quiere realizar manualmente, se puede hacer del siguiente modo::

    $ sudo ln -s $HOME/git/eneboo-tools/eneboo-mergetool /usr/local/bin/eneboo-mergetool
otro dia ;-)
