* CREADO POR: Oscar ABC Vigo en https://github.com/eneboo/doc/wiki/Crear-plantillas-Jasper-para-Eneboo-Reports
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 3 de marzo de 2016
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki/Dise%C3%B1os-de-Impresi%C3%B3n-e-informes%3A-Configurar-archivos-Jasper-Reports)

---

### Diseños de Impresión e informes. Crear un jrxml de Jasper Reports a partir de un kut

#### PASO PREVIO: Instalar el editor Jaspersoft Studio


Puedes encontrar plantillas listas para usar en: https://github.com/eneboo/reports4eneboo-reports

Para crear una nueva plantilla o modificar alguna que quieras adaptar a tus necesidades, puedes usar un editor de reportes jasper como [Jaspersoft Studio](http://community.jaspersoft.com/project/jaspersoft-studio) (editor gráfico de código abierto).

---

- En una de las primeras lineas tienes un propiedad "name" donde pones el nombre que quieres aparezca en la lista de eneboo-reports (no toma el nombre del fichero, sino este nombre)

- Mas abajo se configuran los parametros:

* Como minimo necesitas el WHERE, que es un parametro q te pasa eneboo y que se usará para "filtrar" en la consulta de los datos (p.ej. podría ser idfactura=201500001234, para que te haga informe de solo esa factura). Como nos lo pasa eneboo, no tenemos q darle un valor (eneboo lo rellena con el valor correspondiente al generar cada informe)

* Tb se usan para las rutas a los subreports o al directorio de imàgenes. En este caso se suele dar un valor, pero tb podría venir de eneboo (solo hay q editar codigo en la funcion correspondiente, tu esto ya lo sabrás)

* Puedes configurar otros parametros para usar en lo que necesites. Puedes darle un valor o puede ser enviados por eneboo, como hace el proyecto eneboo-reportunico para tener una sola plantilla q es dinamica.

- Luego van unos parametros sin importancia y luego el select... esto es lenguaje SQL y seleccionas los campos que quieres usar de las tablas que quieras y "filtras" los valores con el where de antes. Con calma ya veré cómo puedo explicar esto para quien no entienda sql.


* para cada campo puedes darle un nombre, para no tener q llamarlos con el nombre tabla.campo (son los "AS loquesea," que ves para cada campo)

* luego va el FROM las, tablas, que, sean

* los inner join y sus amigos son para seleccionar datos "cruzados" en otras tablas (por ejemplo las lineas de una factura)

* el where ya te dije, y a veces se usa un group by que sirve para lo q puedes imaginar ;)

- A continuacion declaras cada campo. Son los campos de arriba y tienes q indicar su tipo (numero, integer, fecha, etc)

- Creo q luego ya solo van las variables, que son digamos "campos calculados" que no tienes en ninguna tabla (p.ej. el suma y sigue)

- Y despues va todo el código para la estructura de las bandas y los grupos. Esta parte creo q es mas facil hacerlo graficamente