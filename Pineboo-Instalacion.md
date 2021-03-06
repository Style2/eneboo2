* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 5 de junio de 2016
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Pineboo-Instalacion)

----


**INTRODUCCIÓN - NOTA SOBRE LINUX**:
* Cómo llego a la **consola"?
     * Entrar a la consola desde la vista-escritorio: Ctrl+Alt+F1
     * Salir de la consola hacia la vista-escritorio: Ctrl+Alt+F7

* Qué teclas sirven para **copiar-y-pegar** el texto en la consola en Linux o Unix ?:
     * Ctrl+Shift+c = copiar
     * Ctrl+Shift+V.= pegar

* Cómo extraer de forma segura un USB?
     * vas a la consola con Ctrl+Alt+F1 y escribes **umount /media/linux(o nombre ordenador)/(nombre de volumen del usb)**

----
####Pineboo en linux:

### PASO 1 - INSTALAMOS Y ARRANCAMOS EL SERVIDOR:

#####1. (PARA postgreSQL): 

Para Linux-UBUNTU "activamos/instalamos" el servidor de postgreSQL que lleva:

     sudo apt-get postgresql

Y luego Ir a consola (Ctrl+Alt+F1) y "arrancar":

     sudo service postgresql start

#####1. (PARA MYSQL): Ir a consola (Ctrl+Alt+F1) y arrancar XAMPP: 

     $ sudo /opt/lampp/lampp start


### PASO 2 - CREAMOS USUARIO Y BASE DE DATOS:

#####Configurar contraseña para el usuario postgres

PostgreSQL crea un usuario llamado postgres a nivel del sistema. Es el homónimo del usuario root en MySQL, es decir, con el usuario postgres vas a poder administrar y configurar el servidor de PostgreSQL.

El método de autenticación por defecto para este usuario es peer. Este método utiliza el nombre del usuario de tu sesión activa para la gestión de accesos al motor de base de datos. Por lo cual necesitamos iniciar sesión con este usuario.

Para iniciar sesión con un usuario diferente debemos ejecutar el siguiente comando:

     sudo su postgres

Una vez hecho el paso anterior iniciaremos sesión en el cliente de PostgreSQL, nuevamente en la terminal ejecuta el siguiente comando:

     psql

Dentro del cliente de PostgreSQL debes ejecutar la siguiente sentencia SQL y presiona la tecla Enter:

     ALTER USER Postgres WITH PASSWORD '<password>';

No olvides cambiar la palabra <password> por la contraseña que deseas asignar al usuario postgres.

Para salir del cliente debes escribir el comando \q seguido de la tecla Enter.

--

sudo su postgres

Para poder desarrollar este nanotutorial necesitamos tener disponible una sesión cliente en un servidor PostgreSQL. Para esto debemos iniciar el cliente con el siguiente comando:

      psql -U postgres -h localhost -W

--

#####1. PARA POSTGRESQL: instalamos pgAdmin3:

sudo apt-get install pgadmin3

y una vez instalado vamos a consola Ctrl+Alt+F7 y damos a "inicio" "ejecutar" "pgadmin3"...y se abre el programa

luego le damos al dibujo del enchufe y creamos una conexión nueva con estos datos:

     <type>postgresql</type>
     <host>127.0.0.1</host>
     <port>5432</port>
     <username>postgres</username>
     <password>postgres</password>
     <database-name>eneboobase</database-name>


### PASO 3 - DESCARGAMOS PINEBOO Y FLSCRIPTPARSER:

1. Llevamos con usb los repositorios de "pineboo" y "flscriptparser" al directorio raíz...mejor descargarlos desde Linux, porque si los bajas desde Windows los graba de forma "DISTINTA" y luego hay que "ADAPTARLO" con el "dos2unix"...

1. Pineboo lanza el comando flscriptparser2, que debe existir en el PATH. Si habéis seguido las instrucciones de instalación, ya lo tenéis. Si no, pues podéis enlazarlo:

     sudo ln -s /path/to/flscriptparser/flscriptparser2 /usr/local/bin/flscriptparser2

en mi caso queda así:

     Linux@linux-AOA150:~$ sudo ln -s /home/linux/flscriptparser/flscriptparser2 /usr/local/bin/flscriptparser2
     [sudo] password for Linux:

### PASO 4 - ARRANCAR ENEBOO DESDE ORDENADOR:

