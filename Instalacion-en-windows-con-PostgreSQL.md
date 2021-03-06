* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 10 de junio de 2016
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Instalacion-en-windows-con-PostgreSQL)

----

###(EN CONSTRUCCIÓN)

# INSTALACION DE ENEBOO EN WINDOWS CON PostgreSQL


###PASO 1.-Descargar e instalar el SERVIDOR DE BASE DE DATOS (incluye POSTGRESQL Y PgAdminIII..) de:

* Descargar e instalar el gestor de bases de datos:

     * **PostgreSQL**

     * INSTALADOR AUTOMÁTICO:
          * **http://www.postgresql.org/download/**
          * Selecciono el "Download the installer from EnterpriseDB for all supported versions. " que te lleva a:
          * donde elijo "Installer version Version 9.5.3  [Readme file for customers interested in using PL/Perl, PL/Python or PL/Tcl]", según el sistema operativo:
          * para WINDOWS 64 bits (ordenadores nuevos con Windows 8.1): descargo la versión de WINDOWS 64 bits que contiene: 
          * para WINDOWS 32 bits (WINDOWS XP): descargo la versión de WINDOWS 32 bits que contiene: 

   * **PostgreSQL** (recomendamos la versión 8.4) para windows del [área de descarga de PostgreSQL](http://www.enterprisedb.com/products-services-training/pgdownload). 

    * La instalación solicitará un usuario y una contraseña de administrador de la base de datos que conviene anotar, ya que serán necesarios más adelante. (por ejemplo: "postgres" y "postgres" sin comillas)

---
####PASO 2.-DESCARGAR EL PROGRAMA ENEBOO:

* Bajarlo de:
     * en http://eneboo.org/pub/contrib/ (ultimas versiones-releases, por ejemplo: "2.4.5.1-rc8")
     * Hay dos opciones:

          * DBA)...en el PRIMER ORDENADOR DE LA RED o “servidor”.....elegir la **version “DBA”**.

                 * sirve para instalar módulos personalizados y otras tareas de "Administrador" 
                 * (http://www.eneboo.org/site/stable). Buscaremos el _Build dbAdmin Windows_ de 32 o 64 bits.
                 * Hacer click en el link y (para Mozilla: darle a la flecha azul de arriba-derecha) luego "mostrar en carpeta" (dibujo de la derecha). Buscar el archivo y con botón derecho: "extraer aqui"

          * QUICK)...en los SIGUIENTES “ordenadores-clientes”.....elegir la **versión “QUICK”**.

                 * sirve para ordenadores donde NO QUIERES que estropeen/instalen NADA, no aparece el "Área de sistema" y evitas problemas...


---
####PASO 3.- EJECUTAR PgAdminIII ....

* (ESTE PASO ES NECESARIO PARA QUE FUNCIONE EL SERVIDOR)
* Ir a "servers" y con el botón de la derecha darle a la versión instalada y a la opción "Connect"...

* En el caso de dar algún mensaje de "error de conexión", ir al "Sistema de Windows" (con permisos de administrador) y re-iniciar el servicio MANUALMENTE:

https://www.postgresql.org/message-id/BANLkTi%3DOQc_FiiMhhiKyKb1P4%3DM7s9bGEg@mail.gmail.com

"Si el problema persiste, puede que haya quedado algún otro problema serio, deberías iniciarlo manualmente por consola y ver que sucede, pOr ej, ir a Inicio, ejecutar, cmd y tipear:"

     runas /user:postgres cmd (ESTO NO ES IMPRESCINDIBLE)
     cd C:\Program Files\PostgreSQL\9.5\data
     pg_ctl.exe restart -D ..\data


---
####PASO 4.- CREAR UNA BASE DE DATOS EN PgAdminIII

* (ESTE PASO ES NECESARIO LA PRIMERA VEZ, porque NO la crea el mismo programa Eneboo al conectar- Aunque en MySQL con WAMP SÍ LO HACÍA...)
* Ir a PgAdminIII, luego a "servers", luego a "bases de datos" y con el botón de la derecha darle "NUEVA BASE DE DATOS"...y luego a "conectar"
* (ESTO PARA PRIMERA INSTALACION, SI ES RE-INSTALAR HAY QUE SALTARSE ESTE PASO & INSTALAR EL DUMP-COPIA DE SEGURIDAD)
* ….cotejamiento por defecto: (lo hace todo automático...)

---
####PASO 5.-ARRANCAR EL PROGRAMA ENEBOO:

* ejecutar el archivo **eneboo.exe** del subdirectorio **bin**. Por ejemplo:("C:\eneboo-2.4.0.2-dba-win32\bin\eneboo.exe")
* **OJO: ANTES EL SERVIDOR PostgreSQL TIENE QUE ESTAR FUNCIONANDO** (ver el Paso 3).
     * ejecutar el archivo ("C:\eneboo-2.4.0.2-dba-win32\bin\eneboo.exe")
     * Arrancar el programa (eneboo) desde el explorador de archivos en la carpeta donde se ha descargado el programa.       
     * Aparecerá la pantalla _Conectar_.

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-01.jpg)

