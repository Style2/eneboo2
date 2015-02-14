* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 14 de febrero de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Instalacion-en-linux)

----


# INSTALACION DE ENEBOO EN LINUX CON MySQL

## Linux-Pasos:

1. Descargar y descomprimir el motor de Eneboo para Linux en el apartado [Versiones Estables](http://www.eneboo.org/site/stable). Buscaremos el _Build dbAdmin Linux_ de 32 o 64 bits.
     * Hacer click en el link y (para Mozilla: darle a la flecha azul de arriba-derecha) luego "mostrar en carpeta" (dibujo de la derecha). Buscar el archivo y con botón derecho: "extraer aqui"

2. Descargar e instalar el gestor de bases de datos:
     * 2.A **PostgreSQL** (recomendamos la versión 8.4) para Linux del [área de descarga de PostgreSQL](http://www.enterprisedb.com/products-services-training/pgdownload). La instalación solicitará un usuario y una contraseña de administrador de la base de datos que conviene anotar, ya que serán necesarios más adelante.
     * 2.B **MySQL**
     * instalo la 
          * "Begin Your Download - mysql-server_5.6.23-1ubuntu14.10_i386.deb-bundle.tar"
          * http://dev.mysql.com/downloads/file.php?id=455351
          * ...registrar? "no thanks, just start my download" (y esperar a flecha azul)...mirar en carpeta...descomprimir aqui...y crea 6 carpetas??
          * error....miro la linux-generic...otro dia...

3. Descargar el [paquete de Eneboo Standard](http://www.eneboo.com/pub/contrib/standard-modules/standard.eneboopkg).
4. [Cargar el paquete de Eneboo Standard](#cargar-el-paquete-de-eneboo-standard).


## Cargar el paquete de Eneboo Standard
![Pantalla de conexión](https://raw.githubusercontent.com/eneboo/doc/master/images/standard/conectar.png)


1. Abrir Eneboo. Aparecerá la pantalla _Conectar_.
1. Rellenar los campos con los siguientes valores:
    * Base de datos: standard
    * Usuario: el administrador de la base de datos PostgreSQL.
    * Contraseña: la del administrador de la base de datos PosgtreSQL.
        
1. Pulsar el botón de la flecha hacia la derecha _Más opciones_.
1. Rellenar los campos de esta pantalla con los siguientes valores: 
    * Controlador: PosgtreSQL
    * Servidor: localhost
    * Puerto: 5432
1. Pulsar el botón _Conectar_. Se mostrará un mensaje con el texto _La base de datos standard no existe ¿Quiere crearla?_. Pulsar _Sí_.
1. Se iniciará el programa y se mostrará el entorno Eneboo. En el área de _Módulos_ de la parte izquierda, abrir la opción _Sistema -> Administración -> Cargar Paquete de módulos_.
1. Localizar el archivo standard.eneboopkg y pulsar _Abrir_. Cuando finalice la carga, Eneboo Standard estará listo para empezar a trabajar.