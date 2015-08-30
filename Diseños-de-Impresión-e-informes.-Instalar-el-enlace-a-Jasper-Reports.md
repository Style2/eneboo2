* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 26 de agosto de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Dise%C3%B1os-de-Impresi%C3%B3n-e-informes%3A-Instalar-el-enlace-a-Jasper-Reports)

----
https://groups.google.com/forum/#!topic/eneboo/RKXQm8QKkTg

Despues de estar peleando con los .kut y acabar el café de la maquina descubrí gracias a esta lista el ar2kut, los .ar mejoran algo pero sigue siendo muy limitado, asi que buscando buscando encuentro eneboo-reports, sin esta lista y la colaboración de todos vosotros seguramente habria desinstalado eneboo rapidamente pero por suerte aqui estamos.

---

###MANUAL DE Diseños de Impresión e informes: Instalar el enlace a Jasper Reports

PASO 0.- INSTALAR LAS EXTENSIONES +ext9002-jasper_plugin Y +ext1058-jplugin_plus EN EL MÓDULO "INFORMES" CON ENEBOO-TOOLS

Visitar:

https://github.com/Miguel-J/eneboo/wiki/eneboo-reports

####PASO 1.- INSTALAR JAVA

####PASO 2.- CREAR LOS DIRECTORIOS:

1.- dentro del directorio de "eneboo....rc7" hay que crear el directorio "reports"...entre el de "plugins" y "share"...

1.- y dentro de "reports" otro directorio CON EL MISMO NOMBRE QUE EL NOMBRE DE LA BASE DE DATOS....

1.- ...y dentro de este "directorio-bd" otros tres:

* "reports"
* "subreports"
* "temp_files"

![eneboo-jasper-directorios-1](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-jasper/eneboo-jasper-esquema-archivos01.jpg)

![eneboo-jasper-directorios-2](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-jasper/eneboo-jasper-esquema-archivos02.jpg)

![eneboo-jasper-directorios-3](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-jasper/eneboo-jasper-esquema-archivos03.jpg)

![eneboo-jasper-directorios-4](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-jasper/eneboo-jasper-esquema-archivos04.jpg)

![eneboo-jasper-directorios-5](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-jasper/eneboo-jasper-esquema-archivos05.jpg)

####PASO 3.- COPIAR EL EJECUTABLE .JAR Y LA CARPETA DE "LIBRERIAS":

Repositorio con libreria a java actualizadas:

https://github.com/eneboo/eneboo-reports

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

## PROBLEMATICAS SOLUCIONADAS:

Parece que no era ni por que soy tan zoquete ni por el postgres 9.3 , el problema esta en que al parecer la libreria no coge el puerto de conexion a la bd correctamente del ejecutable de eneboo y siempre usa el por defecto de  postgres 5432 y yo estaba usando 5433.

SOLUCIÓN: Postgres tiene que estar configurado por el puerto 5432 para que eneboo-reports funcione perfectamente y no el error  de que la bd en cuestión no existe.

---

## SIGUIENTE PASO: CONFIGURAR Y DISEÑAR LOS ARCHIVOS .jrxml CON JASPER STUDIO.

https://github.com/Miguel-J/eneboo/wiki/Dise%C3%B1os-de-Impresi%C3%B3n-e-informes.-Configurar-archivos-Jasper-Reports