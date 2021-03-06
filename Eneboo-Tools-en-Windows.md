* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 7 de junio de 2016
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Eneboo-Tools-en-Windows)

----
### INSTALACIÓN DE ENEBOO-TOOLS EN WINDOWS. EJEMPLO DE USO CON MERGE-TOOL:

####PASO 1 - INSTALAR PYTHON:

Ir a **www.python.org**  y luego a "download"

bajar la "ActivePython-2.7.10.12-win64-x64"

descargarla y ejecutarla: crea el directorio **c:\python27** y un acceso directo en el menú...

####PASO 2 - Descargar las "eneboo-tools" del Github de Gestiweb o de Miguel-J(fork del anterior):

Seguir estos pasos:

https://github.com/Miguel-J/eneboo/wiki/GITHUB-COMO-INSTALARLO-Y-USARLO

Ejemplo:

git clone https://github.com/gestiweb/eneboo-tools

git clone https://github.com/Miguel-J/eneboo-tools

####PASO 3 - Descargar las "extensiones" del Github de KLO o de Miguel-J(fork del anterior):

git clone https://github.com/klo-manolo/eneboo-features

git clone https://github.com/Miguel-J/eneboo-features

####PASO 4 - instalar "Python-lxml" para Windows

        https://pypi.python.org/pypi/lxml/3.5.0

Elegir la versión correcta para tu versión de Windows. Yo instalo la de Windows 64b con Python 2.7:

         lxml-3.5.0.win-amd64-py2.7.exe (md5)   MS Windows installer  2.7  2015-11-14 3MB 

...se instala **automáticamente** en el directorio c:\python27 instalado previamente...


####PASO 5 - colocar cada elemento en el SUB-DIRECTORIO:

Colocar los DOS sub-directorios en uno conjunto (en el ejemplo "emmergetool") Y ÉSTE DENTRO DE LA CARPETA DE ENEBOO-TOOLS (la descargada de Gestiweb)....NOTA: tal vez si se pone el "path" en "variables de entorno" se pueda evitar que estén juntos....

* **NOTA-1**: El directorio del parche a añadir DEBE TENER **EL MISMO NOMBRE** QUE EL ARCHIVO **.XML** principal que marca los cambios a añadir

* **NOTA-2**: no permite nombres de directorios con espacios en blanco
* **NOTA-3**: no permite nombres de directorios largos
* **NOTA-4**: no permite que exista (**antes de ejecutar mergetool**) el directorio donde vuelca la suma (en este ejemplo: "salida")
* **NOTA-5**: el módulo a añadir **debe llamarse por el "alias"**, no el original (en este caso: "informes", no "flfactinfo")
* **NOTA-6**: los módulos "iniciales" **deben estar dentro de un subdirectorio de su área** (en este caso: "facturación")
* **NOTA-7**: los módulos "iniciales" **salen de "TU MEZCLA PERSONALIZADA"....que se consiguen siguiendo este tutorial**: https://github.com/Miguel-J/eneboo/wiki/C%C3%B3mo-sacar-LA-MEZCLA-de-mi-base-de-datos

![mergetools-windows](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-tools/mergetool-windows02.jpg)

####PASO 6 - ejecutar programas

Abrir la consola de  MS-DOS (con el botón derecho mouse-"ejecutar como administrador") y escribir "python" delante del nombre del programa:

https://github.com/Miguel-J/eneboo/wiki/C%C3%B3mo-a%C3%B1adir-una-extensi%C3%B3n-a-una-mezcla-con-MergeTool

ejemplo: c:\github\eneboo-tools\python eneboo-mergetool folder-patch ./emmergetool/info_ventascli ./emmergetool/iniciales ./emmergetool/salida

![mergetools-windows](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-tools/mergetool-windows03.jpg)

* **NOTA**: en mi directorio de "eneboo-tools", "veo" que TODOS los archivos han sido DUPLICADOS a extensión "Compiled Python File"....

####PASO 7 - RESULTADO:

Crea el sub-directorio "salida" con el nuevo módulo.

![mergetools-windows](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-tools/mergetool-windows04.jpg)

####PASO 8 - AÑADIR ARCHIVO "COPYING" AL NUEVO MÓDULO:

Sirve cualquier archivo con licencia (se puede copiar de las carpetas de los módulos oficiales...)

NOTA: Este paso no es necesario si el módulo inicial ya tenía este archivo...

--

####NOTAS - ERRORES CONOCIDOS:

#####A) ERROR-1 POR FALTAR LA LIBRERIA 

* probando si hace algo al ejecutar programas (se puede saltar este paso...)

Abrir la consola de  MS-DOS (botón derecho mouse-ejecutar como administrador) y escribir "python" delante del nombre del programa

ejemplo: c:\github\eneboo-tools\python eneboo-mergetool

* **ERROR**: 

     "ImportError: No module named lxml"

....YA VISTO EN: "https://github.com/Miguel-J/eneboo/wiki/EnebooTools---Instalaci%C3%B3n-en-linux"

