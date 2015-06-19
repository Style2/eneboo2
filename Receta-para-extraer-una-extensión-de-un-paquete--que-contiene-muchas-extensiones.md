INCIDENCIA:

https://groups.google.com/forum/#!topic/eneboo/KTHQjW8ieR4

---
AULLA-MANUAL:

Receta para extraer una extensión de un paquete  que contiene muchas extensiones.

Pasos:

1 Creamos la estructura de la extensión:

Si se ejecuta sin argumentos, preguntará los datos mínimos para crear la plantilla:
$ eneboo-assembler new

Qué tipo de funcionalidad va a crear?
    ext) extensión
    prj) proyecto
    set) conjunto de extensiones
Seleccione una opción: ext

Código para la nueva funcionalidad: A002

Nombre corto de funcionalidad: mifun02

Descripción de la funcionalidad: Funcionalidad 02
Si se le pasa el nombre de la carpeta y la descripción, omite los pasos iniciales y pasa directamente al menú:
$ eneboo-assembler new extA003-mifun03 "Funcionalidad 03"
A la hora de elegir una opción en el menú, existe autocompletado con el tabulador. Si introducimos "flfact*" y pulsamos tabulador, pondrá todos los módulos que coincidan.
En el caso de las rutas, también existe autocompletado con el sistema de ficheros.
Por defecto las extensiones se crean en la primera carpeta de extensiones que haya en la configuración, se puede cambiar la carpeta de destino en una opción del menú.
Importante Aquí vamos a especificar como dependencias los módulos a los que afecta la extensión.




** Todo lo que se va a explicar a continuación ocurrirá dentro de la carpeta build de la extensión que se está creando.


2º Cogemos desde eneboo-modules una copia de los módulos afectados.

 $ eneboo-assembler build “nombre_corto_de_la_funcionalidad” base

3º Creamos una copia de base para poder trabajar en ella.
 
 $ eneboo-assembler build “nombre_corto_de_la_funcionalidad” src
 
4º Echamos nuestros modulos afectados con extensiones dentro de build/src y machacamos.

5º Sacamos todas las diferencias entre base y src machacado.

 $ eneboo-assembler build “nombre_corto_de_la_funcionalidad” fullpatch

6º Limpiamos la basura 

  Vamos eliminando lo que no sea de la extensión que queremos dentro de build/fullpatch. Aquí habrá de todas las extensiones que tenga el módulo afectado. Eliminamos la basura y modificamos el fullpatch.xml

7º Comprobamos que funciona

$ eneboo-assembler build “nombre_corto_de_la_funcionalidad” test-fullpatch

Esto genera en build/test-fullpatch un modulo que contiene la actualización , lo cargamos en eenboo y a probarla. Si falla volvemos a paso 6 hasta que funcione.

8º Sacamos la extensión en limpio y la guardamos.

Movemos el contenido a src y sacamos parche sobre módulos estandarizados

$ eneboo-assembler build “nombre_corto_de_la_funcionalidad” src-fullpatch 
$ eneboo-assembler build “nombre_corto_de_la_funcionalidad” fullpatch

 
Ahora nos ha salido la extensión limpia de polvo y paja.

$ eneboo-assembler save-fullpatch “nombre_corto_de_la_funcionalidad”

Esto generará dentro de la carpeta build/../patches/“nombre_corto_de_la_funcionalidad”/ nuestra extensión.

9º (Opcional) Regeneramos la BD para que eneboo-tool sepa como funciona.

$ eneboo-assembler dbupdate






Listo , borramos carpeta build. Y probamos que el parche funciona.

Si volviéramos a ejecutar los pasos 2 y 3 , en el 3 se añadiría automaticamente el parche.

