* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 12 de junio de 2016
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Pineboo-en-windows-Instalaci%C3%B3n)

----


### PASO 1 - DESCARGAMOS PINEBOO Y FLSCRIPTPARSER:

1. Desde GITHUB, usando este manual:

https://github.com/Miguel-J/eneboo/wiki/GITHUB-COMO-INSTALARLO-Y-USARLO

1. Descargarlos de:

https://github.com/deavid/pineboo

https://github.com/deavid/flscriptparser

1. Llevamos los repositorios de "pineboo" y "flscriptparser" al directorio raíz...

1. Pineboo lanza el comando flscriptparser2, que debe existir en el PATH. (O NO...)

--

### PASO 2 - INSTALAMOS PYTHON 3.x

https://www.python.org/downloads/


Ir a **www.python.org**  y luego a "download"

* bajar la "Python 3.4.4 2015-12-21" (porque la librería "lxml" no veo que tenga la versión para Python 3.5 y Windows no para de avisarme sobre instalarlo....cocoricó!!!...me decido y me dice que no encuentra Python 3.4...toca instalarlo ...)

https://www.python.org/downloads/windows/

Python 3.4.4 - 2015-12-21 // Download Windows x86-64 MSI installer

descargarla y ejecutarla: crea el directorio **c:\python34** y un acceso directo en el menú...

* (ya borraré el 3.5...desinstalado!...y ahora toca mirar el PATH para diferenciar el 2.7 del 3.4 en la misma máquina... C:\Python34\Doc\python344.chm: "3.4. Python Launcher for Windows") **PENDIENTE**

--

* **EJECUTAR PINEBOO**:

* Voy a MS_DOS (Inicio-Programas-Sistema de Windows-Símbolo de sistema y botón derecho "ejecutar como administrador")

* Cambio con "cd" hasta llegar a "C\Python34" y ejecutar:

     c:\Python34>python c:\eneboo-desarrollos\pineboo\pineboo.py



---

### PASO 3 - Instalamos BASH (ESTO ES ZONA GRIS...parece que también funciona con MS-DOS...saltar al "paso 4"...)


A) ESTE ES DEL 2006...

http://atejada.blogspot.com.es/2006/10/emulador-de-bash-en-windows.html (NO LO HE PROBADO)

--

B) A VER ESTOS:

http://www.xataka.com/aplicaciones/asi-es-usar-la-consola-bash-de-ubuntu-en-windows-10

(Abril 2016:) "Hace una semana os hablábamos de cómo Microsoft había anunciado una de las grandes novedades de Windows 10: la posibilidad de hacer uso de una consola Linux de forma nativa en este sistema operativo gracias a la colaboración de Canonical, la empresa responsable del desarrollo de Ubuntu."

"Una vez de nuevo en Windows tendremos que ejecutar un Powershell y una vez dentro escribir 'bash' (sin comillas) y pulsar Enter. Al hacerlo se nos indicará que tenemos que aceptar los términos de licencia de la imagen Ubuntu proporcionada por Canonical, y si lo hacemos el sistema procederá a descargar e instalar esa imagen. Cuando termine el proceso podemos cerrar esa ventana y ya tendremos acceso a esa nueva y singular aplicación llamada "Bash on Ubuntu on Windows". "

--

C) ABRIMOS POWERSHELL