1. Rellenar los campos con los siguientes valores:
    * Base de datos: (nombre empresa)
    * Usuario: postgres (o el que hemos puesto como administrador de la base de datos PostgreSQL-ver phpMyAdminIII).
    * Contraseña: (la del administrador de la base de datos PostgreSQL-ver pgAdminIII).
1. Pulsar el botón de la flecha hacia la derecha _Más opciones_.

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-02.jpg)        

1. Rellenar los campos de esta pantalla con los siguientes valores: 
    * Controlador: POSTGRESQL
    * Servidor: localhost
    * Puerto: 5432

1. Pulsar el botón _Conectar_. Se mostrará un mensaje con el texto _La base de datos standard no existe ¿Quiere crearla?_. Pulsar _Sí_.

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-03.jpg)

1. Una vez iniciado el programa Eneboo se mostrará el entorno Eneboo.

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-04.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-05.jpg)

---
####PASO 6.-DESCARGAR LOS “MÓDULOS” de eneboo...

* Los más recomendados, porque están más actualizados:

1. Clonar el github: https://github.com/eneboo/eneboo-modules  con este manual: https://github.com/Miguel-J/eneboo/wiki/GITHUB-COMO-INSTALARLO-Y-USARLO
1. [Bajar en un zip los Repos oficiales del github de Eneboo](https://github.com/eneboo/eneboo-modules/archive/master.zip).
1. [Bajar en un zip los Repos del github de KLO-MANOLO](https://github.com/klo-manolo/eneboo-modules/archive/master.zip).


![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-01.jpg)

* OTROS: Se pueden descargar de varios sitios o "repositorios", hay unos que llevan más "extensiones" añadidas a la "mezcla básica" que otros...:

* http://www.eneboo.org/site/node/16

1. Descargar el [paquete de Eneboo Standard](http://www.eneboo.com/pub/contrib/standard-modules/standard.eneboopkg). (ESTE MEJOR NO, PORQUE ESTÁ DES-ACTUALIZADO).
1. “Si desea descargar la última versión de nuestros módulos oficiales en ZIP, haga clic en el siguiente enlace: https://github.com/gestiweb/eneboo-modules/zipball/master “ (8 megas) (ESTE MEJOR NO, PORQUE ESTÁ DES-ACTUALIZADO)
1.  “todos los módulos de gestiweb” descargar en zip  (ESTE MEJOR NO, PORQUE ESTÁ DES-ACTUALIZADO, DESCOMPRIME TODOS LOS MODULOS EN UNA CARPETA Y LUEGO SE INSTALAN DESDE EL PROGRAMA ENEBOO):

---
####PASO 7.-INSTALAR LOS MÓDULOS DE ENEBOO:

* (hay 3 opciones):

* OPCIÓN A) todos de golpe en "CARPETA DE MÓDULOS" (LA OPCIÓN MÁS RÁPIDA)

     * Ir a: Menú - Sistema - Cargar directorio de módulos y elegir lo descargado del GITHUB ENEBOO o KLO-MANOLO.

     * “modulos estandar de eneboo” descargar en zip: eneboo_standard.zip (3 megas)o (ESTE NO ES BUENO, DESCOMPRIME SOLO LOS MODULOS DEL AREA DE CONTABILIDAD Y FACTURACION  EN UNA CARPETA Y LUEGO SE INSTALAN DESDE EL PROGRAMA ENEBOO):


* OPCIÓN B) De uno en uno o "MÓDULO A MÓDULO":

     * hay que ir a la carpeta dende están y 
      * “todos los módulos de gestiweb” descargar en zip  (ESTE ESTÁ DES-ASCTUALIZADO, MEJOR NO USAR, DESCOMPRIME TODOS LOS MODULOS EN UNA CARPETA Y LUEGO SE INSTALAN UNO A UNO DESDE EL PROGRAMA ENEBOO):

* OPCIÓN C) todos de golpe en "PAQUETE": (ESTO DA MUCHOS ERRORES, MEJOR INSTALAR LOS MODULOS UNO A UNO o por CARPETAS-DIRECTORIO): 

      * “modulos estandar en paquete eneboo” o: **standard.eneboopkg**
      1. En el área de _Módulos_ de la parte izquierda, abrir la opción _Sistema -> Administración -> Cargar Paquete de módulos_.
      1. Localizar el archivo standard.eneboopkg y pulsar _Abrir_. Cuando finalice la carga, Eneboo Standard estará listo para empezar a trabajar.


![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-05.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-06.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-07.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-08.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-09.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-10.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-11.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-12.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-13.jpg)

* al acabar salir del programa Eneboo y volver a entrar.

* ...ir a “eneboo-sistema-administracion-regenerar la base de datos”...


---
####PASO 8.-REGENERAR LA BASE DE DATOS DESPUÉS DE CARGAR MÓDULOS:

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-13.jpg)
* ...entrar en “eneboo-sistema-administración-cargar Módulo”....e ir a la carpeta donde están guardados o descomprimidos del paso anterior...
* y después de cada uno:  ...ir a “eneboo-sistema-administración-”+mas”-principal-Regenerar la base de datos”..
...hay que “regenerar la base de datos” y salir del programa y volver a entrar después de haber instalado cada módulo......
         
