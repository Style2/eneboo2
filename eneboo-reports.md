* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 5 de septiembre de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/eneboo-reports)

----

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


#### INSTALAR EXTENSIONES 9002 y 1058

Github con esas extensiones: https://github.com/klo-manolo/eneboo-features

* Lo primero que debes de hacer es mezclar las extensiones  con los modulos que estes usando:
Tienes que exportar el módulo flfactinfo , desde sistema - administración - modulos , seleccionar el registro flfactinfo y entrar en el , luego dale a la flecha de exportar.
* Una vez lo tengas exportado en una carpeta de tu pc, lo comprimes y envias a alguien que te inserte las extensiones 9002 y 1058.
* Una vez hecho esto te lo devuelven modificado y tu recargas con las instrucciones que comentas en la bd. Saludos 
* Bien, un par de correos a Aulla por miedo a hacer el ridiculo aqui y despues de que me explicara las 2 extensiones necesarias para hacer andar al bicho ( eneboo-reports ) me lio la manta a la cabeza a y a configurarlo.


#### OTROS CASOS-RESUMEN

* he clonado los repositorios eneboo-modules y eneboo-features, y descargado las eneboo-tools.
* he hecho eneboo-assembler build jasper_plugin final (y lo mismo con jplugin_plus) y ahi me quedo, por que he visto las carpetas "build" en las extensiones, ¿pero ahora que hago?, supongo que cada extension tendra el standar+extension, pero necesito standar+ext1058+ext9002 y eso no se como hacerlo, bueno, haria un build de una, sobrescribiria en eneboo-modules y haria la otra build. pero luego que tengo que pasar a eneboo, ¿todos los modulos? por que toca facturacion, contabilidad, informes...

#### SIGUIENTE PASO:

Configurar Jasper-Report en el ordenador del servidor. Seguir los pasos de:

https://github.com/Miguel-J/eneboo/wiki/Dise%C3%B1os-de-Impresi%C3%B3n-e-informes.-Instalar-el-enlace-a-Jasper-Reports

***


### Re: [eneboo] Re: Operación adiós kuts.



https://groups.google.com/forum/#!searchin/eneboo/jasper$20aulla/eneboo/hWwVOegjORY/n5xkpjnOK6gJ

Eliminar la dependencia, no los kuts en si, es decir, modificar los módulos para eliminar las llamadas directas a kugar y que todas pasen por flfactinfo.lanzarInforme. De esta manera y con el uso de la ext9002-Jasper_Plugin se podría usar los ficheros jrxml( editandolos con iReports) de manera generalizada y aprovechando la posibilidad de cambiar progresivamente de un sistema a otro y que permite la existencia de los dos sistemas simultaneos (ext1058-jplugin_plus.).

El problema es que es un trabajo bastante arduo , en dos partes, por un lado la modificación de los .qs eliminado las llamadas erroneas y por otro la creación de los informes equivalentes a cada kut. 

Con la modificación de los .qs , tendría que ser un cambio transparente para los kut y que no condiciona el uso de Eneboo Reports aún, simplemente cambia la ruta para llamar a los kuts.(dependencia de flfactinfo).

El segundo paso puede ser más pausado y se puede ir completando por necesidad, cuando algún colaborador crea uno de estos informes , lo puede liberar y poco a poco hacer un mapa de informes completo. 

Un aspecto importante del segundo paso es la creación de una plantilla con unas pautas (llamese estilo) e intentar que sea común para todos los informes. 

---

### REPOSITORIO GITHUB JASPER AULLA

Como paso inicial he creado una nueva rama (jasper) en este repo:

https://github.com/eneboo/eneboo-reports

Quien quiera colaborar cambiando el .qs, puede crear un fork e ir haciendo pull requests a este repo anterior.
Para los que quieran colaborar en la creación de reports, pueden usar este otro repo:

https://github.com/Aulla/reports4eneboo-reports

Si no sabes como va el tema y quieres colaborar pregunta, no te cortes, y recuerda que así salimos ganando todos.
Saludos
