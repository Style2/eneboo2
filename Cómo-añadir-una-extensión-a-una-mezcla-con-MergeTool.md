* CREADO POR: [Comunidad Eneboo](http://www.eneboo.org) en https://github.com/eneboo/doc/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 13 de diciembre de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/C%C3%B3mo-a%C3%B1adir-una-extensi%C3%B3n-a-una-mezcla-con-MergeTool)

----
####Podemos aplicar extensiones usando eneboo-mergetool de la siguiente manera:

`# eneboo-mergetool folder-patch ruta_parche ruta_código ruta_mezcla`

donde:

* **eneboo-mergetool** es una de las herramientas de eneboo-tools.

* **folder-patch** es la opción de eneboo-mergetool que nos permite aplicar parches.

* **ruta_parche** es la ruta a la carpeta que encontraremos dentro de la carpeta _'patches'_ de la extensión.

* **ruta_código** es la ruta del código sobre el que queremos aplicar la extensión.

* **ruta_mezcla** es la ruta donde queremos que nos coloque el nuevo código con la extensión ya aplicada.



**Ejemplo** para aplicar la extensión ext0002-norma58:

- Por un lado tenemos la carpeta de extensiones por ejemplo en /home/usuario/eneboo-features
- Por otro lado tenemos el código de nuestros módulos por ejemplo en /home/usuario/eneboo-modules

Por comididad colocaremos una copia de los ficheros necesarios en una misma ruta de trabajo, por ejemplo en /home/usuario/pruebas_mezcla

- Ruta al parche: /home/usuario/pruebas_mezcla/norma58
- Ruta al código: /home/usuario/pruebas_mezcla/codigo-original

Para aplicar la extensión nos colocamos en la ruta de trabajo y lanzamos el siguiente comando:

`# eneboo-mergetool folder-patch ./norma58 ./codigo-original ./codigo-mezcla`

Si todo termina sin errores, en la carpeta "codigo-mezcla" tendremos nuestro nuevo código de módulos con la nueva extensión ya aplicada.