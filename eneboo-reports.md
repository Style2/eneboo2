https://groups.google.com/forum/#!topic/eneboo/RKXQm8QKkTg

## PASO UNO

Lo primero que debes de hacer es mezclar las extensiones  con los modulos que estes usando:
Tienes que exportar el módulo flfactinfo , desde sistema - administración - modulos , seleccionar el registro flfactinfo y entrar en el , luego dale a la flecha de exportar. Una vez lo tengas exportado en una carpeta de tu pc, lo comprimes y envias a alguien que te inserte las extensiones 9002 y 1058.
 Una vez hecho esto te lo devuelven modificado y tu recargas con las instrucciones que comentas en la bd. Saludos 


, una vez mezclado en el apartado de informes dentro de facturación en datos generales tendras una pestaña nueva que se llamara Jasper Plugin, aqui configuraras la carpeta donde tienes  la libreria ( yo lo tengo en c:\jasperplugin) y la carpeta donde almacenas los reports.

"3- Abrimos eneboo y voy a Area de facturación/Informes/Datos generales pestaña Jasper plugin"
...a mi en esa ubicación no me sale la "pestaña Jasper plugin"...qué módulo has instalado para que te salga?
Hola Miguel tienes que integrar 2 extensiones:  ext9002  y ext1058 desde los repos features de github.
Github con extensiones https://github.com/klo-manolo/eneboo-features

estoy totalmente perdido para instalar eneboo-reports... ¿donde se puede encontrar alguna documentacion de como instalarlo? No la encuentro. Me lo he descargado de github(EnebooReports-6.0.0-20141208_7), y he copiado el .jar a /usr/share/java para instalar la libreria( ?¿?¿), la carpeta "lib" a "eneboo/lib" (?¿?¿?)..


y una vez hecho esto, he intentado instalar las extensiones 9002 y 1058, pero no ha habido manera, he clonado los repositorios eneboo-modules y eneboo-features, y descargado las eneboo-tools. he hecho eneboo-assembler build jasper_plugin final (y lo mismo con jplugin_plus) y ahi me quedo, por que he visto las carpetas "build" en las extensiones, ¿pero ahora que hago?, supongo que cada extension tendra el standar+extension, pero necesito standar+ext1058+ext9002 y eso no se como hacerlo, bueno, haria un build de una, sobrescribiria en eneboo-modules y haria la otra build. pero luego que tengo que pasar a eneboo, ¿todos los modulos? por que toca facturacion, contabilidad, informes...

## RESUMEN
Muy buenas a todos, lo primero presentarme, mi nombre es Rubén Díaz y  estamos implantando eneboo para la gestión de mi empresa, venimos de un programa que funciona con bases de datos D3 y pickOS asi que esto es el futuro :)



Despues de estar peleando con los .kut y acabar el café de la maquina descubrí gracias a esta lista el ar2kut, los .ar mejoran algo pero sigue siendo muy limitado, asi que buscando buscando encuentro eneboo-reports, sin esta lista y la colaboración de todos vosotros seguramente habria desinstalado eneboo rapidamente pero por suerte aqui estamos.




Bien, un par de correos a Aulla por miedo a hacer el ridiculo aqui y despues de que me explicara las 2 extensiones necesarias para hacer andar al bicho ( eneboo-reports ) me lio la manta a la cabeza a y a configurarlo.

1- Java , vale no hay problema, lo instalo.

2- Librerias jaspereports.jar , descargadas y dejadas en C/jasper (¿he mencionado que estoy sobre windows?)

3- Abrimos eneboo y voy a Area de facturación/Informes/Datos generales pestaña Jasper plugin

A configurar !

4- Ruta de informes: Segun la documentación de Aulla me creo una carpeta que a su vez contiene otra con el nombre de la bd para la que se va a usar asi que queda del siguiente modo 
C:\listados\v18\reports

C:\listados\v18\subreports


C:\listados\v18\temp_files


Mi bd se llama v18  y en la ruta dejo C:\listados

5- Ruta de la libreria C:/jasperplugin




Asi es como lo tengo, pues bien le doy a comprobar la versión de java  y me muestra una ventana 1.7.0_45 aparece como versión instalada.

## PASO DOS
Bueno bueno, respondo y finalizo la consulta ya que gracias a Aulla el viernes encontramos la solución.
Parece que no era ni por que soy tan zoquete ni por el postgres 9.3 , el problema esta en que al parecer la libreria no coge el puerto de conexion a la bd correctamente del ejecutable de eneboo y siempre usa el por defecto de  postgres 5432 y yo estaba usando 5433.
SOLUCIÓN: Postgres tiene que estar configurado por el puerto 5432 para que eneboo-reports funcione perfectamente y no el error  de que la bd en cuestión no existe.