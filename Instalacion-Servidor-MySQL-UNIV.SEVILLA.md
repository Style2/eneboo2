* CREADO POR: [Universidad de Sevilla](http://www.us.es): Guillermo Molleda Jimena 
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 18 de febrero de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Instalacion-Servidor-MySQL-UNIV.SEVILLA)

----
###EN CONSTRUCCIÓN

#INSTALACIÓN DE MySQL




##Índice de contenido:

1. Instalación de MySQL:	2
1. Instalación en Windows	2
1. Instalación de la parte servidor de MySQL	2
1. Instalación del programa para administrar MySQL	9
1. Instalación en Mac OS X de Apple Macintosh	14
1. Instalación del servidor MySQL en Mac OS X	14
1. Administrar MySQL en Mac OS X	17

--
###Instalación de MySQL:

####Instalación en Windows

En concreto se van a instalar dos programas, el servidor de bases de datos en sí y otro programa para administrar el mismo.

#####Instalación de la parte servidor de MySQL

Usaremos la versión de MySQL 4.1.21 para MS Windows, para ello descarguen  el fichero “mysql-4.1.21-win32.zip” que facilitamos en la plataforma de enseñanza virtual, pueden también descargarlo de la web oficial de MySQL donde también encontrarán el código fuente.

Bajen y descompriman el instalador de Internet, con la opción “Extraer todo...” al pulsar con el botón derecho del ratón. Al hacerlo, se creará un fichero llamado Setup.exe el cual debemos abrir para proceder con la instalación.
Al abrirlo, en la primera ventana pulsen Next para iniciar la instalación: 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-1.PNG)

Pulsen Next sin cambiar el tipo de instalación que viene por defecto: 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-2.PNG)

Pulsen el botón Install para comenzar la instalación real de la aplicación:

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-3.PNG)

Esperen un momento mientras se van copiando los archivos: 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-4.PNG)

Ahora vamos a configurar algunos aspectos básicos del programa, primero elegimos crear una nueva cuenta de usuario de MySQL. Dejar seleccionado “Create a new free MySQL.com account” y pulsar Next.

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-5.PNG)

En las siguientes pantallas vamos a introducir los datos de la nueva cuenta, comenzaremos por la dirección de correo electrónico y la contraseña: 
Email Address: inven@tado.com 
Password: alumno 
Password (again): alumno 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-6.PNG)

Luego los datos nombre y apellido: 
First Name: inven 
Last Name: tado 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-7.PNG)

Y finalizaremos con el código postal, el país y el estado o provincia: 
Zip / Postal Code: 41018 
Country: Spain 
State / Province: Other or N/A 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-8.PNG)

En la siguiente pantalla aparece un resumen de los datos introducidos para confirmarlos con el botón Next: 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-11.PNG)

Para finalizar debemos dejar activada la casilla para configurar el servidor de MySQL, pulsen el botón Finish: 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-12.PNG)

En este momento debemos tener instalado el gestor de bases de datos MySQL. Tras finalizar el proceso de instalación, una nueva ventana ha sido abierta para iniciar la configuración del servidor. 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-13.PNG)

Pulsar el botón Next para iniciar la configuración de MySQL:

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-14.PNG)

Comenzamos la configuración del servidor eligiendo la opción de configuración estándar (Standard Configuration) y pulsando el botón Next: 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-15.PNG)

Con las opciones "Install As Windows Service" (instalar como servicio de Windows) y "Launch the MySQL Server automatically" (arrancar el servidor MySQL de forma automática), pulsaremos el botón Next: 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-16.PNG)

Ahora crearemos una contraseña para administrar el servidor con el usuario root (en español root se traduce como administrador) a la vez que marcamos la opción "[v] Enable root access from remote machines" (permitir el acceso a root desde ordenadores de la red): 
New root password: alumno 
Confirm: alumno 
[v] Enable root access from remote machines

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-17.PNG)

La siguiente pantalla nos prepara para la configuración real del servidor, pulsen el botón Execute: 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-18.PNG)

Y una vez realizada la configuración podemos pulsar el botón Finish para cerrar la ventana: 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-19.PNG)

En este momento debemos tener el servidor de MySQL instalado y funcionando en nuestro ordenador. 
Instalación del programa para administrar MySQL

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-20.PNG)

Todo gestor de bases de datos necesita de un programa que permita administrarlo, entre las tareas de administración están la de poder crear, modificar y eliminar  bases de datos y usuarios del servidor. También debe facilitar labores de mantenimiento como la creación y recuperación de copias de seguridad, etc.

En nuestro caso vamos a utilizar el programa "MySQL Administrator" que pueden descargar de la plataforma de enseñanza virtual, con el nombre mysql-gui-tools seguido de su número de versión, o de la web oficial de MySQL, donde también encontrarán el código fuente.

