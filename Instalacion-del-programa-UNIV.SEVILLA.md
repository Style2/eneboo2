* CREADO POR: [Universidad de Sevilla](http://www.us.es): Guillermo Molleda Jimena
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 13 de febrero de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Instalacion-del-programa-UNIV.SEVILLA)

----
###EN CONSTRUCCIÓN

#INSTALACIÓN DEL PROGRAMA CLIENTE DEL ERP: AbanQ




Índice de contenido
Instalación del programa cliente AbanQ:	2
Instalación de AbanQ	2
Ejecución de AbanQ	4
La impresión con AbanQ	5
Caso particular para procesadores de 64 bits:	7

Instalación del programa cliente AbanQ:

Instalación de AbanQ

Descarguen el fichero de instalación desde la plataforma de enseñanza virtual de la asignatura o desde la dirección de internet oficial de la empresa creadora del software, para el sistema operativo que utilicen (AbanQ ejecutable para Linux, MS Windows o Mac OS X):
http://www.abanq.com/productos/productos.php?fam=desc

Acepten el contrato de licencia y descarguen el programa.


Descompriman el fichero descargado y ejecútenlo como administrador del equipo:
En Linux y Windows simplemente un doble clic del ratón comenzará la instalación, sigan las instrucciones que vayan saliendo.
En Mac OS X es fácil la instalación, ya que se trata de un paquete autoinstalable.

La instalación comienza preguntando el idioma y pidiendo confirmación para instalarlo en el sistema:

Sigan el proceso de instalación, comencemos cerrando todas las aplicaciones abiertas, yo añadiría que hasta desactiven el antivirus (algunas veces los antivirus dificultan la instalación de programas generando errores), y pulsen el botón Siguiente tal como nos pide la ventana inicial:

Lean los términos del contrato, está sujeto a la licencia GPL (Licencia Pública General) que le garantiza la libertad de compartir y modificar el software libre. Pulsen el botón Instalar para proseguir:

Al terminar la instalación podemos dejar que se abra el programa y leer el fichero Léame, antes de continuar os informamos de los siguiente:

En Linux, se ha creado un enlace en el menú Aplicaciones – AbanQ, mientras que en Windows se han creado enlaces  para su ejecución tanto en el escritorio como en el menú Inicio – Todos los programas.

Ejecución de AbanQ

Abran el programa AbanQ que acaban de instalar, pulsen el botón vertical que aparece en el margen derecho para abrir las opciones de conexión tal como ven más abajo, elijan el Controlador: PostgreSQL o MySQL, según sea el que hayan instalado. Dejen el Servidor: localhost (localhost es equivalente a la dirección IP 127.0.0.1 y siempre señala al propio ordenador) y el puerto 5432 si usan PostgreSQL o 3306 si fuera MySQL. En la parte izquierda pongan el nombre de la base de datos a usar (envoltosa), el usuario (postgres para PostgreSQL o root para MySQL) y la contraseña (alumno):


Pulsen el botón Conectar para iniciar AbanQ.

En GNU/Linux, si comprueban que no se pueden escribir vocales acentuadas, abran una terminal (menú Aplicaciones – Accesorios – Terminal) y prueben los siguientes comandos escribiendo alguna vocal acentuada en el lugar destinado al nombre de la base de datos:

LANG=es_ES.ISO-8859-1 fllite
LANG=es_ES.ISO-8859-15 fllite
LANG=es_ES.UTF-8@euro fllite
XMODIFIERS='' LANG=es_ES@euro fllite 

En cuanto funcionen los acentos con alguno de ellos, salgan de AbanQ con el botón cancelar y prueben a automatizar el comando apropiado: Desde la misma terminal que tengan abierta pueden crear un fichero con las dos líneas propuestas a continuación, y hacerlo ejecutable

sudo gedit /usr/bin/fllite_es

#!/bin/sh 
XMODIFIERS='' LANG=es_ES@euro fllite # Aquí el comando elegido

sudo chmod 755 /usr/bin/fllite_es

Cambien el menú, con el botón derecho del ratón sobre el menú aplicaciones, editar los menús y en la entrada Aplicaciones – Otras – AbanQ con el botón derecho del ratón cambien el comando a llamar a “/usr/bin/fllite_es” sin las comillas.
La impresión con AbanQ

No es necesario seguir este apartado para la asignatura, son instrucciones para poder imprimir correctamente los informes de AbanQ: listados de artículos, pedidos, facturas, etc.

En linux, al menos en sistemas basados en Debian (Ubuntu, Guadalinex, Linex), hay que crear un enlace a las impresoras del sistema:
Abrir la consola con el menú Aplicaciones – Accesorios – Terminal, y escribir las órdenes,
sudo mv /etc/printcap /etc/printcapold
sudo ln -s /var/run/cups/printcap /etc/printcap

En Windows es necesario instalar el programa Ghostscript para imprimir correctamente, a continuación explicamos la forma de instalarlo:

Primero descargar el programa siempre que no sea mayor que la version 9.0:
Para Windows de 32 bits sirve la versión 8.53 de la dirección:
http://ftp.us.es/ftp/especiales/sifico/gs853w32.exe
Y para Windows de 64 bits sirve la version 8.71 de la direccion:
http://ftp.us.es/ftp/especiales/sifico/gs871w64.exe

Si el directorio no existiera, habrá que buscar el programa, en su versión GPL, en http://www.ghostscript.com.

Hay que instalarlo como usuario Administrador del sistema operativo, para ello cierre sesión del usuario de cuenta limitada, sólo si estuviera trabajando con cuenta limitada, e inicie sesión de Windows con su cuenta de administrador. Si no saben de qué hablamos, es porque ya es administrador del equipo, tenga cuidado con los virus ya que van dirigidos a usuarios como tú.

Ejecuten el programa instalador descargado antes y pulsen el botón Setup de la primera ventana:

Atención, en la siguiente ventana seleccionen la opción "[V] All users" y después pulsar Install:

Tras la instalación pueden cerrar las ventanas que queden abiertas. No hemos terminado ya que para que el programa funcione es necesario que su directorio de instalación esté en la variable de entorno PATH. Para añadirlo, en el Windows XP (como administrador), hacer lo siguiente:

Pulsa en "Mi PC" con el botón derecho del ratón y dirigirse a Propiedades, luego en la pestaña Opciones avanzadas pulsa el botón "Variables de entorno":

Aparece otra ventana, en el cuadro inferior "variables del sistema" selecciona para modificar la variable Path, introducir al final de la línea, sin las comillas pero con el punto y coma del principio, lo siguiente: ";C:\Archivos de programa\gs\gs8.53\bin" o el nombre del directorio donde se haya instalado el ghostscript:

Aceptar, cerrar la sesión de administrador para volver al de usuario limitado y ya podrán imprimir perfectamente con fllite. Para comprobar que todo es correcto, en Inicio-Ejecutar escriban: gswin32 y debe salir la ventana de comandos de ghostscript de la que pueden salir con la orden "quit" y pulsando ENTER.
Caso particular para procesadores de 64 bits:

Si usted tiene un procesador y un sistema operativo de 64 bits, descargue el instalador correspondiente a dicha arquitectura desde la web de AbanQ: http://www.abanq.com
