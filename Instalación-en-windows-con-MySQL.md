* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 26 de febrero de 2016
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Instalaci%C3%B3n-en-windows-con-MySQL)

----

INSTALACION ENEBOO CON MYSQL:
-----------------------------

**NOTA - ATENCIÓN - PAGINA EN REVISIÓN : RECOMIENDO INSTALAR EL WAMP 2.2 QUE LLEVA MySQL 5.5 EN VERSIÓN 32 bits (incluso si tu ordenador es de 64 bits), TANTO PARA WINDOWS XP, VISTA, 7, 8, 8.1 como 10. ES EL ÚNICO QUE PERMITE TRABAJAR EN INNODB (imprescindible para hacerlo compatible con Facturascripts). El motivo es que todos los motores de Eneboo, a dia de hoy (octubre-2015) se compilan con librerías MySQL 5.5 y no "soporta" las que llevan 5.6...**


![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-20-error.jpg)

---
###PASO 1.-DESCARGAR e instalar el SERVIDOR DE BASE DE DATOS WAMP (incluye APACHE, MYSQL Y PHPMYADMIN..) de:
www.wampserver.com\en

![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-01.jpg)

--
#####PASO 1- OPCIÓN A- INSTALACIÓN EN WINDOWS 7 o 8 o 8.1 o 10: 

* **NOTA: a no ser que vayas a trabajar con motor MyISAM (o no-INNODB), lo mejor es seguir las instrucciones de abajo para Windows XP con wamp 2.2 para 32 bits, AUNQUE TU ORDENADOR SEA DE 64 BITS**.

* Si el ordenador es de **estructura 64 bits**, instalar la versión 2.5 para 64 bits (ver flecha roja en imagen) con:
     * apache 2.4.9
     * mysql  5.6.17 (ES MEJOR LA DE 5.5.24)
     * php 5.5.12
     * phpMyAdmin 4.1.14
     * sqlbuddy 1.3.3
     * xdebug 2.2.5
* Si el ordenador es de **estructura 32 bits**, instalar la versión 2.5 para 32 bits (ver flecha roja en imagen)

* **A CONTINUACIÓN SALTARSE LOS PASOS DE LA OPCIÓN B: PARA WINDOWS XP**

--
#####PASO 1- OPCIÓN B- INSTALACIÓN EN WINDOWS XP:

* En esta es la  2.2e con mysql 5.5.24 de 32 bits ....la 2.5 NO porque daba error en el mySQL superior al 5.5....

![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-02.jpg)
![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-03.jpg)
![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-04.jpg)
![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-05.jpg)
![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-06.jpg)
![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-07.jpg)
![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-08.jpg)
![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-09.jpg)

---
#### A PARTIR DE AQUI ES IGUAL TANTO PARA LA OPCIÓN DE WINDOWS XP COMO PARA LA DE WINDOWS 8 (en 32 O en 64 bits):

![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-10.jpg)
![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-11.jpg)
![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-12.jpg)
![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-13.jpg)
![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-14.jpg)

* ...(si pide instalar el “Visual c++ 2010 x86 ver.32 bits....pues se instala...)
* ...te pide el explorador de internet predeterminado...enter
* ….te pide el server....”localhost”....y el email para configuar el PHP...dejo “you@yourdomain”

* **NOTA: CÓMO SABEMOS QUE FUNCIONA?: PORQUE ABAJO-A LA DERECHA (AL LADO DEL RELOJ) HAY UNA "W" DE COLOR VERDE** (si está amarilla o roja es que algo va mal...)

---
####PASO 2.- AÑADIR USUARIOS.  (PASO NO-OPCIONAL...hay que hacerlo para el servidor % y para localhost)

* NOTA 1: Este paso no es imprescindible si sólo se trabaja con un ordenador y NO está conectado a internet, porque el programa ya crea el usuario "root" sin contraseña, pero es recomendable usar otro usuario y AÑADIR UNA CONTRASEÑA A ROOT...para evitar hackers...

