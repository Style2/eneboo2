Archivo original: [ENEBOO/doc](https://github.com/eneboo/doc/wiki/[Eneboo Standard] Instalación)
Actualizado: 29-enero-2015
# Instalador automático
El instalador permite que en pocos minutos Eneboo Standard esté listo para trabajar. El instalador realiza las siguientes tareas de forma automática:

* Instala el motor de Eneboo.
* Instala el gestor de bases de datos PostgreSQL con la configuración por defecto.
* Carga los módulos y extensiones del proyecto Eneboo Standard.
    
Se puede descargar en el apartado [Versiones Estables](http://www.eneboo.org/site/stable) del área de descarga de Eneboo. Buscaremos el _Windows Installer Quick_ que mejor se adapte a nuestras necesidades (Windows o Linux, 32 ó 64 bits).

De momento no hay instalador automático para Mac.

# Instalación manual

## Macintosh

1. Descargar y descomprimir el [motor de Eneboo para Mac OS X] (http://eneboo.com/pub/eneboo/builds/v2.4.0/eneboo-v2.4.0-alpha5-mac32.zip) (sólo para 32 bits).
2. Descargar e instalar el gestor de bases de datos PostgreSQL (recomendamos la versión 8.4) para Mac del [área de descarga de PostgreSQL](http://www.enterprisedb.com/products-services-training/pgdownload). La instalación solicitará un usuario y una contraseña de administrador de la base de datos que conviene anotar, ya que serán necesarios más adelante.
3. Descargar el [paquete de Eneboo Standard](http://www.eneboo.com/pub/contrib/standard-modules/standard.eneboopkg).
4. [Cargar el paquete de Eneboo Standard](#cargar-el-paquete-de-eneboo-standard).
    
## Linux

1. Descargar y descomprimir el motor de Eneboo para Linux en el apartado [Versiones Estables](http://www.eneboo.org/site/stable). Buscaremos el _Build dbAdmin Linux_ de 32 o 64 bits.
2. Descargar e instalar el gestor de bases de datos PostgreSQL (recomendamos la versión 8.4) para Linux del [área de descarga de PostgreSQL](http://www.enterprisedb.com/products-services-training/pgdownload). La instalación solicitará un usuario y una contraseña de administrador de la base de datos que conviene anotar, ya que serán necesarios más adelante.
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