* Qué es eso?: ( https://es.wikipedia.org/wiki/Windows_PowerShell )

 "Windows PowerShell es una interfaz de consola (CLI) con posibilidad de escritura y unión de comandos por medio de instrucciones (scripts en inglés)."

* Cómo se ejecuta? ( http://www.tenforums.com/tutorials/25581-windows-powershell-open-windows-10-a.html )

1. Press the Win+R keys to open Run.

2. Type powershell, and click/tap on OK in the search results at the top. (see screenshot below)

* Vamos al directorio "pineboo" con "cd.." y ejecutamos "/. pineboo" sin comillas...


--
https://ubuntulife.wordpress.com/2016/05/09/ejecutar-la-shell-de-bash-en-windows-mediante-cmder/



---

...pero ahora me pide python3-lxml...

### PASO 4 - instalar "Python-lxml" para Windows

        https://pypi.python.org/pypi/lxml/3.5.0

Elegir la versión correcta para tu versión de Windows. Yo instalo la de Windows 64b con Python 3.4:

         lxml-3.5.0.win-amd64-py3.4.exe (md5)   MS Windows installer  3.4  2016-06-08 3MB
 
...se instala **automáticamente** en el directorio c:\python34 instalado previamente...

--

* probamos pineboo y responde:

...pero ahora me pide psycopg2...

---

### PASO 5 - Instalar PYTHON3-PSYCOPG2 :

"Psycopg is a PostgreSQL adapter for the Python programming language."

http://initd.org/psycopg/docs/install.html

"Jason Erickson maintains a packaged Windows port of Psycopg with installation executable. Download. Double click. Done."

te lleva a: http://www.stickpeople.com/projects/python/win-psycopg/

donde bajo el "psycopg2-2.6.1.win-amd64-py3.4-pg9.4.4-release.exe"

descargo, ejecuto, se instala sólo en c\Python34 y listo

--

* probamos pineboo y responde:

...pero ahora me pide pyqt4...

---

### PASO 6 - Instalar PYTHON3-PYQT4 :

https://www.riverbankcomputing.com/software/pyqt/download

donde bajo el "PyQt4-4.11.4-gpl-Py3.4-Qt4.8.7-x64.exe Windows 64-bit installer "

lo ejecuto y reinicio el ordenador...

--

* probamos pineboo y responde: ABRE EL FORMULARIO DE CONEXIÓN !!

---

### PASO 7 - INSTALAR SERVIDOR PostgreSQL :

https://github.com/Miguel-J/eneboo/wiki/Instalacion-en-windows-con-PostgreSQL

* NOTA: CUIDADO, resulta que Pineboo se conecta al 127.0.0.1 y PostgreSQL se configura para "oír" sólo "localhost"...por lo que hay que arreglarlo editando el archivo "postgresql.conf" (C:\Program Files\PostgreSQL\9.5\data) y/o los datos de conexión del servidor en PgAdminIII...???...pues pone "*"...???....pruebo a reiniciar todo sin cambiar nada, a ver....ok, ya funciona...

---

### PASO 8 - DAR DE ALTA NUEVO USUARIO Y BASE DE DATOS EN SERVIDOR PostgreSQL :

https://github.com/Miguel-J/eneboo/wiki/Instalacion-en-windows-con-PostgreSQL

---

### PASO 9 - (OPCIONAL) ARRANCAR ENEBOO Y CARGAR PAQUETE/DIRECTORIO DE MÓDULOS para PostgreSQL :

https://github.com/Miguel-J/eneboo/wiki/Instalacion-en-windows-con-PostgreSQL

---

### PASO 10 - EDITAR EL ARCHIVO \pineboo\projects\eneboo-base.xml

---

YA FUNCIONA, FALTA FUTURIZE .....PERO DA MUCHOS ERRORES...SERÁ POR ESO?


### PASO 11 - AÑADIR DATOS CONEXIÓN AL FORMULARIO DE ENTRADA

Los mismos de EDITAR EL ARCHIVO \pineboo\projects\eneboo-base.xml

---


### PASO 12 - INSTALAR PYTHON3-PLY : (esto no lo he hecho)

http://www.dabeaz.com/ply/

"Welcome to the PLY homepage. PLY is an implementation of lex and yacc parsing tools for Python. If you don't have the slightest idea what that means, you're probably in the wrong place. Otherwise, keep reading."

http://www.gossamer-threads.com/lists/python/python/906263

 "Python setup.py install"......"Change "python" to the full path of your pythonw.exe executable."

--

Lo descargo y ejecuto "setup" desde el directorio de"ply-3.8":

C:\ENEBOO-DESARROLLOS\pineboo\ply-3.8\setup.py install

--

...el problema es que se instala en \python27 y no en \python34 ...?¿?¿

...No lo pide pero me lo dicen en eneboo-groups....

     sudo apt-get install python3-ply

### PASO 13 - INSTALAR PYTHON3-FUTURE : (esto no lo he hecho)

https://github.com/deavid/pineboo/blob/master/README.python3.rst

* "[Pineboo-Deavid] Adicionalmente, hacemos uso de un paquete llamado "future", que es el que me ha ayudado a hacer la transformación con una herramienta llamada futurize."

* "Future se usa ahora en el código para que Python2.7 pueda ejecutar nuestro código de python3 y que ambos hagan lo mismo. (Emulando python3)"

* "Esto hace que algunos ficheros requieran de esta librería con Python3, pero creo que es una dependencia que se puede eliminar en el futuro (cuando casi nadie use python2). De todos modos para Python3 creo que no hace casi nada." ...PARECE QUE LOS MÓDULOS NO SE CARGAN BIEN...SERÁ POR ESTO?...LO INSTALO:


* ...????...qué paquete es? este?:

https://pypi.python.org/pypi/future/0.15.2

o este?:

https://pypi.python.org/pypi/futures

....ni idea...


---

### PASO 15 - ARRANCAR PINEBOO:

* Voy a MS_DOS (Inicio-Programas-Sistema de Windows-Símbolo de sistema y botón derecho "ejecutar como administrador")

* Cambio con "cd" hasta llegar a "C\Python34" y ejecutar:

     c:\Python34>python c:\eneboo-desarrollos\pineboo\pineboo.py


--

* ESTO ERA EN LINUX:

1. A la hora de enecutar pineboo, puedes hacerlo de varias maneras:

     ./pineboo a secas. Pide datos de conexión en un form

     ./pineboo -l nombre_proyecto. Busca un fichero .xml dentro de projects

     ./pineboo -c user:passwd@host:port/database. Especificando datos de conexión por linea de comandos

1. desde qué directorio he de lanzar ese comando? ....Lo de "./" es porque llama a un subdirectorio?

RESPUESTA:  "./" significa en este mismo directorio. Si no le pones el "./", busca en el path del sistema y si no lo encuentra da error.

---