* NOTA 2: En Windows 10 hay que modificar el httconf de Apache y el phpmyadmin.con del directorio /alias para añadir "Allow from ::1" (porque Windows 10 no reconoce como localhost el 121.0.0.1 al usar IP6)

* Ejecutar PHPMYADMIN con botón izquierdo en la W VERDE.... 

![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-16.jpg)

* **AÑADIR el o los usuarios que se quieran**:

     * Poner un nombre, ejemplo: ”usuario” (u otra) 
     * servidor: ”%”, 
     * contraseña “usuario”, (u otra)
     * y “marcar todos”, resto igual...
     * PULSAR: ”**añadir usuario**”.

* repetirlo para servidor= localhost

* **NOTA: PARA UN SOLO ORDENADOR NO HACE FALTA TOCAR NADA MÁS: ni apache, ni MySQL, ni PHP....dejar el wamp como está.**

![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-17.jpg)
![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-18.jpg)
![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-19.jpg)
![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-19b.jpg)
![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-19c.jpg)
![servidor wampserver](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-MySQL-WAMPSERVER/eneboo-MySQL-WAMPSERVER-19d.jpg)

---
####PASO 3.- CREAR UNA BASE DE DATOS. (PASO OPCIONAL)

* no es imprescindible este paso porque Eneboo lo crea la primera vez que se conecta a la base de datos....
* (ESTO PARA PRIMERA INSTALACION, SI ES RE-INSTALAR HAY QUE SALTARSE ESTE PASO & INSTALAR EL DUMP-COPIA DE SEGURIDAD)
* ir a phpMyAdmin
* ...lo hace en: C:\wamp\bin\mysql\mysql5.5.24\data \prueba 
* ….cotejamiento por defecto: “utf8_general_ci”


---
####PASO 4.-DESCARGAR EL PROGRAMA ENEBOO:

* Bajarlo de:
     * A) en http://eneboo.org/pub/contrib/ 
              (últimas versiones-releases...no uses el 2.4.0.2, está obsoleto, usa el 2.4.5.1 rc8 o el rc7:)
     * B) en www.eneboo.org (el que incluye postgre, sql u otro). Ir a “descargas”......”versiones estables”.....abajo....Hay dos opciones:
          * B.1)...en el PRIMER ORDENADOR DE LA RED o “servidor”.....elegir la **version “DBA”**.
                 * sirve para instalar módulos personalizados y otras tareas de "Administrador" 
          * B.2)...en los SIGUIENTES “ordenadores-clientes”.....elegir la **versión “QUICK”**.
                 * sirve para ordenadores donde NO QUIERES que estropeen/instalen NADA y evita problemas.

* (nota: la primera vez que lo descargué dio error en instalacion....eso es porque no se bajaron los 11,5 Mb...volverlo a descargar...)

---
####PASO 5.-ARRANCAR EL PROGRAMA ENEBOO:

* ejecutar el archivo **eneboo.exe** del subdirectorio **bin**. Por ejemplo:("C:\eneboo-2.4.5.1-rc8-dba-win64\bin\eneboo.exe")
* **(OJO: primero tiene que funcionar WAMPSERVER como servidor...QUE LA "W" AL LADO DEL RELOJ ESTÉ DE COLOR VERDE...SI ESTÁ ROJA O AMARILLA NO FUNCIONARÁ)** 

* Aparecerá la pantalla _Conectar_.

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-01.jpg)


* y cambiar la conexión:
     * Nombre: igual que el dado a la BD de phpMyAdmin: 
     * Usuario: root (o el que hemos puesto en phpMyAdmin...)
     * Contraseña:
(Por ejemplo, desde la página de inicio de phpMyAdmin seleccione Privilegios y agregue la contraseña a root@localhost. Deberá escribir la misma contraseña en config.inc.php de phpMyAdmin.)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-02.jpg)
* Darle a la flecha de la derecha y completar:
     * Base de datos: ...para poder poner MySQL(o INNODB) hay que tener el 5.5 (puedes usar MySQL_NO_INNODB si usas mysql 5.6 pero NO lo recomiendo porque da muchos errores con los módulos y en contabilidad...)
     * servidor: 127.0.0.1 (antes se llamaba “localhost”).....o aquí pondriamos el TCP_IP del ordenador que tiene la BD... 
     * puerto: el que da eneboo....3306

