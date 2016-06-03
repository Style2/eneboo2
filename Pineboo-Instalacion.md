* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 31 de mayo de 2016
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Pineboo-Instalacion)

----

# EN CONSTRUCCION


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

1. Llevamos con usb los repositorios de "pineboo" y "flscriptparser" al directorio raíz..

1. ??


### PASO 4 - ARRANCAR ENEBOO DESDE ORDENADOR APAGADO:

1. Volver a ventanas (Ctrl+Alt+F7) y arrancar el programa (eneboo) desde el explorador de archivos en:
         * /home/linux/Descargas/eneboo--dba/bin

