* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 5 de junio de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Instalacion-en-linux-con-PostgreSQL)

----


# INSTALACION DE ENEBOO EN LINUX CON POSTGRESQL


**NOTA SOBRE LINUX**:
* Cómo llego a la **consola"?
     * Entrar a la consola desde la vista-escritorio: Ctrl+Alt+F1
     * Salir de la consola hacia la vista-escritorio: Ctrl+Alt+F7

* Qué teclas sirven para **copiar-y-pegar** el texto en la consola en Linux o Unix ?:
     * Ctrl+Shift+c = copiar
     * Ctrl+Shift+V.= pegar

* Cómo extraer de forma segura un USB?
     * vas a la consola con Ctrl+Alt+F1 y escribes **umount /media/linux(o nombre ordenador)/(nombre de volumen del usb)**

----

### PASO 1 - INSTALAMOS Y ARRANCAMOS EL SERVIDOR:

#####1. (PARA postgreSQL): 

Para Linux-UBUNTU "activamos/instalamos" el servidor de postgreSQL que lleva:

     sudo apt-get postgresql

Y luego Ir a consola (Ctrl+Alt+F1) y "arrancar":

     sudo service postgresql start


### PASO 2 - CREAMOS USUARIO Y BASE DE DATOS:

https://www.nanotutoriales.com/instalacion-de-postgresql-server

https://www.nanotutoriales.com/como-crear-un-usuario-y-asignarle-permisos-en-postgresql


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

ejemplo: ALTER USER Postgres WITH PASSWORD 'postgres';


Para salir del cliente debes escribir el comando \q seguido de la tecla Enter.

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


## Pasos:

1. Descargar y descomprimir el motor de Eneboo para Linux en el apartado [Versiones Estables](http://www.eneboo.org/site/stable). Buscaremos el _Build dbAdmin Windows_ de 32 o 64 bits.
     * Hacer click en el link y (para Mozilla: darle a la flecha azul de arriba-derecha) luego "mostrar en carpeta" (dibujo de la derecha). Buscar el archivo y con botón derecho: "extraer aqui"


2. Descargar e instalar el gestor de bases de datos:

     * 2.A **PostgreSQL**

     * AUTOMATICO:
          * **http://www.postgresql.org/download/**
          * descargo la versión de WINDOWS 64 bits que contiene: 


----------------------------

CONTINUARÁ (lo que sigue no vale)


     * Arrancar el programa (eneboo) desde el explorador de archivos en:
         * /home/linux/Descargas/eneboo--dba/bin

1. Abrir Eneboo. Aparecerá la pantalla _Conectar_.

![Pantalla de conexión](https://raw.githubusercontent.com/eneboo/doc/master/images/standard/conectar.png)

1. Rellenar los campos con los siguientes valores:
    * Base de datos: (nombre empresa)
    * Usuario: postgres (o el administrador de la base de datos PostgreSQL-ver phpMyAdminIII).
    * Contraseña: (la del administrador de la base de datos PostgreSQL-ver phpMyAdminIII).
        
1. Pulsar el botón de la flecha hacia la derecha _Más opciones_.
1. Rellenar los campos de esta pantalla con los siguientes valores: 
    * Controlador: POSTGRESQL
    * Servidor: localhost
    * Puerto: 5432
1. Pulsar el botón _Conectar_. Se mostrará un mensaje con el texto _La base de datos standard no existe ¿Quiere crearla?_. Pulsar _Sí_.

# INSTALACIÓN DE MÓDULOS:

1. Descargar el [paquete de Eneboo Standard](http://www.eneboo.com/pub/contrib/standard-modules/standard.eneboopkg).
1. [Cargar el paquete de Eneboo Standard](#cargar-el-paquete-de-eneboo-standard).
1. Una vz iniciado el programa Eneboo se mostrará el entorno Eneboo.
1. En el área de _Módulos_ de la parte izquierda, abrir la opción _Sistema -> Administración -> Cargar Paquete de módulos_.
1. Localizar el archivo standard.eneboopkg y pulsar _Abrir_. Cuando finalice la carga, Eneboo Standard estará listo para empezar a trabajar.

# ARRANCAR ENEBOO DESDE ORDENADOR APAGADO:

1. Ir a consola (Ctrl+Alt+F1) y arrancar XAMPP: `$ sudo /opt/lampp/lampp start`
1. Volver a ventanas (Ctrl+Alt+F7) y arrancar el programa (eneboo) desde el explorador de archivos en:
         * /home/linux/Descargas/eneboo--dba/bin

# OTROS: instalacion con PostgreSQL:

   * 2.B MY SQL .....NOTA: ESTO NO FUNCIONÓ: instalo la:

          * "Begin Your Download - mysql-server_5.6.23-1ubuntu14.10_i386.deb-bundle.tar"
          * http://dev.mysql.com/downloads/file.php?id=455351
          * ...registrar? "no thanks, just start my download" (y esperar a flecha azul)...mirar en carpeta...descomprimir aqui...y crea 6 carpetas??
          * error....miro la linux-generic...otro dia...

   * 2.A **PostgreSQL** (recomendamos la versión 8.4) para Linux del [área de descarga de PostgreSQL](http://www.enterprisedb.com/products-services-training/pgdownload). La instalación solicitará un usuario y una contraseña de administrador de la base de datos que conviene anotar, ya que serán necesarios más adelante.