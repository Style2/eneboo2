* CREADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 6 de junio de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/GITHUB-COMO-INSTALARLO-Y-USARLO)

----
##COMO COPIAR EL GITHUB EN EL ORDENADOR DE CASA
1. Cuando estas en una pagina de github, ABAJO-DERECHA hay un botón que pone "CLONE IN DESKTOP", entonces le das y empieza a DESCARGAR un ejecutable...
1. Aceptas el ejecutable y se instala.
1. Eliges un directorio de trabajo en el ordenador local
1. Una vez instalado vas a PROGRAMAS-GITHUB y le das a "GITHUB"....se abre una pantalla en blanco....
1. Vas ARRIBA-DERECHA a la rueda dentada y le das a "OPEN IN GIT SHELL", entonces se abre una ventana parecida al MSDOS de windows con unas letras en colores entre corchetes...
1. Escribes: "git clone https://github.com/(y aqui el nombre de la carpeta a copiar)"
 * NOTA: Para COPIAR-Y-PEGAR en la consola GIT-SHELL NO VALE el Ctrl+V, hay que hacerlo con el ratón (botón derecho)
1. Ejemplos: 
 * "git clone https://github.com/Miguel-J/eneboo" (este almacén-repositorio (pero sin el wiki) con las imágenes)
 * "git clone https://github.com/Miguel-J/eneboo.wiki" (este wiki)
 * "git clone https://github.com/klo-manolo" (el repositorio + actualizado)

* ...y al darle a ENTER lo pone como subdirectorio en el directorio de descargas elegido...

* NOTA: No poner ":" en los nombres de las páginas o no se descargan bien...

##COMO COORDINAR LA COPIA LOCAL Y LA DEL WEB GITHUB
1. Vas ARRIBA-DERECHA a la rueda dentada y le das a "OPEN IN GIT SHELL", entonces se abre una ventana parecida al MSDOS de windows con unas letras en colores entre corchetes...
1. **Para "TRAER" a la copia local los cambios de la copia-"master" del servidor github ponemos:**
 * NOTA: No se por qué no me deja hacerlo si el contenido en local es distinto, dice no-se-que del ".gitattribute", por lo que lo que hago es borrar el directorio local y hacer un "clone"...
 * OJO: El PULL hay que hacerlo DESDE EL DIRECTORIO DONDE QUIERES QUE DESCARGUE los archivos....si no es donde estás poner "cd (subdirectorio)" hasta situarse en el correcto...sin los parentesis.
 * "git pull https://github.com/Miguel-J/eneboo" (sin el wiki)
 * "git pull https://github.com/Miguel-J/eneboo.wiki" (este wiki)
 * "git pull https://github.com/gestiweb/eneboo-modules" (módulos básicos gestiweb)
 * "git pull https://github.com/gestiweb/eneboo-features" (extensiones básicas gestiweb)
 * "git pull https://github.com/klo-manolo/eneboo-features" (extensiones básicas KLO-más actualizadas???)
1. **Para "SUBIR" la copia local MODIFICADA a la copia-"master" del servidor github ponemos:**
 * OJO: ANTES de hacer un PUSH es mejor hacer un PULL, porque si detecta que las partes del "master" del servidor que NO ACTUALIZAS son distintas a lo que tienes en el "local", no te dejará subir nada...
 * OJO: El PUSH hay que hacerlo DESDE EL DIRECTORIO DONDE QUIERES QUE COPIE los archivos....si no es donde estás poner "cd (subdirectorio)" hasta situarse en el correcto...sin los parentesis.

* **Primero hay que decirle al programa quien somos...:**
    * "git config user.mail "miguelajsmaps@gmail.com" "(o la cuenta email de cada uno)
    * "git config user.name "Miguel-J" "(o el nombre de usuario de cada uno)
* **luego hay que decirle que hemos cambiado cosas de los archivos...:**
    * "git add (nombre del archivo)" (para cada archivo nuevo)
        * ejemplo: _"C:\Users\portatil\Documents\GitHub\eneboo-manual\eneboo.wiki [master +6 0 0 1] git add EnebooTools.md"_ 
        * NOTA: NO olvidarse de la extensión ".md"
    * "git commit -a" (esto solo vale si no hemos creado ningún archivo)
        * ejemplo:_"C:\Users\portatil\Documents\GitHub\eneboo-manual\eneboo.wiki [master +6 0 0 1] git commit -a"_ 
        * NOTA: se abre una ventana de texto para poner una explicación del cambio que "subes"....no se puede dejar en blanco....al acabar cerrarla y decirle que SI a grabar (lo hace en un dir. temporal que luego borra)
*  **y ahora hay que decirle que SUBA esos cambios:**
    * _"git push https://github.com/Miguel-J/eneboo master"_
    * _"git push https://github.com/Miguel-J/eneboo.wiki master"_
    * OJO: hay que añadir esa palabra "master" al final de la dirección para indicarle que el que manda es el del servidor...
    * Habrá que poner el USUARIO y PASSWORD de la cuenta propia en el GITHUB

##COMO CREAR SUBDIRECTORIOS DESDE LA WEB

* Simplemente al crear una página nueva añadir delante del nombre el nombre del subdirectorio: "/imagen/prueba"

##COMO SUBIR IMAGENES DE SUBCARPETA AL GITHUB:

1. Primero haces un "pull" para bajar todos los cambios de internet:
     * `c:\Users\yo\Documents\GitHub\eneboo-manual\eneboo>`
     * "git pull https://github.com/Miguel-J/eneboo" (sin el wiki)
![imágenes de github](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-github-imagen/eneboo-github-imagen-02.jpg)
1. ...luego mueves el subdirectorio en el ordenador local...
![imágenes de github](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-github-imagen/eneboo-github-imagen-03.jpg)
1. ...luego hay que ir justo encima del subdirectorio (con cd subdirectorio)...
     * `c:\Users\yo\Documents\GitHub\eneboo-manual\eneboo\imagen>`
1. ...luego hacer un "git add (nombre subdirectorio) desde su raíz...(en este caso sin extensión)...
1. ...luego haces un "git commit -a" (añadir algo de descripción y cerrar grabando)... 
![imágenes de github](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-github-imagen/eneboo-github-imagen-04.jpg)
![imágenes de github](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-github-imagen/eneboo-github-imagen-05.jpg)
![imágenes de github](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-github-imagen/eneboo-github-imagen-06.jpg)

![imágenes de github](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-github-imagen/eneboo-github-imagen-07.jpg)

1. ...luego hacer un "push":
* _"git push https://github.com/Miguel-J/eneboo master"_
* NOTA: misteriosamente conserva el orden de subdirectorios del local....
![imágenes de github](https://github.com/Miguel-J/eneboo/blob/master/imagen/eneboo-github-imagen/eneboo-github-imagen-08.jpg)
