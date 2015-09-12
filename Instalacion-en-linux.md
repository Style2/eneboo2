* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 12 de septiembre de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Instalacion-en-linux)

----


# INSTALACION DE ENEBOO EN LINUX CON MySQL

## Índice de instalación en Linux-Pasos:

1. [Descargar e Instalar el motor Eneboo.](#1-descargar-e-instalar-el-motor-eneboo)
2. [Instalar un gestor de bases de datos (recomendado LAMPP con MySQL).](#2-descargar-e-instalar-un-gestor-de-bases-de-datos-lampp)
3. [Acceder a la aplicación.](#3-acceder-a-la-aplicación)
4. [Cargar el paquete de módulos (por ejemplo: Eneboo Standard).](#4-cargar-el-paquete-de-módulos)


# 1. Descargar e instalar el motor Eneboo:

1. Descargar y descomprimir el motor de Eneboo para Linux en el apartado [Versiones Estables]

(http://www.eneboo.org/site/stable). Buscaremos el _Build dbAdmin Linux_ de 32 o 64 bits.
     * Hacer click en el link y (para Mozilla: darle a la flecha azul de arriba-derecha) luego "mostrar en carpeta" (dibujo de la derecha). Buscar el archivo y con botón derecho: "extraer aqui"


#2. Descargar e instalar un gestor de bases de datos LAMPP:

     * 2.B **MySQL**

     * INSTALAR XAMP (equivalente a wampserver):
          * **www.apachefriends.org/download**
          * descargo la versión de 32 bits que contiene: "Includes: Apache 2.4.10, MySQL 5.6.21, PHP 5.5.19 & PEAR + SQLite 2.8.17/3.7.17 + multibyte (mbstring) support, Perl 5.16.3, ProFTPD 1.3.4c, phpMyAdmin 4.2.11, OpenSSL 1.0.1j, GD 2.0.35, Freetype2 2.4.8, libpng 1.5.9, gdbm 1.8.3, zlib 1.2.8, expat 2.0.1, Sablotron 1.0.3, libxml 2.0.1, Ming 0.4.5, Webalizer 2.23-05, pdf class 0.11.7, ncurses 5.9, pdf class 0.11.7, mod_perl 2.0.8-dev, FreeTDS 0.91, gettext 0.18.1.1, IMAP C-Client 2007e, OpenLDAP (client) 2.4.21, mcrypt 2.5.8, mhash 0.9.9.9, cUrl 7.30.0, libxslt 1.1.28, libapreq 2.12, FPDF 1.7, ICU4C Library 4.8.1, APR 1.4.6, APR-utils 1.5.1"
          * darle a la flecha azul...ver en carpeta...ejecutar?
          * ayuda on-line: `www.apachefriends.org/faq_linux.html`
            * a) descargar la versión elegida y 32-bit o 64-bit.
            * b) situarse en el subdirectorio de la descarga del "installer"
            * c) dar permisos al instalador:
                 * Ctr+Alt+F1
                 * `$ chmod 755 xampp-linux-5.5.19-0-installer.run` (en mi caso, cambiar por la versión descargada)
            * d) ejecutar el installer
                 * `$ sudo ./xampp-linux-*-installer.run` (uhm, parece que con el * también funciona)
                 * opciones:
                     * instalar XAMPP Developer Files? "Y" (por si acaso digo "Y" a todo...)
                     * "Y" a todo...instala en directorio: "/opt/lampp" (aprox. 10 minutos)
            * Salir de consola: Ctrl+Alt+F7 y verificar en mozilla: "localhost"...luego "español" y "status" en menú izquierda

* aquí meter captura pantalla XAMPP

* arrancar XAMPP: `$ sudo /opt/lampp/lampp start`
* arrancar mySQLserver: `$ sudo /opt/lampp/bin/mysql.server start`

* configurar seguridad XAMPP: `$ sudo /opt/lampp/lampp security (xampp=usuario)`
* error al conectar por eneboo....111 cannt connect...????
* edito my.cnf de /opt/lampp/etc y modifico las líneas:
     * (aprox.linea 35) max_allow_packet=2M (había 1M)...esto por un problema con una tabla .ui del modulo contable...
     * añado # a la línea 30: user=mysql
     * añado # a la línea : skipnetworking.....peeero no graba....como?????
     * ayuda: `http://es.kioskea.net/faq/312-seguridad-privilegios-de-acceso-gnu-linux`
     * ir a la consola y mirar los permisos en el directorio: `ls -l`
        * `-rw-r--r-- 1 root root fecha my.cnf`
     * cambio los permisos de escritura: `$ sudo chmod a+w my.cnf`
     * ahora vuelvo (Ctrl+Alt+F7) al editor del explorador de archivos y hago los cambios descritos antes...ok
     * de vuelta a consola y devuelvo los permisos:
        * `$ sudo chmod a-w my.cnf`
        * `$ sudo chmod u+w my.cnf` 
     * ejecuto XAMPP: `$ sudo /opt/lampp/lampp start`

     * Salir de consola: Ctrl+Alt+F7 

     * y **verificar que funciona** en mozilla/chrome poniendo la dirección: "http://localhost"...luego "español" y "status" en menú izquierda

     * Verificar usuarios en phpMyadmin (menú izquierda-abajo)

#3. Acceder a la aplicación: 

     * Arrancar el programa (eneboo) desde el explorador de archivos en:
         * /home/linux/Descargas/eneboo--dba/bin


Abrir Eneboo. Aparecerá la pantalla _Conectar_.

![Pantalla de conexión](https://raw.githubusercontent.com/eneboo/doc/master/images/standard/conectar.png)

1. Rellenar los campos con los siguientes valores:
    * Base de datos: (nombre empresa)
    * Usuario: root (o el administrador de la base de datos MySQL-ver phpMyAdmin).
    * Contraseña: (la del administrador de la base de datos MySQL-ver phpMyAdmin).
        
1. Pulsar el botón de la flecha hacia la derecha _Más opciones_.

1. Rellenar los campos de esta pantalla con los siguientes valores: 
    * Controlador: MySQL_NO_INNODB
    * Servidor: localhost
    * Puerto: 3306

1. Pulsar el botón _Conectar_. Se mostrará un mensaje con el texto _La base de datos standard no existe ¿Quiere crearla?_. Pulsar _Sí_.

#4. Cargar el paquete de módulos:

1. Descargar el [paquete de Eneboo Standard](http://www.eneboo.com/pub/contrib/standard-modules/standard.eneboopkg).
1. [Cargar el paquete de Eneboo Standard](#cargar-el-paquete-de-eneboo-standard).
1. Una vz iniciado el programa Eneboo se mostrará el entorno Eneboo.
1. En el área de _Módulos_ de la parte izquierda, abrir la opción _Sistema -> Administración -> Cargar Paquete de módulos_.
1. Localizar el archivo standard.eneboopkg y pulsar _Abrir_. Cuando finalice la carga, Eneboo Standard estará listo para empezar a trabajar.

#### ARRANCAR ENEBOO DESDE ORDENADOR APAGADO:

1. Ir a consola (Ctrl+Alt+F1) y arrancar XAMPP: `$ sudo /opt/lampp/lampp start`
1. Volver a ventanas (Ctrl+Alt+F7) y arrancar el programa (eneboo) desde el explorador de archivos en:
         * /home/linux/Descargas/eneboo--dba/bin

#### OTROS: instalacion con PostgreSQL:

   * 2.B MY SQL .....NOTA: ESTO NO FUNCIONÓ: instalo la:
          * "Begin Your Download - mysql-server_5.6.23-1ubuntu14.10_i386.deb-bundle.tar"
          * http://dev.mysql.com/downloads/file.php?id=455351
          * ...registrar? "no thanks, just start my download" (y esperar a flecha azul)...mirar en carpeta...descomprimir aqui...y crea 6 carpetas??
          * error....miro la linux-generic...otro dia...
   * 2.A **PostgreSQL** (recomendamos la versión 8.4) para Linux del [área de descarga de PostgreSQL](http://www.enterprisedb.com/products-services-training/pgdownload). La instalación solicitará un usuario y una contraseña de administrador de la base de datos que conviene anotar, ya que serán necesarios más adelante.