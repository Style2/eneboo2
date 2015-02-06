
....en construcción...paciencia.

##PASOS DE INSTALACIÓN:

###PASO 1: HACERSE CON UN LINUX
Por qué? ...pues porque parece ser que necesitamos unas "librerías" para el programa Python...y no hay versión "viable" en Windows...

...Tenemos por ahí un Ubuntu...

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
