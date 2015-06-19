* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 19 de junio de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Personalizar-eneboo-con-las-extensiones)

----

##Personalizar eneboo con las extensiones:
-----------------------------

https://groups.google.com/forum/#!searchin/eneboo/jmarco/eneboo/gpsrwXpDBPQ/QM2b4S7HH1IJ

Hola. No se si te voy a aclarar algo o te voy a liar más de lo que estás:

Asumo varias cosas:

1) Tienes una rama personalizada.

2) estas personalizaciones , no las tienes estandarizadas (es decir, no usaste en su momento los módulos de eneboo-modules + la ext personalizada)., sino que es una rama anterior a eneboo.

3) Este mismo problema podría volver a producirse si le da al cliente por pedirte una nueva extensión.

Yo te recomiento una estrategia  de :

a) Estandarización.Facil de mantener bug y añadir extensiones en el futuro

b) Sintetizar extensión (modificaciones previas). Crear una extensión con solamente las modificaciones especificas de ese cliente.

c) Creación de un proyecto.Para manetener a ese clente facilmente.




Pasos a seguir:

a y b) Usa una de estas recetas para extraer en una extensión todas las modificaciones viejas(la v3 es ligeramente diferente).

Con esto vas a sacar las personalizaciones en una extensión y te permite usar los módulos eneboo-modules como base.

c) para crear el proyecto

eneboo-assembler new y a seguir instrucciones y recordar que cada vez que creamos algo hacer :

eneboo-assembler dbupdate


Un truco:

si al usar la receta, sabemos que extensiones hay ya aplicadas a nuestra rama , podemos añadirlas a la extensión como dependencias (extXXXX/conf/required_features). Al final del proceso , la extensión resultante = total  - (módulos oficiales + extensiones requeridas).

Saludos
