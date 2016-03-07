* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 25 de octubre de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Lenguajes-de-programaci%C3%B3n.-TABLES)

----

Lenguajes de programación. TABLES
-----------------------------


#####1. Extensión de archivos: .mtd

Se pueden abrir con "Wordpad".

#####1. Añadir un comentario:

`<!-- aquí escribes lo que quieras, para aclarar lo que hace ese código	-->`

#####1. Estructura básica:

     <!DOCTYPE TMD>
     <TMD>

Aquí se pone el nombre de la tabla:

	     <name>articulos</name>

Aquí se pone la explicación del nombre de la tabla:

	     <!-- Listado de artículos con todos los datos	-->

...y aquí el código-enlace que usaremos parra traducirlo:

	     <alias>QT_TRANSLATE_NOOP("MetaData","Articulos")</alias>

...ahora vienen los campos de esa tabla:

	     <field>
		     <name>referencia</name>
		     <!-- Código de referencia del artículo	-->
		     <alias>QT_TRANSLATE_NOOP("MetaData","Referencia")</alias>
		     <null>false</null>
		     <pk>true</pk>
		     <type>string</type>
		     <length>18</length>

...y luego van las "relaciones" de ese campo, por ejemplo "1M" aquí y "M1" en la .mtd de "articulosagen":

		     <relation>
			     <table>articulosagen</table>
			     <field>referencia</field>
			     <card>1M</card>
		     </relation>
	     </field>
     </TMD>

---

#####1. Tipos de "type"´s:

string=