NOTA: Este paso no es imprescindible, pero sirve para controlar que la conexión "habitual" funciona...

Volver a ventanas (Ctrl+Alt+F7) y arrancar el programa (eneboo) desde el explorador de archivos en:
         * /home/linux/Descargas/eneboo--dba/bin

### PASO 5 - DESCARGAR DEL GITHUB "ENEBOO-MODULES" Y PONERLO EN LA CARPETA DE PINEBOO

NOTA: Este paso no es imprescindible, de hecho no sé si sirve de algo...pero por si acaso...

### PASO 6 - CARGAR MÓDULOS EN LA EMPRESA "eneboobase": 

NOTA: Este paso no es imprescindible, pero sirve para controlar que la conexión "habitual" funciona...

con Sistema-Cargar directorio de módulos de un src cualquiera...

### PASO 7 - DAR PERMISOS DE EJECUCIÓN A PINEBOO:

El fichero ./pineboo es un script, y como tal mira si tiene permiso de ejecución. (Permite ejecutar el script como un programa). 

http://blog.desdelinux.net/cual-es-la-diferencia-entre-ejecutar-un-script-bash-usando-sh-y/

Para otorgar permisos de ejecución a nuestro script, debemos escribir:

     chmod a+x pineboo

Use el comando ls para ver los permisos que posee el script:

     $ ls -l nombre-del-script

--

NOTA: Para poder ejecutar un script por sí solo deben cumplirse 2 condiciones:

1. el script debe incluir un “bang line”. Se trata de la primera línea de un script, que debe comenzar con los caracteres #! y que debe especificar la ruta en la que se encuentra el intérprete. Es importante notar que esta condición se cumple para cualquier tipo de script (python, perl, etc.), no sólo los de bash. Así, por ejemplo, nuestro script debería contener como primera línea lo siguiente:

     #!/bin/bash

1. el archivo debe tener permisos de ejecución:

Al incluir una “bang line”, tus scripts serán mucho más fáciles de distribuir, ya que los usuarios no deberán recordar la ruta en la que se encuentran los intérpretes necesarios para poder ejecutarlos. 

--

### PASO 8 - ERRORES CONOCIDOS: CONVERTIR A UNIX

1. Si pues si, lo descargué desde mi Windows...

lo he arreglado con dos2unix:

http://systemadmin.es/2011/02/bin-bash-bad-interpreter

Debemos fijarnos que nos indica “/bin/bash^M“, nos indica que tenemos los intros de DOS (Windows) posiblemente por haber sido editado con dicho sistema operativo. Para corregirlo simplemente deberemos usar la utilidad dos2unix:

     $ dos2unix parser.sh 
     dos2unix: converting file parser.sh to UNIX format ...

EJEMPLO:
 
     sudo apt-get install dos2unix
     dos2unix pineboo

A continuación si lo ejecutamos ya lo hará correctamente:

...pero ahora me pide python3-lxml...

### PASO 9 - INSTALAR PYTHON 3 :

     sudo apt-get install python3-lxml

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


1. con qué usuario debería llamarlo? el mio-administrador ("linux") o el de la base de datos "eneboobase"="postgres" ?

RESPUESTA: Con tu usuario habitual de sistema ("linux"). ...he mirado el archivo \etc\"passwd" y salen (entre muchos):

     root:x:0:0:root:/root:/bin/bash
     linux:x:1000:1000:linux,,,:/home/linux:/bin/bash
     ...osease que "linux" NO es "root"

---

...y TE VAS AL ENTORNO GRÁFICO Ctrl+Alt+F7 y aparece el cuadro de conexión:



![Pineboo en linux](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-pineboo/eneboo-pineboo-01.jpg)

![Pineboo en linux](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-pineboo/eneboo-pineboo-02.jpg)

![Pineboo en linux](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-pineboo/eneboo-pineboo-03.jpg)

![Pineboo en linux](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-pineboo/eneboo-pineboo-04.jpg)

![Pineboo en linux](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-pineboo/eneboo-pineboo-05.jpg)

![Pineboo en linux](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-pineboo/eneboo-pineboo-06.jpg)

![Pineboo en linux](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-pineboo/eneboo-pineboo-07.jpg)

...y si TE VAS AL ENTORNO CONSOLA Ctrl+Alt+F1 y aparece la relación de mensajes:

![Pineboo en linux](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-pineboo/eneboo-pineboo-08.jpg)