Una vez descargado comprobarán por su extensión (.msi) que se trata de un instalador para Windows (el formato Windows Installer es MSI), este tipo de instalador asegura la correcta instalación y futura desinstalación del programa.

Ejecuten el instalador y verán aparecer la ventana de bienvenida. Pulsen el botón Next para continuar: 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-21.PNG)

Antes de continuar, pueden ver que el programa se acoge a la licencia GPL, dando las mayores libertades a sus usuarios. Acepten la licencia y pulsen el botón Next: 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-22.PNG)

El programa se instalará en la carpeta de "Archivos de programa" de vuestro equipo, sigan con la instalación pulsando el botón Next: 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-23.PNG)

En la ventana para elegir el tipo de instalación, dejen la opción Complete seleccionada y pulsen Next: 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-24.PNG)


Tras repasar las opciones seleccionadas, comenzar el proceso de instalación real pulsando el botón Install: 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-25.PNG)

Esperen mientras se copian los ficheros: 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-26.PNG)

A continuación nos presentan varios servicios que la empresa desarrolladora de MySQL oferta a los usuarios; en el mundo del software libre (GPL) el negocio está en la venta de productos y sobretodo servicios que complementan al programa principal: Formación, mantenimiento, otras aplicaciones, etc.

Pulsen el botón Next de las siguientes ventanas: 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-27.PNG)



Finalmente pulsaremos el botón Finish para cerrar la ventana del instalador: 

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-28.PNG)

De esta forma hemos finalizado la instalación del Administrador de MySQL. 


Ahora debemos configurar el sistema, para ello deben abrir la aplicación “MySQL Administrator” utilizando el menú Inicio – Todos los programas – MySQL – MySQL Administrator:

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-29.PNG)

Al principio os pide un servidor que debe ser localhost, un usuario: root y la contraseña la dejan en blanco porque no hemos asignado ninguna todavía.


Una vez que hayamos conectado con el servidor, en la opción User Administration, seleccionen el usuario “root” del recuadro User Accounts. A la derecha, en la información del usuario root asignen la contraseña alumno tanto en Password como en Confirm password:

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-30.PNG)


Aceptados los cambios podremos usar MySQL desde otros programas utilizando el servidor localhost, el puerto 3306, el usuario root y la contraseña alumno.

--
###Instalación en Mac OS X de Apple Macintosh

####Instalación del servidor MySQL en Mac OS X
Descargar la versión de MySQL 5.0 compatible con el sistema operativo1 (en el ejemplo, trabajaremos con la versión Mac OS X 10.4.9), en la dirección: 
http://dev.mysql.com/downloads/ , se puede elegir para Mac OS X 10.3 y Mac OS X 10.4

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-31.PNG)

Pulsar la opción:
MySQL_5.0 – Generally Available (GA) release for production use

Buscar, al final de la siguiente página, la opción “Mac OS X (package format)

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-32.PNG)

En función del equipo elegir entre las opciones mostradas y pulsar en “Pick a mirror”, elija si no le suena 32-bit (ejemplo: Mac OS X 10.4 PowerPC, 32 bits).

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-33.PNG)

Pulsen el botón “No thanks, just take me to the downloads!” para no tener que  registrarse:

![DibujoMYSQL-1](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-34.PNG)

Seleccionar el HTTP del Mirror más cercano, en nuestro caso Madrid (si fallara, pueden elegir FTP e incluso un mirror diferente, aunque el más cercano posible).


Y guardar el archivo:

![DibujoMYSQL-35](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-35.PNG)

Ya pueden instalar el programa descargado con el nombre “mysql-5.0.45-osx10.4-powerpc.dmg”



--
####Administrar MySQL en Mac OS X

Ahora vamos a instalar las herramientas para administrar las bases de datos, vuelvan a la dirección: http://dev.mysql.com/downloads/ y pulsar la opción “MySQL GUI Tools”

![DibujoMYSQL-36](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-36.PNG)

Pulsar “Pick a Mirror” del apartado correspondiente a Mac:

![DibujoMYSQL-37](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-37.PNG)


Pulsar en “No thanks, just take me to the downloads!”

![DibujoMYSQL-38](https://raw.githubusercontent.com/Miguel-J/eneboo/master/imagen/dibujoMySQL/DibujoMySQL-38.PNG)

Seleccionar el HTTP del Mirror más cercano, en nuestro caso Madrid, como se hizo en el punto anterior. Y posteriormente instalar el programa con el nombre “mysql-gui-tools-5.0-r12-osx10.4-universal.dmg”

Abran la aplicación “MySQL Administrator”, al principio os pide un servidor que debe ser localhost, un usuario: root y la contraseña la dejan en blanco porque no hemos asignado ninguna todavía. Una vez que hayamos conectado con el servidor, modifiquen con la opción User Administrator al usuario root para asignarle la contraseña alumno. Pueden mirar el apartado correspondiente a Windows para ver cómo hacerlo.
