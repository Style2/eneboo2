###INICIO:
...puedo acceder al archivo donde aparece....por Eneboo-Sistema-Admin-modulos, y luego "flfactppal" y modificar y de nuevo modificar "FLWidgetMasterTable.ui"...

....donde deberia cambiar el "iconset" o re-definir la "data format" que sale al final de ese archivo:

    <property name="iconSet">
    <iconset>image0</iconset>
y tmb:
    <image name="image0">
    <data format="PNG" length="1555">
https://groups.google.com/forum/#!topic/eneboo/Eb2265EINDM
Un consejo , previamente conviertela a 32x32 para que no se quede colgado eneboo al cargar ese formulario con una imagen gigantesca. 

###COMO "SACAR" LOS ICONOS DE ENEBOO:

En eneboo-tools tienes una utilidad para extraer iconos: 

$ eneboo-uiimage download ~/path/to/facturacion/principal/master.ui 

Y te crea, en la carpeta donde ejecutes, los ficheros de imagenes. 

https://groups.google.com/forum/#!topic/eneboo/lxqbvj7W2fA


###PAGINAS DE DESCARGA DE "ICONSET" EN INTERNET:

http://www.iconarchive.com/

http://www.iconarchive.com/commercialfree.html

### UNA PROPUESTA DE FLAT-ICONS
http://tecneca.com/eneboo-flat-icons/

#####Eneboo Flat Icons 


30 octubre, 2014 por Sergio Bellver Aliaga —Deja un comentario


Con motivo del próximo lanzamiento de nuestra versión oficial de Eneboo ERP + GMAO hemos decidido dar uniformidad en los iconos del ERP y pasarnos a la nueva tendencia de los iconos planos, o flat icons.

Ya en su día planteamos al Grupo de Partners de Eneboo la necesidad de realizar esto y tratamos de hacerlo sobre el pack de iconos koloria; pero este pack tenía alguna carencia en sus iconos, creemos que este nuevo formato es mucho más visual.

Para realizar esta conversión hemos utilizado los recientes recursos de Google en GitHub  y los que nos ofrece la web Flat Icons

Para facilitarnos un poco la tareas, creamos un script que nos abre todos los formularios ui de un directorio pasado como argumento

 

https://gist.github.com/sbellver/129de8b399e7e5d0b5ef#file-qtdesigner-sh

`#!/bin/bash`
`# Es necesario pasarle el directorio como parÃ¡metro.`
`for f in /*.ui`
`do`
  `echo "Abriendo $f ..."`
  `open -a /Applications/eneboo/bin/designer.app --args $f`
  `read -p "Pulse enter para pasar al siguiente UI ... "`
`done`

1

2


 `#!/bin/bash`

`# Es necesario pasarle el directorio como parámetro.`

`for f in /*.ui`

`do`

  `echo "Abriendo $f ..."`

  `open -a /Applications/eneboo/bin/designer.app --args $f`

  `read -p "Pulse enter para pasar al siguiente UI ... "`

`done`


 

view raw qtdesigner.sh hosted with ❤ by GitHub 

Previamente pasamos la utilidad eneboo-uiimage, que simplifica el proceso notablemente.

 




1

2
 # Cambia los iconos de todos los ui en el directorio y subdirectorios pasado como parámetro

eneboo-uiimage theme ~/git/eneboo-tools/themes-uiimage/master_plane.ui $1 overwrite


 

view raw eneboo-iconos.sh hosted with ❤ by GitHub 

Si queréis descargar el master_plane.ui lo tenéis disponible AQUI.

La colección de iconos que usamos, con muchos de ellos con el nombre descriptivo de su funcionalidad, los tenéis AQUI.

Para el ejecutable, ya que en muchos formularios se usa el master_copy.ui , podéis descargaros los ficheros AQUI. Estos hay que situarlos en /Applications/eneboo/share/eneboo/forms/ o donde tengáis eneboo instalado.

Cuando esté la versión 2.4.5 pasada a estable actualizaremos el git para que la podáis compilar cuando queráis.

Por si alguien se anima a realizar su propia versión, encontramos algunos problemas con los que tenían las imágenes puestas como pixmap, no como icon; lo solucionamos cambiando de uno a otro.

Además, en los menús, algunos ítems no se encontraban, por lo que tuvimos que abrirlos en modo texto para añadirlos al menú; de esta forma, con el designer ya se pueden seleccionar y cambiar sus iconos de forma más sencilla.

Los resultados creemos que son muy buenos, dejando eneboo más limpio visualmente y un poco más moderno.


Galería de Imágenes




Compártenos...Share on Google+ 0 Share on LinkedIn 0 Tweet about this on Twitter 0 Share on Facebook 0 



Archivada en: Blog, ERP, GMAO

Etiquetada con: Eneboo, ERP, Flat icons


Acerca de Sergio Bellver Aliaga


CEO y fundador de Tecneca Networks. Apasionado de la tecnología. Obsesionado con la resolución de los problemas.
