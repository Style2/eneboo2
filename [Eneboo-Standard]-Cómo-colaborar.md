* CREADO POR: [Comunidad Eneboo](http://www.eneboo.org) en https://github.com/eneboo/doc/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 7 de febrero de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/%5BEneboo-Standard%5D-C%C3%B3mo-colaborar)

----
Este manual lo han creado miembros de la [Comunidad Eneboo](http://www.eneboo.org). Si deseas completarlo, este capítulo te interesa. ¿Crees que no tienes suficientes conocimientos técnicos? No te preocupes, verás que es muy fácil. ¡Anímate a colaborar!

# Guía rápida de edición del wiki de GitHub
Como puedes ver, este manual está publicado en el wiki de GitHub. Es una herramienta sencilla, intuitiva y muy fácil de usar. En este apartado mostraremos cómo utilizar las opciones que se usan para la edición de este manual. Puedes encontrar un manual más completo [aquí](http://www.adictosaltrabajo.com/tutoriales/tutoriales.php?pagina=githubWiki), aunque esta documentación está algo desactualizada.

## Pídenos permiso
Si quieres colaborar con la edición necesitarás una cuenta de GitHub con permisos de edición sobre el wiki. Date de alta en GitHub y después solicita permisos de edición en el [foro de Eneboo](https://groups.google.com/forum/#!forum/eneboo).

## Crear o editar una página
Cada capítulo del manual se escribe en una página distinta. Con los botones _Edit Page_ o _New Page_ podemos respectivamente editar o crear una nueva página.

Siempre utilizaremos el modo de edición (_Edit mode_) _Markdown_, el que usa el wiki por defecto.

## La barra de botones de edición
Al crear o editar una página nos aparecerá una barra de botones de edición.
![Barra de botones de edición](https://raw.githubusercontent.com/eneboo/doc/master/images/standard/barra_botones_wiki.png)

Hay que aclarar que el editor del wiki no es del tipo [WYSIWYG](http://es.wikipedia.org/wiki/WYSIWYG). Por tanto, no veremos inmediatamente los cambios de formato que producen los botones, sino que al pulsarlos se introducirán unas marcas en el texto. Para ver cómo quedará finalmente la página debemos guardarla o pulsar el botón _Preview_ que podemos encontrar al final de ésta.

Los tres primeros botones (**_h1_**, **_h2_** y **_h3_**) sirven para indicar que un párrafo es un título. El nombre de una sección de un capítulo se marca con _h1_, con _h2_ el de una subsección y con _h3_ se marca el nombre de una subsección un nivel más abajo.

El botón de **_Link_** sirve para crear enlaces. Los tenemos de tres tipos:

1. Enlaces internos. Son los que hacemos dentro de la misma página, al título de una sección. Tienen la forma:
`[Texto del enlace](#titulo-seccion)`
1. Enlaces a otras páginas del wiki. Tienen la forma:
`[Texto del enlace]([Eneboo Standard] Nombre de la página)`
1. Enlaces externos (a otras páginas web que no pertenecen al wiki). Tienen la forma:
`[Texto del enlace](http://www.unapaginacualquiera.com/pagina)`

Las imágenes se insertan con el botón **_Image_**, que abre un diálogo que nos pide la URL de la imagen y un texto alternativo (que no se ve normalmente y que se utiliza para, por ejemplo, para mostrarlo cuando por alguna razón la imagen no se puede visualizar). Las imágenes se han de subir a la carpeta _images/standard/_ del repositorio _doc_. La URL que hemos de indicar tendrá la forma:
`https://raw.githubusercontent.com/eneboo/doc/master/images/standard/nombre_imagen.png`.

Podemos obtener esta URL navegando por GitHub hasta llegar a la imagen en el repositorio, pulsando el botón _Raw_ y copiando la URL que nos muestre el navegador.

El resto de las opciones de la barra de botones hacen lo que se espera de ellas y no merecen una explicación detallada. Se puede ver su funcionamiento simplemente probándolas.

# Convenciones usadas para este manual
Para conseguir que el manual, editado por muchos colaboradores, tenga una apariencia homogénea, seguiremos unas sencillas convenciones.

1. Los elementos propios de la aplicación, como nombres de campos o botones, deberán ir en cursiva para distinguirlos mejor. Durante la edición el texto se verá como se muestra en el siguiente ejemplo:
`Para crear una nueva factura pulse el botón *Insertar registro*.`
1. Los nombres de las páginas irán precedidos siempre por el texto `[Eneboo Standard]`. Esto se hace así para poder ver en el listado de páginas del wiki todas las que se refieren a un mismo tema de forma agrupada, ya que el wiki no muestra carpetas.

# El índice
En la parte superior derecha de cada página verás un índice que nos permite acceder directamente a cada una de ellas. Este índice no se genera de forma automática, sino que hay que editarlo.

Podemos hacerlo cuando pulsamos el botón _Edit Page_. Iremos al final de la página y pulsaremos en la flecha hacia abajo que hay junto _Sidebar_. Ahí podemos añadir o modificar los enlaces del índice como hemos explicado en la sección [La barra de botones de edición](#la-barra-de-botones-de-edici%C3%B3n) para el caso de enlaces a páginas del mismo wiki.

**Nota:** Cuando crees una página nueva verás que no aparece el índice. Esto es porque el wiki por defecto crea la página en el directorio raíz del repositorio del wiki, donde no le afecta el archivo _Sidebar.md que contiene el índice, ya que este archivo está en el directorio _standard_. Para que se muestre el índice debes hacer lo siguiente:

1. Bájate con _git_ el repositorio del wiki ejecutando `git clone https://github.com/eneboo/doc.wiki.git`.
1. Mueve la página al directorio _standard_ con `git mv \[Eneboo-Standard\]-Nombre-de-la-pagina.md standard/`.
1. Haz _commit_ y _push_.

Si tienes problemas para hacer esto coméntalo en el [foro](https://groups.google.com/forum/#!forum/eneboo), te echaremos una mano.
