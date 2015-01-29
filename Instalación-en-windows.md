INSTALACION ENEBOO CON MYSQL:
-----------------------------

###1.-Descargar e instalar WAMP (incluye APACHE, MYSQL Y PHPMYADMIN..) de:
www.wampserver.com\en

1.a-INSTALACION EN WINDOWS 7 o 8: instalo la 2.5 para 64 bits con:
apache 2.4.9
mysql  5.6.17
php 5.5.12
phpMyAdmin 4.1.14
sqlbuddy 1.3.3
xdebug 2.2.5


1.b- INSTALACION EN WINDOWS XP: En esta es la  2.2e de 32 bits ....la 2.5 NO porque daba error en el mySQL superior al 5.5....

...(pide instalar el “Visual c++ 2010 x86 ver.32 bits....pues lo instalo...)....despues vuelvo y te lleva al sourgeforge
apache 2.2.22
mysql  5.5.12
php      5.4.16
phpMyAdmin 4.0.4
sqlbuddy 1.3.3
xdebug 2.2.3

...te pide el explorador de internet predeterminado...enter
….te pide el server....”localhost”....y el email para configuar el PHP...dejo “you@yourdomain”


***otra opcion: (se instaló mal...)1.-Descargar e instalar easyphp en www.easyphp.org: incluye APACHE, EASYPHP Y PHPMYADMIN..Ejecutarlo (doble click en la “e” junto al reloj)....si da problemas con apache le das otra vez a conectar y en paz.2.- Ejecutar “Administracion” (boton derecha mouse en la “e”)...y allí “php myadmin”



####2.- Ejecutar PHPMYADMIN con botón izquierdo en la W VERDE....
***Solo AÑADIR los usuarios:
2.a.-”usuario”, para servidor:”%”, contraseña “usuario”, y “marcar todos”, resto igual...”añadir usuario”.


****NOTA: PARA UN SOLO ORDENADOR NO HACE FALTA TOCAR NADA MÁS: ni apache, ni MySQL, ni PHP....dejar el wamp como está.*******************


####3.- Crear una base de datos en myAdmin. “prueba"
 (ESTO PARA PRIMERA INSTALACION, SI ES RE-INSTALAR HAY QUE SALTARSE ESTE PASO & INSTALAR EL DUMP-COPIA DE SEGURIDAD)
...lo hace en: C:\wamp\bin\mysql\mysql5.6.12\data \prueba
….cotejamiento por defecto: “utf8_general_ci”


####4.-Instalar eneboo en www.eneboo.org (el que incluye postgre sql u otro). 

Ir a “descargas”......”versiones estables”.....abajo....Hay dos opciones:

A)...en el “servidor” la version “DBA”...para instalar módulos personalizados.
B)…en los “clientes” la versión “QUICK”...que evita problemas.

VERSION DBA:
Build dbAdmin Windows 32bits
http://www.eneboo.org/pub/eneboo/builds/v2.4.0/eneboo-v2.4.0.2-dba-win32-installer.exe


(nota: la primera vez que lo descargué dio error en instalacion....eso es porque no se bajaron los 11,5 Mb...volverlo a descargar...)
(nota2....cuando instalé la dbadmin 2.4.2 dio muchos errores:
http://eneboo.org/pub/eneboo/builds/v2.4.2/eneboo-2.4.2.2-dba-win32.tar.bz2
….ojo....esta version mejor no instalarla....)


####5.-Arrancar eneboo:
 ("C:\eneboo-2.4.0.2-dba-win32\bin\eneboo.exe") (OJO: primero tiene que funcionar WAMPSERVER como servidor...) y cambiar la conexión:
Nombre: igual que el dado a la BD de phpMyAdmin: 
Usuario: usuario (lo da  phpMyAdmin)
Contraseña:
(Por ejemplo, desde la página de inicio de phpMyAdmin seleccione Privilegios y agregue la contraseña a root@localhost. Deberá escribir la misma contraseña en config.inc.php de phpMyAdmin.)
Base de datos: MySQL_NO_INNODB
servidor: 127.0.0.1 (antes se llamaba “localhost”).....o aquí pondriamos el TCP_IP del ordenador que tiene la BD... 

puerto: el que da eneboo....3306


####6.-Instalar los “módulos” de eneboo...
http://www.eneboo.org/site/node/16
...descargar el: (hay 3 opciones):

A) todos de golpe (ESTO DA MUCHOS ERRORES, MEJOR INSTALAR LOS MODULOS UNO A UNO): “modulos estandar en paquete eneboo”o: standard.eneboopkg

“gestiweb-eneboo-modules-aea6681” (ESTO DA MUCHOS ERRORES, MEJOR INSTALAR LOS MODULOS UNO A UNO)
...entrar en “eneboo-sistema-administracion-cargar paquete de modulos”....e ir a la carpeta donde estan guardados...darle al enter en el listado...esperar....mucho...salen errores...
...“flfiles:Módulo : El valor flcontmode no existe en la tabla flmodules “...
...”existen tablas que no usan el sistema INNODB...quiere convertirlas?”...NO
...ir a “eneboo-sistema-administracion-regenerar la base de datos”...


B) “modulos estandar de eneboo” descargar en zip: eneboo_standard.zip (3 megas)o (ESTE ES BUENO, DESCOMPRIME SOLO LOS MODULOS DEL AREA DE CONTABILIDAD Y FACTURACION  EN UNA CARPETA Y LUEGO SE INSTALAN DESDE EL PROGRAMA ENEBOO):


C) “todos los modulos de gestiweb” descargar en zip  (ESTE ES MEJOR, DESCOMPRIME TODOS LOS MODULOS EN UNA CARPETA Y LUEGO SE INSTALAN DESDE EL PROGRAMA ENEBOO):
“Si desea descargar la última versión de nuestros módulos oficiales en ZIP, haga clic en el siguiente enlace: https://github.com/gestiweb/eneboo-modules/zipball/master “ (8 megas)


.

####CARGAR MODULOS:
...entrar en “eneboo-sistema-administracion-cargar Módulo”....e ir a la carpeta donde estan guardados o descomprimidos del paso anterior...
y después de cada uno:  ...ir a “eneboo-sistema-administracion-”+mas”-principal-Regenerar la base de datos”..
...hay que “regenerar la base de datos” y salir del programa y volver a entrar despues de haber instalado cada módulo......