...`es porque la librería de Python "libxml2" en sus versiones recientes no instalan "cosas antiguas" como "lxml", por lo que hay que instalar también:`

...por lo que hay que instalar:

         `$ sudo apt-get install python-lxml` 

* **SOLUCIÓN**: Seguir el **PASO-4** y descargar la librería lxml

#####B) ERROR-2 de codificación

https://groups.google.com/forum/#!topic/eneboo/xE_LOYDPHwA

`UNEXPECTED ERROR UnicodeDecodeError: 'ascii' codec can't decode byte 0xf1 in position 57: ordinal not in range(128)`
`Traceback (most recent call last):`

  `File "C:\GITHUB\eneboo-tools\enebootools\mergetool\__init__.py", line 273, in do_folder_patch`

    `return flpatchdir.patch_folder(self, basedir, finaldir, patchdir)`

  `File "C:\GITHUB\eneboo-tools\enebootools\mergetool\flpatchdir.py", line 537, in patch_folder`

    `iface.debug(u"Folder Patch $basedir:%s $finaldir:%s $patchdir:%s" % (basedir,finaldir,patchdir))`

`UnicodeDecodeError: 'ascii' codec can't decode byte 0xf1 in position 57: ordinal not in range(128)`

* **SOLUCIÓN**: Seguir el **PASO-5** y revisar (simplificando) los nombres de los directorios donde están los módulos iniciales y los del parche-extensión

#####C) ERROR-3 de ubicación-falta de path

     `WARN: ** Se ha ignorado acción desconocida 'action' **`
     `WARN: ** Se ha ignorado acción desconocida 'action' **`
     `WARN: ** Se ha ignorado acción desconocida 'action' **`

* **SOLUCIÓN**: Seguir el **PASO-5** y colocar los directorios (y subdirectorios) en la carpeta de "eneboo-tools"

---

### INTENTOS ANTERIORES - ANTIGUOS (descartarlos)

https://groups.google.com/forum/#!topic/eneboo/eVkmQNMUzGQ

1. **mfdezp    27/8/12**
Me acabo de Instalar el Python en Windows, pero siguiendo la guia de las Eneboo-tools, me dice que lo primero que hay que hacer es tener una serie de librerías (que no sé como tenerlas operativas para python en windows) y luego hacer un 
_sudo make install_ (que entiendo que es la instalación en linux). 

2. **Aulla Sistemas**
Mi recomendación es que te instales un linux tipo ubuntu 10.10 en una máquina virtual.

3. **David Martínez Martí**
En windows las librerías de python se descargan como ejecutables (instaladores). Para cada versión menor de Python  (2.5.x, 2.6.x) hay un instalador distinto. 

Entonces, en resumen, lo que hay que hacer es: 

- Identificar tu versión de Python, supongamos que es 2.7.3 
- Identificar el paquete, por ejemplo "python-lxml" 
- Buscar la página del proyecto con google (por ejemplo, busca <python lxml>) 
- Localizar las descargas del proyecto para Windows, y bajar la 
adecuada para tu versión de Python 
- Ejecutar el instalador y seguir los pasos (siguiente, siguiente, etc) 

Y se repite el proceso para el resto de librerías. 

De todos modos, la consola de Windows se quedará un poco "corta" para 
manejar estos programas.... y yo recomendaría la solución de Aulla, 
una máquina virtual. 

---

####COMO INSTALAR VIRTUALBOX CON UBUNTU 14.04
Pongo los pasos aquí, pero mi experiencia personal con un:
* Windows 8.1 de x64
* AMD A4-1250 1Gb con 4 Gb RAM y 450 Gb disco duro
* es que decir LENTO es ser muy optimista.....aunque funciona, puedes ir a dar la vuelta a la manzana hasta que acaba de ejecutar cualquier programa...eso si no se "cuelga"....

1. **INSTALAR VIRTUALBOX**

https://www.virtualbox.org/wiki/Downloads

Aunque hay muchos tuturiales, a mi me gustó este:
https://netfaozz.wordpress.com/2012/03/05/tutorial-de-virtual-box-instalar-linux-en-windows/

1. **DESCARGAR LA ISO DE UBUNTU**

http://www.ubuntu-es.org/

Que resulta que virtualbox viene en estructura x32, por lo que no vale la ISO de x64 (aunque tu ordenador la prefiera....mal rollo):

1. **INSTALAR UBUNTU A TRAVÉS DE VIRTUALBOX**

No hay problema en aceptar todas las opciones COMO si fuese un disco virgen, VIRTUALBOX limita los formateos, etc a la cuota de disco establecida...

http://blog.uptodown.com/tutorial-virtualizar-ubuntu-14-virtualbox/

...falta ajustar el tamaño de pantalla con "Insertar imagen de CD de las Guest Additions"...

... y quitar un mensaje inofensivo de error de un SMSBus:
http://hablemosdetic.blogspot.com.es/2011/02/solucionar-el-problema-de-piix4smbus-en.html

**Pero repito que el resultado fue una tortuga**

