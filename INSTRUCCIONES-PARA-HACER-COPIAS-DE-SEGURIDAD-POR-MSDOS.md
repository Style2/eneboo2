* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 29 de febrero de 2016
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/INSTRUCCIONES-PARA-HACER-COPIAS-DE-SEGURIDAD-POR-MSDOS)

----
##1. AÑADIR UN PATH A WINDOWS PARA QUE ENCUENTRE EL PROGRAMA DE COPIAR:

#### **A) PARA MySQL:**

* hace falta poner en el path de windows la ruta a mysql_dump.exe

1. en windows /panel-de-control /sistema /configuracion-avanzada-del-sistema
 /variables-de-entorno / path(en el listado de la ventana de abajo), esta el path.

1. hay que darle a EDITAR y decirle que añada al path (con un ";" al final) 
;c:\wamp\bin\mysql\mysql5.5.24\bin (cambiar por el NUMERO DE VERSION CORRECTO)

     * que es el directorio donde esta el archivo: "mysql_dump.exe" (si no es ese directorio, buscarlo por el explorador de archivos...)

1. una vez hecho se reinicia y listo, el equipo que tiene la BD ya puede hacer dumps

--

#### **B) PARA PostgreSQL:**

* hace falta poner en el path de windows la ruta a pg_dump.exe

1. en windows /panel-de-control /sistema /configuracion-avanzada-del-sistema
 /variables-de-entorno / path(en el listado de la ventana de abajo), esta el path.

1. hay que darle a EDITAR y decirle que añada al path (con un ";" al final) 
;C:\Program Files\PostgreSQL\9.4\bin(cambiar por el NUMERO DE VERSION CORRECTO)

     * que es el directorio donde esta el archivo: "pg_dump.exe" (si no es ese directorio, buscarlo por el explorador de archivos...)

1. una vez hecho se reinicia y listo, el equipo que tiene la BD ya puede hacer dumps

----
##2. PARA MYSQL: CAMBIAR EL MAX PACKET EN my.cnf

+ para evitar el error: `ERROR 2006 (HY000): MySQL server has gone away`

+ ir a la carpeta: c:\wamp\bin\mysql\mysql5.5.24

+ dentro de my.conf (en Windows 10 CAMBIARLOS TODOS los que empiezan por "my") hay que cambiar el valor:
 
     * max_allowed_packet = 1M 
     * por:
     * max_allowed_packet = 2M  (mejor poner algo como 500M)

---------------------------------------------------------
##3. CREAR LA COPIA DE SEGURIDAD O el dump: (DESDE MS-DOS)

NOTA: Para acceder al MSDOS en Windows 8/10 ir a "INICIO"- "EJECUTAR" - "CMD" (usando www.classicshell.net) o "INICIO"- "PROGRAMAS" - "SISTEMA DE WINDOWS" - "SÍMBOLO DEL SISTEMA" (botón derecho mouse: "ejecutar como administrador")

#### **A) PARA MySQL:**

El comando es:
     mysqldump -hipdelservidor -uusuario -p nombre_bd > path_destino/nombre.sql

EJEMPLO:

     C:\Documents and Settings\facturacion>mysqldump -h192.168.1.2 -uroot -p empresa > C:\dump_empresa_140423.sql
     Enter password: ******


#### **B) PARA PostgreSQL:**

El comando es:
     pgdump -hipdelservidor -uusuario -p nombre_bd > path_destino/nombre.sql

EJEMPLO:

     C:\Documents and Settings\facturacion>pgdump -h192.168.1.2 -uroot -p empresa > C:\dump_empresa_140423.sql
     Enter password: ******

---------------------------------------------------------
##RECUPERAR COPIA DE SEGURIDAD GUARDADA:

(METEMOS LOS DATOS DESDE MS-DOS-----OJO! EN WINDOWS-8 HACERLO CON BOTON DERECHA MOUSE "EJECUTAR COMO ADMINISTRADOR")

**PRE-REQUISITOS: path incluido; wamp activado; 

mysql -h192.168.1.2 -root -p nombre_BD < path_destino/nombre.sql

****ejemplo:

     C:\Documents and Settings\facturacion>mysql -h192.168.1.2 -uroot -p empresa < c:\dumps\dump_empresa_140423.sql
     Enter password: ******

****fin ejemplo


WINDOWS 8: (ejecutar como administrador)

     C:\Windows\system32>mysql -uroot -p empresa < c:\dump_empresa_140718.sql
     Enter password:

     C:\Windows\system32>mysqldump -uroot -p empresa > c:\dump_empresa_140721.sql


###NOTA: PARA VERIFICAR QUE las copias se hacen bien:

 mirar que el fichero "pese", por ejemplo, de 30 megas !!

