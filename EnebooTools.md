* CREADO POR: [Comunidad Eneboo](http://www.eneboo.org) en https://github.com/eneboo/doc/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 13 de febrero de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/EnebooTools)

----
####Video Tutoriales de Eneboo-Tools
* https://www.youtube.com/watch?v=8f6LL8dRZ2s
* https://www.youtube.com/watch?v=tSWC-_fmM2w

####TUTORIALES
https://groups.google.com/forum/#!topic/eneboo/eVkmQNMUzGQ

Actualmente hay muy poca documentación. Lo mejor que existe (que yo recuerde ahora) está en el README de eneboo-tools.
Puedes verlo aquí: (al final de la página)

https://github.com/gestiweb/eneboo-tools




Recomiendo leerlo todo e intentar entender las herramientas en sí mismas. 




Lo que necesitas:

1. Tener instalado correctamente eneboo-tools en el sistema.

1. clonar el proyecto de eneboo-modules

1. clonar el proyecto de eneboo-features




El How-To del Eneboo Assembler creo que detalla bien los pasos para empezar.




Para entender un poco mejor las cosas, explico qué es (conceptualmente) eneboo-tools:




Eneboo Tools es un compendio de herramientas para ayudar al desarrollo de módulos y extensiones. Actualmente sólo tiene dos herramientas funcionales: **assembler y mergetool**. Normalmente verás que la gente usa Assembler.




* **Eneboo Assembler** es una herramienta de generación de mezclas de cero. Es decir, es un sistema automático que junta ciertos módulos con ciertas extensiones. Además permite la modificación fácil de las extensiones.




Internamente Assembler está usando Eneboo Mergetool para hacer el trabajo; así que, cualquier cosa que hace assembler automáticamente, la hace mergetool manualmente.




* **Eneboo Mergetool** es una herramienta de generación y aplicación de parches específicos; digamos que es una colección de heramientas diff y patch pero que son conocedoras de la sintaxis del fichero para el que están diseñadas. Esto permite sacar parches de unos cambios y aplicarlos en otro sitio sin apenas ningún conflicto.




Mergetool tiene cinco modos:
* file-diff
* file-patch
* folder-diff
* folder-patch
* y file-check.

1. **"Diff"** implica extraer unas diferencias y escribir un parche.
1. **"Patch"** significa leer un fichero de parche (de diferencias) y aplicarlas.
1. **"Check"** es realizar comprobaciones rutinarias.
1. Las acciones **"file"** trabajan con ficheros sueltos y **"folder"** con carpetas enteras (generalmente proyectos).




Mergetool a su vez tiene las acciones **"folder-*"** construidas a partir de las "file-*"; es decir, que es lo mismo aplicarlo a toda una carpeta, que ir manualmente fichero por fichero. Hay algo más que realizan las acciones "folder-*", pero es mínimo.




Las acciones **file-diff y file-patch** funcionan del siguiente modo: indicamos el tipo de fichero a tratar, y los dos ficheros a analizar, y el programa imprime por consola el resultado de la acción diff o patch (o al fichero indicado por --output-file).




Suena complicado, pero es muy sencillo. Solo hay que poner un par de ejemplos para que se vea.




En este momento existen 3 tipos de fichero posibles:
* qs
* qsdir. (qsdir es experimental (es para parchear ficheros qs), así que de momento lo dejo aparte.)
* y xml.






Imaginemos que tenemos un fichero flfactalma.qs con unos cambios agregando una nueva clase ivaIncluido. Necesitaremos el fichero original (al que llamamos $base o $previo) y el fichero modificado (que llamamos $final o $nuevo). Queremos generar un fichero de diferencias (parche) que llamaremos $parche (o también $patch)




Ejecutamos:

$ eneboo-mergetool file-diff qs \
    antiguo/facturacion/facturacion/scripts/flfactalma.qs \
    nuevo/facturacion/facturacion/scripts/flfactalma.qs \
    --output-file patches/flfactalma.qs

Esto nos generará "patches/flfactalma.qs" (y lo sobreescribe si ya existe). Este fichero contendrá la clase ivaIncluido o las clases que sean que se hayan agregado. 

Al aplicar este parche sobre otro fichero (file-patch), se le insertará al fichero las clases que vengan en el parche. 


Las acciones folder-* hacen lo mismo, pero con todos los ficheros del proyecto que han cambiado. Lanzan el tipo apropiado (qs o xml) y van escribiendo los parches en una carpeta. Para darle sentido a la carpeta se crea un fichero XML cuyo nombre coincide con el nombre de la carpeta (esto es un requisito importante) y es un listado de ficheros, rutas y tipo de parche generado. Esta misma carpeta se puede usar con folder-patch para que aplique todos los cambios de un golpe.


Hay que tener en cuenta que los ficheros qry, kut y mod no se parchean sino que se sobreescriben. Es posible que esto lo mejoremos en el futuro.

###esto lo meto aquí, de momento:



2º) Me leeré la documentación de las toos, aunque con lo que me acabas de enviar empiezo a entender cosas. En cuanto tenga instalada las tools y acceso al Git. Empezaré a practicar. hablas de ficheros qs, xml y qsdir (que no se que es lo que es). Pero y qué pasa con los forms, las querys y los informes? Me pones que se reescriben, eso que significa que no podré saber las diferencias? ¿De las tablas (.mtd) tampoco?





los "formatos" son eso, formatos. Hay muchas extensiones con el mismo formato. Y varios "formatos" para la misma extensión. 




Por ejemplo, QS y QSDir son para ficheros *.qs; lo único es que el segundo es más .... agresivo, llega más lejos extrayendo y aplicando cambios. El primero sólo pone y quita clases.




En el caso de los XML, prácticamente todos los otros ficheros son XML. Actualmente reconoce *.ui (formularios), *.mtd (tablas) y *.xml (acciones). Experimentalmente soporta *.kut (reports).




Pero en el caso de los folder-diff y folder-patch, las extensiones *.qry, *.kut directamente se sobreescribirán. 

El motivo de que se sobreescriban es que la herramienta original de InfoSial lo hacía así y mi objetivo inicial era conseguir el mismo resultado.


 


3º) Aunque ya se que es una tontería, cómo monto, por ejemplo en ubuntu Python (me imagino que de esto si habrá cosas en internet). Pero por si hay que hacer algo específico. Tampoco entiendo la instalación de las eneboo-tools.






Todo funciona con paquetes en Linux. Ubuntu tiene un instalador de paquetes, no sé si el synaptics. En ese programa buscas python y el resto de dependencias (nombres de paquete), le das a instalar y listo. Él se encarga de todo.




O para instalar desde consola sería: $ sudo apt-get install $paquete1 $paquete2 $paqueteN




... es indiferente si lo instalas por consola o por entorno gráfico, el resultado es idéntico.


En fin, para más detalle, hay que leerse el README, probar mucho y preguntar.
