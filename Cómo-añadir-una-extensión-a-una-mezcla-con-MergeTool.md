* CREADO POR: [Comunidad Eneboo](http://www.eneboo.org) en https://github.com/eneboo/doc/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 23 de diciembre de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/C%C3%B3mo-a%C3%B1adir-una-extensi%C3%B3n-a-una-mezcla-con-MergeTool)

----
**NOTA SOBRE LINUX**:
* Cómo llego a la **consola"?
     * Entrar a la consola desde la vista-escritorio: Ctrl+Alt+F1
     * Salir de la consola hacia la vista-escritorio: Ctrl+Alt+F7

* Qué teclas sirven para **copiar-y-pegar** el texto en la consola en Linux o Unix ?:
     * Ctrl+Shift+c = copiar
     * Ctrl+Shift+V.= pegar

* Cómo extraer de forma segura un USB?
     * vas a la consola con Ctrl+Alt+F1 y escribes **umount /media/linux(o nombre ordenador)/(nombre de volumen del usb)**

----
####Podemos aplicar extensiones usando eneboo-mergetool de la siguiente manera:

`# eneboo-mergetool folder-patch ruta_parche ruta_código ruta_mezcla`

donde:

* **eneboo-mergetool** es una de las herramientas de eneboo-tools.

* **folder-patch** es la opción de eneboo-mergetool que nos permite aplicar parches.

* **ruta_parche** es la ruta a la carpeta que encontraremos dentro de la carpeta _'patches'_ de la extensión.

* **ruta_código** es la ruta del código sobre el que queremos aplicar la extensión.

* **ruta_mezcla** es la ruta donde queremos que nos coloque el nuevo código con la extensión ya aplicada.



####**Ejemplo** para aplicar la extensión ext0002-norma58:

##### PASO 1 - PREPARACIÓN DE DATOS PREVIOS:

- Por un lado tenemos la carpeta de extensiones por ejemplo en:
         /home/usuario/eneboo-features
- Por otro lado tenemos el código de los módulos de nuestra mezcla privada, por ejemplo en:
         /home/usuario/inicial

##### PASO 2 - COLOCACIÓN DE DATOS PREVIOS:

Por comodidad colocaremos los ficheros necesarios en una misma ruta de trabajo, por ejemplo en:
         /home/usuario/pruebas_mezcla

...quedando así:

- Ruta al parche: /home/usuario/pruebas_mezcla/norma58
- Ruta al código: /home/usuario/pruebas_mezcla/inicial

##### PASO 3 - EJECUCIÓN ORDEN "mergetool":

Para aplicar la extensión nos colocamos en el directorio **pruebas_mezcla**:

`cd pruebas_mezcla`

...y lanzamos el siguiente comando:

`~/pruebas_mezcla$ eneboo-mergetool folder-patch ./norma58 ./inicial ./salida`

Si todo termina sin errores, en la carpeta "salida" tendremos nuestro nuevo código de módulos con la nueva extensión ya aplicada.