* Pulsar el botón **"CONECTAR"** y si esa base de datos no existe, te pregunta si quieres crearla...SI.

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-03.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-04.jpg)

* ...y aparece el entorno Eneboo (pero no puede hacer nada hasta que se carguen los módulos...):
![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-05.jpg)

---
####PASO 6.-DESCARGAR LOS “MÓDULOS” de eneboo...

* Se pueden descargar de varios sitios o "repositorios", hay unos que llevan más "extensiones" añadidas a la "mezcla básica" que otros...recomiendo las extensiones del github de KLO y los módulos del github "oficial" de ENEBOO...

* Ejemplos:

1. Agosto 2015- el mas recomendado: [paquete de Eneboo Standard julio-2015](http://eneboo.org/pub/contrib/2.4.5.1-rc7/).
1. Descargar el [paquete de Eneboo Standard](http://www.eneboo.com/pub/contrib/standard-modules/standard.eneboopkg).
1. Otro lugar de descarga: [Repos del git de KLO-MANOLO](https://github.com/klo-manolo/eneboo-modules/archive/master.zip).


---
####PASO 7.-INSTALAR LOS MÓDULOS DE ENEBOO:

* (hay 3 opciones):

* **OPCIÓN A) todos de golpe en "PAQUETE"**: 

* NOTA: **a fecha de hoy, octubre de 2015, esta es la mejor opción si empiezas de cero**: lo mejor es que uses el paquete: **prj0001-standard-2015_06_25.eneboopkg** de:

http://eneboo.org/pub/contrib/2.4.5.1-rc7/

...porque incluye ya las principales extensiones, que a los módulos oficiales deberás añadir....y no es fácil para un novato...por ejemplo el jasper-report, SEPA, renumeración de asientos, recibos de proveedores, etc...


      * “modulos estandar en paquete eneboo” o: **standard.eneboopkg**
      1. En el área de _Módulos_ de la parte izquierda, abrir la opción _Sistema -> Administración -> Cargar Paquete de módulos_.
      1. Localizar el archivo standard.eneboopkg y pulsar _Abrir_. Cuando finalice la carga, Eneboo Standard estará listo para empezar a trabajar.
      1. A mi me dio ERROR (con MySQL 5.6, NO da error con MySQL 5.5):
          * ...entrar en “eneboo-sistema-administracion-cargar paquete de modulos”....e ir a la carpeta donde estan guardados...darle al enter en el listado...esperar....mucho...salen errores...
          * ...“flfiles:Módulo : El valor flcontmode no existe en la tabla flmodules “...

* **OPCIÓN B) todos de golpe en "CARPETA DE MÓDULOS"**:

     * “modulos estandar de eneboo” descargar en zip: eneboo_standard.zip (3 megas)o (ESTE ES BUENO, DESCOMPRIME SOLO LOS MODULOS DEL AREA DE CONTABILIDAD Y FACTURACION  EN UNA CARPETA Y LUEGO SE INSTALAN DESDE EL PROGRAMA ENEBOO):


* **OPCIÓN C) De uno en uno o "MÓDULO A MÓDULO"**:

      * ojo!: en el caso de usar MySQL 5.6, no cambiar los archivos NO-INNODB:
          * **...”existen tablas que no usan el sistema INNODB...quiere convertirlas?”...NO**
      * “todos los módulos de gestiweb” descargar en zip  (ESTE ES MEJOR, DESCOMPRIME TODOS LOS MODULOS EN UNA CARPETA Y LUEGO SE INSTALAN UNO A UNO DESDE EL PROGRAMA ENEBOO):
      * “Si desea descargar la última versión de nuestros módulos oficiales en ZIP, haga clic en el siguiente enlace: https://github.com/gestiweb/eneboo-modules/zipball/master “ (8 megas) (es mejor usar los módulos del "oficial", están más actualizados: https://github.com/eneboo/eneboo-modules )

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-05.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-06.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-07.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-08.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-09.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-10.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-11.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-12.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-13.jpg)

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-14.jpg)

