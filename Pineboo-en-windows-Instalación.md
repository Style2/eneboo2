* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 5 de junio de 2016
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Pineboo-en-windows-Instalaci%C3%B3n)

----

### PASO 0 - DESCARGAMOS PINEBOO Y FLSCRIPTPARSER:

1. Llevamos con usb los repositorios de "pineboo" y "flscriptparser" al directorio raíz...mejor descargarlos desde Linux, porque si los bajas desde Windows los graba de forma "DISTINTA" y luego hay que "ADAPTARLO" con el "dos2unix"...

1. Pineboo lanza el comando flscriptparser2, que debe existir en el PATH. Si habéis seguido las instrucciones de 

--

### PASO 1 - INSTALAMOS PYTHON 3.5

https://www.python.org/downloads/

### PASO 2 - INSTALAMOS BASH


A) ESTE ES DEL 2006...

http://atejada.blogspot.com.es/2006/10/emulador-de-bash-en-windows.html

B) A VER ESTOS:

--

http://www.xataka.com/aplicaciones/asi-es-usar-la-consola-bash-de-ubuntu-en-windows-10

(Abril 2016:) Hace una semana os hablábamos de cómo Microsoft había anunciado una de las grandes novedades de Windows 10: la posibilidad de hacer uso de una consola Linux de forma nativa en este sistema operativo gracias a la colaboración de Canonical, la empresa responsable del desarrollo de Ubuntu. 

Una vez de nuevo en Windows tendremos que ejecutar un Powershell y una vez dentro escribir 'bash' (sin comillas) y pulsar Enter. Al hacerlo se nos indicará que tenemos que aceptar los términos de licencia de la imagen Ubuntu proporcionada por Canonical, y si lo hacemos el sistema procederá a descargar e instalar esa imagen. Cuando termine el proceso podemos cerrar esa ventana y ya tendremos acceso a esa nueva y singular aplicación llamada "Bash on Ubuntu on Windows". 

--

B) ABRIMOS POWERSHELL

* Qué es eso?: ( https://es.wikipedia.org/wiki/Windows_PowerShell )

 "Windows PowerShell es una interfaz de consola (CLI) con posibilidad de escritura y unión de comandos por medio de instrucciones (scripts en inglés)."

* Cómo se ejecuta? ( http://www.tenforums.com/tutorials/25581-windows-powershell-open-windows-10-a.html )

1. Press the Win+R keys to open Run.

2. Type powershell, and click/tap on OK in the search results at the top. (see screenshot below)



--
https://ubuntulife.wordpress.com/2016/05/09/ejecutar-la-shell-de-bash-en-windows-mediante-cmder/

--

Y ARRANCAMOS EL SERVIDOR:

#####1. (PARA postgreSQL): 

A continuación si lo ejecutamos ya lo hará correctamente:

...pero ahora me pide python3-lxml...

### PASO 9 - INSTALAR PYTHON 3 :

     sudo apt-get install python3-lxml (ESTO NO FUNCIONA EN WINDOWS...)

...pero ahora me pide psycopg2...

### PASO 10 - INSTALAR PYTHON3-PSYCOPG2 :

     sudo apt-get install python3-psycopg2

...pero ahora me pide pyqt4...

### PASO 11 - INSTALAR PYTHON3-PYQT4 :

     sudo apt-get install python3-pyqt4


### PASO 12 - INSTALAR PYTHON3-PLY :

...No lo pide pero me lo dicen en eneboo-groups....

     sudo apt-get install python3-ply

### PASO 13 - INSTALAR PYTHON3-FUTURE :

https://github.com/deavid/pineboo/blob/master/README.python3.rst

[Pineboo-Deavid] Adicionalmente, hacemos uso de un paquete llamado "future", que es el que me ha ayudado a hacer la transformación con una herramienta llamada futurize.

Future se usa ahora en el código para que Python2.7 pueda ejecutar nuestro código de python3 y que ambos hagan lo mismo. (Emulando python3)

Esto hace que algunos ficheros requieran de esta librería con Python3, pero creo que es una dependencia que se puede eliminar en el futuro (cuando casi nadie use python2). De todos modos para Python3 creo que no hace casi nada.

Esta dependencia, al menos en ubuntu 14.04 necesita de "pip" para instalarse. No está disponible para apt-get.

     $ sudo apt-get install pip3 $ sudo pip3 install future (ESTO NO VA)

??? SE HA VUELTO LOCO....se pasa 2 a 5 minutos haciendo "Nota, seleccionando `<<mbrola-la1>>` en lugar de `<<mbrola-voice-la>>` "...y al final dice que "E: No se ha podido localizar el paquete pip3 / install / future"

     $ sudo apt-get install python3-pip

...Y LUEGO:

     $ sudo pip3 install future

...AHORA SI.

### PASO 14 - ERROR DE CONEXIÓN:

En el caso de que siga el mensaje de:

     "pineboo.py: cannot connect to X server".....???? 

http://stackoverflow.com/questions/646930/cannot-connect-to-x-server-0-0-with-a-qt-application

ponemos:

     export DISPLAY=0:0.0

### PASO 15 - ARRANCAR PINEBOO:

1. A la hora de enecutar pineboo, puedes hacerlo de varias maneras:

     ./pineboo a secas. Pide datos de conexión en un form

     ./pineboo -l nombre_proyecto. Busca un fichero .xml dentro de projects

     ./pineboo -c user:passwd@host:port/database. Especificando datos de conexión por linea de comandos

1. desde qué directorio he de lanzar ese comando? ....Lo de "./" es porque llama a un subdirectorio?

RESPUESTA:  "./" significa en este mismo directorio. Si no le pones el "./", busca en el path del sistema y si no lo encuentra da error.


