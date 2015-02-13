

INSTALACIÓN DE MySQL




Índice de contenido
Instalación de MySQL:	2
Instalación en Windows	2
Instalación de la parte servidor de MySQL	2
Instalación del programa para administrar MySQL	9
Instalación en Mac OS X de Apple Macintosh	14
Instalación del servidor MySQL en Mac OS X	14
Administrar MySQL en Mac OS X	17

Instalación de MySQL:

Instalación en Windows

En concreto se van a instalar dos programas, el servidor de bases de datos en sí y otro programa para administrar el mismo.

Instalación de la parte servidor de MySQL

Usaremos la versión de MySQL 4.1.21 para MS Windows, para ello descarguen  el fichero “mysql-4.1.21-win32.zip” que facilitamos en la plataforma de enseñanza virtual, pueden también descargarlo de la web oficial de MySQL donde también encontrarán el código fuente.

Bajen y descompriman el instalador de Internet, con la opción “Extraer todo...” al pulsar con el botón derecho del ratón. Al hacerlo, se creará un fichero llamado Setup.exe el cual debemos abrir para proceder con la instalación.
Al abrirlo, en la primera ventana pulsen Next para iniciar la instalación: 


Pulsen Next sin cambiar el tipo de instalación que viene por defecto: 


Pulsen el botón Install para comenzar la instalación real de la aplicación:


Esperen un momento mientras se van copiando los archivos: 


Ahora vamos a configurar algunos aspectos básicos del programa, primero elegimos crear una nueva cuenta de usuario de MySQL. Dejar seleccionado “Create a new free MySQL.com account” y pulsar Next.


En las siguientes pantallas vamos a introducir los datos de la nueva cuenta, comenzaremos por la dirección de correo electrónico y la contraseña: 
Email Address: inven@tado.com 
Password: alumno 
Password (again): alumno 


Luego los datos nombre y apellido: 
First Name: inven 
Last Name: tado 


Y finalizaremos con el código postal, el país y el estado o provincia: 
Zip / Postal Code: 41018 
Country: Spain 
State / Province: Other or N/A 



En la siguiente pantalla aparece un resumen de los datos introducidos para confirmarlos con el botón Next: 


Para finalizar debemos dejar activada la casilla para configurar el servidor de MySQL, pulsen el botón Finish: 


En este momento debemos tener instalado el gestor de bases de datos MySQL. Tras finalizar el proceso de instalación, una nueva ventana ha sido abierta para iniciar la configuración del servidor. 


Pulsar el botón Next para iniciar la configuración de MySQL:


Comenzamos la configuración del servidor eligiendo la opción de configuración estándar (Standard Configuration) y pulsando el botón Next: 


Con las opciones "Install As Windows Service" (instalar como servicio de Windows) y "Launch the MySQL Server automatically" (arrancar el servidor MySQL de forma automática), pulsaremos el botón Next: 


Ahora crearemos una contraseña para administrar el servidor con el usuario root (en español root se traduce como administrador) a la vez que marcamos la opción "[v] Enable root access from remote machines" (permitir el acceso a root desde ordenadores de la red): 
New root password: alumno 
Confirm: alumno 
[v] Enable root access from remote machines


La siguiente pantalla nos prepara para la configuración real del servidor, pulsen el botón Execute: 


Y una vez realizada la configuración podemos pulsar el botón Finish para cerrar la ventana: 


En este momento debemos tener el servidor de MySQL instalado y funcionando en nuestro ordenador. 
Instalación del programa para administrar MySQL

Todo gestor de bases de datos necesita de un programa que permita administrarlo, entre las tareas de administración están la de poder crear, modificar y eliminar  bases de datos y usuarios del servidor. También debe facilitar labores de mantenimiento como la creación y recuperación de copias de seguridad, etc.

En nuestro caso vamos a utilizar el programa "MySQL Administrator" que pueden descargar de la plataforma de enseñanza virtual, con el nombre mysql-gui-tools seguido de su número de versión, o de la web oficial de MySQL, donde también encontrarán el código fuente.

Una vez descargado comprobarán por su extensión (.msi) que se trata de un instalador para Windows (el formato Windows Installer es MSI), este tipo de instalador asegura la correcta instalación y futura desinstalación del programa.