* PARA RENOVAR LA CACHÉ: al acabar salir del programa Eneboo y volver a entrar.

* OPCIONAL:...ir a “eneboo-sistema-administracion-regenerar la base de datos”...(es bueno cuando hay cambios de DATOS, la primera vez que se instala no es imprescindible...)

---
####PASO 8.-REGENERAR LA BASE DE DATOS DESPUÉS DE CARGAR MÓDULOS:

* ...entrar en “eneboo-sistema-administración-cargar Módulo”....e ir a la carpeta donde están guardados o descomprimidos del paso anterior...
* y después de cada uno:  ...ir a “eneboo-sistema-administración-”+mas”-principal-Regenerar la base de datos”..
...hay que “regenerar la base de datos” y salir del programa y volver a entrar después de haber instalado cada módulo......

![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-20.jpg)
![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-21.jpg)
![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-22.jpg)
![Pantalla de conexión](https://github.com/Miguel-J/eneboo/blob/master/imagen/ENEBOO-manual-instalacion-imagenes/ENEBOO-manual-instalacion-imagenes-23.jpg)
---
###PASO EXTRA-Aclaración...por qué yo elegí MySQL?

* RESUMEN: Por
1. simplicidad de uso del servidor
1. compatibilidad con los servidores externos del mercado
1. compatibilidad con otros programas (FacturaScripts, Prestashop, etc)


https://groups.google.com/forum/#!searchin/eneboo/mysql/eneboo/jNP7-5Ysz5g/S_NzOAW6F8gJ

* 17-nov-2013: 
     * Miguel-J: "Tengo prestashop con mysql, y como ya me suena un poco phpmyadmin, preferiría instalar eneboo con mysql en vez de postgreSql" 
     * NOTA 1: (...más adelante cambiaría phpmyadmin por Heidi, mucho mejor gestor, consejo de JMarco )
     * NOTA 2: Prestashop: Trabaja como MyISAM   ....??
* 21-nov-2013:
     * Miguel-J: "He seguido el consejo e instalando módulo a módulo es más fácil y no da problemas.
     * ...he pasado del easyPHP y ahora uso el WAMPserver, y parece que va mejor, pero lo único raro es que me dice Eneboo que mi MySQL no acepta INNODB, cuando si miro en configuración lo tiene puesto como "default"..es la versión :
          * Apache:  2.4.4
          * MySQL: 5.6.12
          * PHP: 5.4.16"
     * **NOTA: SIEMPRE QUE AL CARGAR MÓDULOS PREGUNTE SI QUIERE CONVERTIR LAS TABLAS NO-INNODB, CONTESTAR QUE NO, PORQUE SIEMPRE SE BLOQUEA** (y no se por qué)

* 25-junio-2014: https://groups.google.com/forum/#!searchin/eneboo/mysql/eneboo/Xcmq_S2VRz0/xw-khiaDeyQJ
     * Miguel-J: "He vuelto a probar el paquete estandar y con windows y mysql no se carga bien...."
     * JMarco: "Mi consejo es trabajar con MySQL 5.5. (WAMP3),(...) con la versión 5.6 no va muy fino."
     * AullaSistemas: "Version del servidor: 5.6.17 ... Ya hemos comentado que en mysql 5.6 contabilidad falla porque el tamaño mediumtext es mas pequeño que en la version 5.5, y hay un fichero .ui que excede ese tamaño nuevo. Por favor usa un mysql 5.5.x ."
     * AullaSistemas: "dentro de my.conf hay que cambiar el valor
          * `max_allowed_packet = 1M`
          * por:
          * `max_allowed_packet = 2M` (pero podria ser por 8 o 16)
          * ...en cambio, en linux sale: (ubuntu) max_allowed_packet = 16M
          * Por favor confirmen que el fichero contabilidad/modelos/form/co_modelo390.ui de 1.4Mb +- produce error en la primera situación (windows) y no en la segunda (linux). Si alguien prueba en un mysql 5.6 sería de agradecer..."