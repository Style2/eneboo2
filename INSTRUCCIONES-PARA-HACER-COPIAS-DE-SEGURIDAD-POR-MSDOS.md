
##1. AÑADIR UN PATH A WINDOWS PARA QUE ENCUENTRE EL PROGRAMA DE COPIAR:

* hace falta poner en el path de windows la ruta a mysql_dump.exe

1. en windows /panel-de-control /sistema /configuracion-avanzada-del-sistema
 /variables-de-entorno / path(en el listado de la ventana de abajo), esta el path.

1. hay que darle a EDITAR y decirle que añada al path (con un ";" al final) 
;c:\wamp\bin\mysql\mysql5.5.24\bin (cambiar por el NUMERO DE VERSION CORRECTO)

* en windows /sistema /variable de entorno , esta el path. 
hay que decirle que añada al path c:\wamm\apps\mysql\bin\mysql_dump.exe

1. una vez hecho se reinicia y listo, el equipo que tiene la BD ya puede hacer dumps

---------------------------------------------------------
##CREAR LA COPIA DE SEGURIDAD O el dump: (DESDE MS-DOS)

NOTA: Para acceder al MSDOS en Windows 8 ir a "INICIO"- "EJECUTAR" - "CMD" (usando www.classicshell.net)

El comando es:
mysqldump -hipdelservidor -uusuario -p nombre_bd > path_destino/nombre.sql

EJEMPLO:

C:\Documents and Settings\facturacion>mysqldump -h192.168.1.2 -uroot -p empresa > C:\dump_empresa_140423.sql
Enter password: ******


---------------------------------------------------------
##RECUPERAR COPIA DE SEGURIDAD GUARDADA:

(METEMOS LOS DATOS DESDE MS-DOS-----OJO! EN WINDOWS-8 HACERLO CON BOTON DERECHA MOUSE "EJECUTAR COMO ADMINISTRADOR")

**PRE-REQUISITOS: path incluido; wamp activado; 

mysql -h192.168.1.2 -root -p nombre_BD < path_destino/nombre.sql

****ejemplo:
C:\Documents and Settings\facturacion>mysql -h192.168.1.2 -uroot -p empresa
< c:\dumps\dump_empresa_140423.sql
Enter password: ******

****fin ejemplo


WINDOWS 8: (ejecutar como administrador)

C:\Windows\system32>mysql -uroot -p empresa < c:\dump_empresa_140718.sql
Enter password:

C:\Windows\system32>mysqldump -uroot -p empresa > c:\dump_empresa_140721.sql


###NOTA: PARA VERIFICAR QUE las copias se hacen bien:

 mirar que el fichero "pese", por ejemplo, de 30 megas !!
