* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 25 de octubre de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/FACTURASCRIPTS---Instalaci%C3%B3n-y-configuraci%C3%B3n)

----


### INSTALACION DE FACTURASCRIPTS

### CONFIGURACIÓN DEL SERVIDOR PARA OPEN SSL

back-on-business....a mi me pasaba lo mismo: en wampserver tienes que:

A) ir a la W verde - botón izquierdo mouse - Apache - apache modules - bajar por la lista y activar el "ssl_module" 

Y ADEMÁS:

B) ir a la W verde - botón izquierdo mouse - PHP - PHP extensions - a mitad de la lista y activar el "php_openssl" 

...Y LUEGO  ir a la W verde - botón izquierdo mouse - "Restart all services"

...Y YA QUE ESTÁS, ACTIVA TAMBIÉN EL "CURL" EN:

C)  ir a la W verde - botón izquierdo mouse - PHP - PHP extensions - a mitad de la lista y activar el "php_curl" 

...Y LUEGO  ir a la W verde - botón izquierdo mouse - "Restart all services"

-----
## CORRECCION ERRORES CONOCIDOS:

### ( ! ) Fatal error: Maximum execution time of 30 seconds exceeded in ...

http://www.facturascripts.com/comm3/index.php?page=community_item&id=1528

SOLUCIÓN: en tu configuración de php.ini el maximum_execution_time deberias ampliarlo de 30 a 120 o algún valor que te permita mantener el proceso activo mas tiempo, no debes tocar código de FS para eso, solo es configuración en el lado del servidor.

--

###  hay un error en el ORDEN DE SINCRONIZACIÓN.

http://www.facturascripts.com/comm3/index.php?page=community_item&id=1531

 En la tabla "fs_var", el campo "ps_sync_step", se define el orden de la sincronización...
 ...he sacado estos pasos:

 0.- eliminar articulos
 1.- descargar pedidos
 2.- descargar categorías y descargar pedidos (AQUI ESTA EL ERROR, LO EXPLICO DEBAJO)
 3.- comprobar artículos
 4.- eliminar categorías antiguas
 5.- eliminar pedidos
 6.- eliminar categorías obsoletas
 7.- eliminar etiquetas obsoletas.

 ----

 El error es que yo trabajo OFF-LINE, y me conecto SÓLO para sincronizar: pues si borro una categoría en mi ordenador, cuando sincroniza NUNCA BORRA LA CATEGORIA, PORQUE PRIMERO ME LA TRAE DE PRESTASHOP en el punto 2, ANTES del punto 6

SOLUCIÓN: A dia de hoy no hay....gestionar las categorías desde Prestashop....

--

##  después de dar un error al pasar familias a categorías (solucionado por la cocina de phpmyadmin), el sincronizador dice que no continua hasta que solucione ese paso.

http://www.facturascripts.com/comm3/index.php?page=community_item&id=1527

 No consigo sacarlo de ahí. 
 Si desinstalo el plugin, al reinstalarlo recuerda la configuración anterior. 
 Si "desactivo" el sincronizador, lo único que consigo es "pausarlo", debería poder "re-iniciarlo".....

SOLUCIÓN: Eliminar la línea: fs_var.ps_familias2cats o darle un valor DISTINTO a "1"
