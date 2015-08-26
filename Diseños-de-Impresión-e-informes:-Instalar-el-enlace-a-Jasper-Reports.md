* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 26 de agosto de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Dise%C3%B1os-de-Impresi%C3%B3n-e-informes%3A-Instalar-el-enlace-a-Jasper-Reports)

----
###MANUAL DE Diseños de Impresión e informes: Instalar el enlace a Jasper Reports

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