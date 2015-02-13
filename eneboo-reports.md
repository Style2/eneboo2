* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 13 de febrero de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/eneboo-reports)

----
https://groups.google.com/forum/#!topic/eneboo/RKXQm8QKkTg

Despues de estar peleando con los .kut y acabar el café de la maquina descubrí gracias a esta lista el ar2kut, los .ar mejoran algo pero sigue siendo muy limitado, asi que buscando buscando encuentro eneboo-reports, sin esta lista y la colaboración de todos vosotros seguramente habria desinstalado eneboo rapidamente pero por suerte aqui estamos.

## INSTALACIÓN:

#### PASO UNO: INSTALAR JAVA

1- Java , vale no hay problema, lo instalo.

#### PASO DOS: INSTALAR EXTENSIONES 9002 y 1058

Github con esas extensiones: https://github.com/klo-manolo/eneboo-features

* Lo primero que debes de hacer es mezclar las extensiones  con los modulos que estes usando:
Tienes que exportar el módulo flfactinfo , desde sistema - administración - modulos , seleccionar el registro flfactinfo y entrar en el , luego dale a la flecha de exportar.
* Una vez lo tengas exportado en una carpeta de tu pc, lo comprimes y envias a alguien que te inserte las extensiones 9002 y 1058.
* Una vez hecho esto te lo devuelven modificado y tu recargas con las instrucciones que comentas en la bd. Saludos 
* Bien, un par de correos a Aulla por miedo a hacer el ridiculo aqui y despues de que me explicara las 2 extensiones necesarias para hacer andar al bicho ( eneboo-reports ) me lio la manta a la cabeza a y a configurarlo.

#### PASO TRES: INSTALAR LIBRERIAS

2- Librerias jaspereports.jar , descargadas y dejadas en C/jasper (¿he mencionado que estoy sobre windows?)
* he copiado el .jar a /usr/share/java para instalar la libreria
* una vez mezclado en el apartado de informes dentro de facturación en datos generales tendras una pestaña nueva que se llamara Jasper Plugin, aqui configuraras la carpeta donde tienes  la libreria ( yo lo tengo en c:\jasperplugin) y la carpeta donde almacenas los reports.
* la carpeta "lib" a "eneboo/lib"???

#### PASO CUATRO: CONFIGURAR PESTAÑA JASPER

1- Abrimos eneboo y voy a Area de facturación/Informes/Datos generales pestaña Jasper plugin"

1- **Ruta de informes:** 
Segun la documentación de Aulla me creo una carpeta que a su vez contiene otra con el nombre de la bd para la que se va a usar asi que queda del siguiente modo 
C:\listados\v18\reports
C:\listados\v18\subreports
C:\listados\v18\temp_files

Mi bd se llama v18  y en la ruta dejo C:\listados

1- **Ruta de la librería**
C:/jasperplugin

## OTROS CASOS-RESUMEN

* he clonado los repositorios eneboo-modules y eneboo-features, y descargado las eneboo-tools.
* he hecho eneboo-assembler build jasper_plugin final (y lo mismo con jplugin_plus) y ahi me quedo, por que he visto las carpetas "build" en las extensiones, ¿pero ahora que hago?, supongo que cada extension tendra el standar+extension, pero necesito standar+ext1058+ext9002 y eso no se como hacerlo, bueno, haria un build de una, sobrescribiria en eneboo-modules y haria la otra build. pero luego que tengo que pasar a eneboo, ¿todos los modulos? por que toca facturacion, contabilidad, informes...

Asi es como lo tengo, pues bien le doy a comprobar la versión de java  y me muestra una ventana 1.7.0_45 aparece como versión instalada.

## PROBLEMATICAS SOLUCIONADAS:
Bueno bueno, respondo y finalizo la consulta ya que gracias a Aulla el viernes encontramos la solución.
Parece que no era ni por que soy tan zoquete ni por el postgres 9.3 , el problema esta en que al parecer la libreria no coge el puerto de conexion a la bd correctamente del ejecutable de eneboo y siempre usa el por defecto de  postgres 5432 y yo estaba usando 5433.
SOLUCIÓN: Postgres tiene que estar configurado por el puerto 5432 para que eneboo-reports funcione perfectamente y no el error  de que la bd en cuestión no existe.