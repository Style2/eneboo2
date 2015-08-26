* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 26 de agosto de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Dise%C3%B1os-de-Impresi%C3%B3n-e-informes%3A-Instalar-el-enlace-a-Jasper-Reports)

----
###MANUAL DE Diseños de Impresión e informes: Instalar el enlace a Jasper Reports


####PASO 1.- INSTALAR JAVA

####PASO 2.- CREAR LOS DIRECTORIOS:

1.- dentro del directorio de "eneboo....rc7" hay que crear el directorio "reports"...entre el de "plugins" y "share"...

1.- y dentro de "reports" otro directorio CON EL MISMO NOMBRE QUE EL NOMBRE DE LA BASE DE DATOS....

1.- ...y dentro de este "directorio-bd" otros tres:

* "reports"
* "subreports"
* "temp_files"

####PASO 3.- COPIAR EL EJECUTABLE .JAR Y LA CARPETA DE "LIBRERIAS":

1.- Pones el ejecutable "enebooreports.jar" DENTRO DE LA PRIMERA CARPETA "reports"...


1.- ...y las librerias en la carpeta-directorio "lib", DENTRO DE LA PRIMERA CARPETA "reports" (al mismo nivel que la carpeta con el nombre de la base de datos, NO dentro de ésta)

####PASO 4.- ENLAZAR CON JAVA Y LAS LIBRERIAS:

Y luego vas a menu eneboo-area facturacion-informes-datos generales

..luego pestaña al lado: "jasper plugin" y le das a "..."

y ahora le do a los botones Java JRE y Conección a Librería eneboo reports

y buscas la PRIMERA carpeta "report" que has creado DENTRO del ejecutable de Eneboo

Aceptar
 
En el segundo campo, lo mismo: busca la misma carpeta.

Y activa el boton "compilar todos los reports"

Guardar

####PASO 5.- PROBAR QUE ENLAZA CON JAVA Y LAS LIBRERIAS:

Daarle al botón del "test"

####PASO 6.- CREAR LAS CARPETAS DE LOS INFORMES

Tienen que tener EL MISMO NOMBRE que el nombre que se le da en eneboo a su correspondiente ".kut"

(aqui poner cuadro equivalencias)

####PASO 7.- COLOCAR LOS ARCHIVOS .jrxml EN SU CARPETA-DIRECTORIO


---
### INSTALAR LAS EXTENSIONES JASPER A LA MEZCLA DE MÓDULOS DE ENEBOO 

https://groups.google.com/forum/#!topic/eneboo/MLislQP1BSw

Hola otra vez, 
he estado mirando todas las respuestas anteriores, y he descargado las eneboo-features, los eneboo-modules y he instalado las eneboo-tools. He parcheado las extensiones y he subido los módulos siguiendo estas instrucciones: 

"Extraer modulo flfactinfo de eneboo (SISTEMA->ADMINISTRACION->MODULOS->Doble clik sobre flfactinfo->Click en flecha verde(exportar ficheros)) 

renombrar "flfactinfo" a "informes"(nombre correcto) 

crear nueva carpeta "original" y dentro de ella otra con nombre "facturacion" e introducir "informes" en ella.(estructura de carpetas correcta) 

descargar ext9002 y ext1058 de github. 

ejecutar eneboo-merge folder-patch ext9002-jasper_plugin original parcheado9002 (parcheamos con la ext9002) 
ejecutar eneboo-merge folder-patch ext1058-jplugin_plus parcheado9002 final(parcheamos con ext1058 la version ya parcheada con ext9002) 
entramos en final y creamos un archivo COPYING 

En eneboo, importamos "final" (SISTEMA->ADMINISTRACION->MODULOS->Doble clik sobre flfactinfo->Click en flecha azul(Cargar ficheros)) " 

(Gracias a "Preguntas r" por el magnífico resumen, aunque el ejecutable es eneboo-mergetool, no eneboo-merge) 

Y ahí me he quedado. No me funcionan los informes, y en "facturación>informes>datos generales" no me sale la pestaña del jasperplugin. 
He intentado hacer "eneboo-assembler build jasper_plugin base" y me dice que: 
ERROR: Funcionalidad jasper_plugin desconocida 

¿y ahora qué hago? 

Muchísimas gracias a todos!