Ejecuten el instalador y verán aparecer la ventana de bienvenida. Pulsen el botón Next para continuar: 


Antes de continuar, pueden ver que el programa se acoge a la licencia GPL, dando las mayores libertades a sus usuarios. Acepten la licencia y pulsen el botón Next: 


El programa se instalará en la carpeta de "Archivos de programa" de vuestro equipo, sigan con la instalación pulsando el botón Next: 


En la ventana para elegir el tipo de instalación, dejen la opción Complete seleccionada y pulsen Next: 



Tras repasar las opciones seleccionadas, comenzar el proceso de instalación real pulsando el botón Install: 


Esperen mientras se copian los ficheros: 


A continuación nos presentan varios servicios que la empresa desarrolladora de MySQL oferta a los usuarios; en el mundo del software libre (GPL) el negocio está en la venta de productos y sobretodo servicios que complementan al programa principal: Formación, mantenimiento, otras aplicaciones, etc.

Pulsen el botón Next de las siguientes ventanas: 




Finalmente pulsaremos el botón Finish para cerrar la ventana del instalador: 


De esta forma hemos finalizado la instalación del Administrador de MySQL. 


Ahora debemos configurar el sistema, para ello deben abrir la aplicación “MySQL Administrator” utilizando el menú Inicio – Todos los programas – MySQL – MySQL Administrator:


Al principio os pide un servidor que debe ser localhost, un usuario: root y la contraseña la dejan en blanco porque no hemos asignado ninguna todavía.


Una vez que hayamos conectado con el servidor, en la opción User Administration, seleccionen el usuario “root” del recuadro User Accounts. A la derecha, en la información del usuario root asignen la contraseña alumno tanto en Password como en Confirm password:



Aceptados los cambios podremos usar MySQL desde otros programas utilizando el servidor localhost, el puerto 3306, el usuario root y la contraseña alumno.


Instalación en Mac OS X de Apple Macintosh
Instalación del servidor MySQL en Mac OS X
Descargar la versión de MySQL 5.0 compatible con el sistema operativo1 (en el ejemplo, trabajaremos con la versión Mac OS X 10.4.9), en la dirección: 
http://dev.mysql.com/downloads/ , se puede elegir para Mac OS X 10.3 y Mac OS X 10.4


Pulsar la opción:
MySQL_5.0 – Generally Available (GA) release for production use

Buscar, al final de la siguiente página, la opción “Mac OS X (package format)


En función del equipo elegir entre las opciones mostradas y pulsar en “Pick a mirror”, elija si no le suena 32-bit (ejemplo: Mac OS X 10.4 PowerPC, 32 bits).



Pulsen el botón “No thanks, just take me to the downloads!” para no tener que  registrarse:



Seleccionar el HTTP del Mirror más cercano, en nuestro caso Madrid (si fallara, pueden elegir FTP e incluso un mirror diferente, aunque el más cercano posible).


Y guardar el archivo:


Ya pueden instalar el programa descargado con el nombre “mysql-5.0.45-osx10.4-powerpc.dmg”




Administrar MySQL en Mac OS X

Ahora vamos a instalar las herramientas para administrar las bases de datos, vuelvan a la dirección: http://dev.mysql.com/downloads/ y pulsar la opción “MySQL GUI Tools”

 

Pulsar “Pick a Mirror” del apartado correspondiente a Mac:



Pulsar en “No thanks, just take me to the downloads!”



Seleccionar el HTTP del Mirror más cercano, en nuestro caso Madrid, como se hizo en el punto anterior. Y posteriormente instalar el programa con el nombre “mysql-gui-tools-5.0-r12-osx10.4-universal.dmg”

Abran la aplicación “MySQL Administrator”, al principio os pide un servidor que debe ser localhost, un usuario: root y la contraseña la dejan en blanco porque no hemos asignado ninguna todavía. Una vez que hayamos conectado con el servidor, modifiquen con la opción User Administrator al usuario root para asignarle la contraseña alumno. Pueden mirar el apartado correspondiente a Windows para ver cómo hacerlo.
