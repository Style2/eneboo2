####Video Tutoriales de Eneboo-Tools
* https://www.youtube.com/watch?v=8f6LL8dRZ2s
* https://www.youtube.com/watch?v=tSWC-_fmM2w

####TUTORIALES
https://groups.google.com/forum/#!topic/eneboo/eVkmQNMUzGQ

Actualmente hay muy poca documentación. Lo mejor que existe (que yo recuerde ahora) está en el README de eneboo-tools.
Puedes verlo aquí: (al final de la página)

https://github.com/gestiweb/eneboo-tools




Recomiendo leerlo todo y intentar entender las herramientas en sí mismas. 




Lo que necesitas:

- Tener instalado correctamente eneboo-tools en el sistema.

- clonar el proyecto de eneboo-modules

- clonar el proyecto de eneboo-features




El How-To del Eneboo Assembler creo que detalla bien los pasos para empezar.




Para entender un poco mejor las cosas, explico qué es (conceptualmente) eneboo-tools:




Eneboo Tools es un compendio de herramientas para ayudar al desarrollo de módulos y extensiones. Actualmente sólo tiene dos herramientas funcionales: assembler y mergetool. Normalmente verás que la gente usa Assembler.




Eneboo Assembler es una herramienta de generación de mezclas de cero. Es decir, es un sistema automático que junta ciertos módulos con ciertas extensiones. Además permite la modificación fácil de las extensiones.




Internamente Assembler está usando Eneboo Mergetool para hacer el trabajo; así que, cualquier cosa que hace assembler automáticamente, la hace mergetool manualmente.




Eneboo Mergetool es una herramienta de generación y aplicación de parches específicos; digamos que es una colección de heramientas diff y patch pero que son conocedoras de la sintaxis del fichero para el que están diseñadas. Esto permite sacar parches de unos cambios y aplicarlos en otro sitio sin apenas ningún conflicto.




Mergetool tiene cinco modos: file-diff, file-patch, folder-diff, folder-patch y file-check. "Diff" implica extraer unas diferencias y escribir un parche. "Patch" significa leer un fichero de parche (de diferencias) y aplicarlas. "Check" es realizar comprobaciones rutinarias. Las acciones "file" trabajan con ficheros sueltos y "folder" con carpetas enteras (generalmente proyectos).




Mergetool a su vez tiene las acciones "folder-*" construidas a partir de las "file-*"; es decir, que es lo mismo aplicarlo a toda una carpeta, que ir manualmente fichero por fichero. Hay algo más que realizan las acciones "folder-*", pero es mínimo.




Las acciones file-diff y file-patch funcionan del siguiente modo: indicamos el tipo de fichero a tratar, y los dos ficheros a analizar, y el programa imprime por consola el resultado de la acción diff o patch (o al fichero indicado por --output-file).




Suena complicado, pero es muy sencillo. Solo hay que poner un par de ejemplos para que se vea.




En este momento existen 3 tipos de fichero posibles: qs, qsdir y xml.

qsdir es experimental (es para parchear ficheros qs), así que de momento lo dejo aparte.




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

En fin, para más detalle, hay que leerse el README, probar mucho y preguntar.
