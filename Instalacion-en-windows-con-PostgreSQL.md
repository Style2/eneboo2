* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 6 de junio de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Instalacion-en-windows-con-PostgreSQL)

----
(EN CONSTRUCCIÓN)

# INSTALACION DE ENEBOO EN WINDOWS CON POSTGRESQL


###PASO 1.-Descargar e instalar el SERVIDOR DE BASE DE DATOS WAMP (incluye APACHE, POSTGRESQL Y PHPAdminIII..) de:

2. Descargar e instalar el gestor de bases de datos:

     * 2.A **PostgreSQL**

     * AUTOMATICO:
          * **http://www.postgresql.org/download/**
          * para WINDOWS 64 bits (ordenadores nuevos con Windows 8.1): descargo la versión de WINDOWS 64 bits que contiene: 
          * para WINDOWS 32 bits (WINDOWS XP): descargo la versión de WINDOWS 32 bits que contiene: 
   * 2.A **PostgreSQL** (recomendamos la versión 8.4) para windows del [área de descarga de PostgreSQL](http://www.enterprisedb.com/products-services-training/pgdownload). La instalación solicitará un usuario y una contraseña de administrador de la base de datos que conviene anotar, ya que serán necesarios más adelante.

---
####PASO 2.- EJECUTAR PgAdminIII ....
* (ESTE PASO NO ES NECESARIO)

---
####PASO 3.- CREAR UNA BASE DE DATOS EN PgAdminIII
* (ESTE PASO NO ES NECESARIO)
* no es imprescindible este paso porque Eneboo lo crea la primera vez que se conecta a la base de datos....
* (ESTO PARA PRIMERA INSTALACION, SI ES RE-INSTALAR HAY QUE SALTARSE ESTE PASO & INSTALAR EL DUMP-COPIA DE SEGURIDAD)
* ...lo hace en: 
* ….cotejamiento por defecto: 

---
####PASO 4.-DESCARGAR EL PROGRAMA ENEBOO:

* Bajarlo de:
     * A) en http://eneboo.org/pub/contrib/ (ultimas versiones-releases...ojo: LAS BETA, NO)
     * B) en www.eneboo.org (el que incluye PostgreSQL, MySQL u otro). Ir a “descargas”......”versiones estables”.....abajo....Hay dos opciones:
          * B.1)...en el PRIMER ORDENADOR DE LA RED o “servidor”.....elegir la **version “DBA”**.
                 * sirve para instalar módulos personalizados y otras tareas de "Administrador" 
          * B.2)...en los SIGUIENTES “ordenadores-clientes”.....elegir la **versión “QUICK”**.
                 * sirve para ordenadores donde NO QUIERES que estropeen/instalen NADA y evita problemas.

1. Descargar y descomprimir el motor de Eneboo para Linux en el apartado [Versiones Estables](http://www.eneboo.org/site/stable). Buscaremos el _Build dbAdmin Windows_ de 32 o 64 bits.
     * Hacer click en el link y (para Mozilla: darle a la flecha azul de arriba-derecha) luego "mostrar en carpeta" (dibujo de la derecha). Buscar el archivo y con botón derecho: "extraer aqui"


---
####PASO 5.-ARRANCAR EL PROGRAMA ENEBOO:

* ejecutar el archivo **eneboo.exe** del subdirectorio **bin**. Por ejemplo:("C:\eneboo-2.4.0.2-dba-win32\bin\eneboo.exe")
* **OJO: ANTES EL SERVIDOR PostgreSQL TIENE QUE ESTAR FUNCIONANDO**.
     * ejecutar el archivo ("C:\eneboo-2.4.0.2-dba-win32\bin\eneboo.exe")
     * Arrancar el programa (eneboo) desde el explorador de archivos en la carpeta donde se ha descargado el programa.       
     * Aparecerá la pantalla _Conectar_.

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-01.jpg)
1. Rellenar los campos con los siguientes valores:
    * Base de datos: (nombre empresa)
    * Usuario: postgres (o el que hemos puesto como administrador de la base de datos PostgreSQL-ver phpMyAdminIII).
    * Contraseña: (la del administrador de la base de datos PostgreSQL-ver phpMyAdminIII).
1. Pulsar el botón de la flecha hacia la derecha _Más opciones_.

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-02.jpg)        

1. Rellenar los campos de esta pantalla con los siguientes valores: 
    * Controlador: POSTGRESQL
    * Servidor: localhost
    * Puerto: 5432
1. Pulsar el botón _Conectar_. Se mostrará un mensaje con el texto _La base de datos standard no existe ¿Quiere crearla?_. Pulsar _Sí_.

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-03.jpg)

1. Una vez iniciado el programa Eneboo se mostrará el entorno Eneboo.


![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-02.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-03.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-04.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-05.jpg)

---
####PASO 6.-DESCARGAR LOS “MÓDULOS” de eneboo...

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-01.jpg)
* Se pueden descargar de varios sitios o "repositorios", hay unos que llevan más "extensiones" añadidas a la "mezcla básica" que otros...:

* http://www.eneboo.org/site/node/16
1. Descargar el [paquete de Eneboo Standard](http://www.eneboo.com/pub/contrib/standard-modules/standard.eneboopkg).
1. “Si desea descargar la última versión de nuestros módulos oficiales en ZIP, haga clic en el siguiente enlace: https://github.com/gestiweb/eneboo-modules/zipball/master “ (8 megas)
1.  “todos los módulos de gestiweb” descargar en zip  (ESTE ES MEJOR, DESCOMPRIME TODOS LOS MODULOS EN UNA CARPETA Y LUEGO SE INSTALAN DESDE EL PROGRAMA ENEBOO):
1. Otro lugar de descarga: [Repos del git de KLO-MANOLO](https://github.com/klo-manolo/eneboo-modules/archive/master.zip).

---
####PASO 7.-INSTALAR LOS MÓDULOS DE ENEBOO:

* (hay 3 opciones):

* OPCIÓN A) todos de golpe en "PAQUETE":

      * “modulos estandar en paquete eneboo” o: standard.eneboopkg
      1. En el área de _Módulos_ de la parte izquierda, abrir la opción _Sistema -> Administración -> Cargar Paquete de módulos_.
      1. Localizar el archivo standard.eneboopkg y pulsar _Abrir_. Cuando finalice la carga, Eneboo Standard estará listo para empezar a trabajar.

* OPCIÓN B) todos de golpe en "CARPETA DE MÓDULOS"

     * “modulos estandar de eneboo” descargar en zip: eneboo_standard.zip (3 megas)o (ESTE ES BUENO, DESCOMPRIME SOLO LOS MODULOS DEL AREA DE CONTABILIDAD Y FACTURACION  EN UNA CARPETA Y LUEGO SE INSTALAN DESDE EL PROGRAMA ENEBOO):


* OPCIÓN C) De uno en uno o "MÓDULO A MÓDULO":

     * hay que ir a la carpeta dende están y 
     * al acabar salir del programa y volver a entrar


![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-02.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-03.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-04.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-05.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-06.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-07.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-08.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-09.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-10.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-11.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-12.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-13.jpg)
---
####PASO 8.-REGENERAR LA BASE DE DATOS DESPUÉS DE CARGAR MODULOS:

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-13.jpg)
* ...entrar en “eneboo-sistema-administración-cargar Módulo”....e ir a la carpeta donde están guardados o descomprimidos del paso anterior...
* y después de cada uno:  ...ir a “eneboo-sistema-administración-”+mas”-principal-Regenerar la base de datos”..
...hay que “regenerar la base de datos” y salir del programa y volver a entrar después de haber instalado cada módulo......
         
