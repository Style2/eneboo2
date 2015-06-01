* CREADO POR: desconocido y adaptado por: miguelajsmaps@gmail.com
* EDITADO POR: miguelajsmaps@gmail.com en https://github.com/Miguel-J/eneboo/wiki
* ULTIMA ACTUALIZACIÓN: 1 de junio de 2015
* [Para imprimir esta pagina en PDF PULSAR AQUI](https://gitprint.com/Miguel-J/eneboo/wiki//Manual-de-Inteligencia)

----
##MÓDULO DE ANÁLISIS DE DATOS - GUIA BÁSICA DE USUARIO
###1. Introducción
El módulo de Análisis de Datos (Business Intelligence) permite realizar consultas dinámicas sobre datos
acumulados que pueden hacer referencia a distintos aspectos de la empresa (ventas, compra,
rentabilidad, producción, etc.). El módulo dispone de un diseñador de Cuadros de Mando que permiten
tener una visión gráfica de los datos necesarios para tener una visión clara y directa del estado de la
empresa en un determinado aspecto.

En esta guía básica veremos cómo usar el navegador para realizar consultas y gráficos y cómo crear y
explotar cuadros de mando.

El módulo de Análisis de Datos ha sido programado siguiendo la teoría de cubos OLAP. Este sistema se
basa en guardar los datos a analizar de una determinada forma (lo que se llama un Cubo de Datos) en la
que es muy rápido y sencillo establecer consultas y restricciones sobre los mismos. Tiene más
información sobre la teoría de cubos OLAP en http://es.wikipedia.org/wiki/Cubo_OLAP
Parámetros Generales. El módulo puede instalarse en la misma base de datos en la que está instalado
AbanQ o en una nueva base de datos. En cualquiera de estos dos casos el funcionamiento es el mismo.
La diferencia es que si se lleva el análisis a una nueva base de datos, los cubos de datos generados, que
pueden llegar a ocupar mucho espacio, quedan fuera de la base de datos principal. Dado que la
información de estos cubos es redundante y puede ser regenerada cuando se desee, esta opción es
conveniente si no se desea que la base de datos principal crezca demasiado, o si se desea poder llevar a
otro lugar dichos datos de análisis sin necesidad de realizar una copia completa de toda la base de datos
principal. Llamaremos a este tipo de instalación Instalación Distribuida, y la instalación en una única base
de datos Instalación Normal.

###Formulario de configuración
En el formulario de configuración debemos indicar qué es nuestra base de datos respecto al módulo de
Análisis de Datos. Dicha base de datos puede ser:
* Origen: En una instalación distribuida, corresponde a la base de datos que contiene la
información a partir de la cual se construirán los cubos de datos. Los datos de conexión permiten
que aunque los cubos no residan en esta base de datos sea posible acceder a ellos como si
realmente estuvieran ahí.
* Destino: En una instalación distribuida, corresponde a la base de datos que contiene los cubos de
datos. Los datos de conexión permiten al módulo conectarse a la base de datos origen para
recargar los cubos de datos cuando el usuario lo solicita.
* Ambas: Este es el valor a indicar en una instalación normal, donde los cubos y los datos de
origen coexisten en la misma base de datos.

Otros dato a establecer en la configuración del módulo es el rango de años a usar en la recarga de cubos.
Puede ser que aunque nuestra base de datos contenga datos de hace muchos años, queramos que los
cubos únicamente contengan información de los últimos 2 ó 3 años.

###2. Navegador de cubos (Tablas)
Antes de hablar del navegador de cubos, es necesario tener claros varios conceptos de la teoría de cubos
OLAP. Ello nos facilitará la tarea de comprender cómo podemos obtener fácilmente la información que
buscamos:
* Medida: Una medida es un valor que queremos consultar. Ejemplos de medidas son “Total neto
facturado”, “Descuento medio”, etc.
* Dimensión o nivel: Una dimensión es una clasificación en la que podemos organizar o filtrar las
medidas. Ejemplos de dimensión son “Cliente”, “Año”, etc. Un ejemplo de organización es “Total
neto facturado para cada Cliente”. Una ejemplo de restricción es “Descuento medio en el año
2010”.

Un cubo OLAP contendrá siempre información sobre una o más medidas clasificada por varias
dimensiones. El cubo que por defecto trae el módulo de Análisis de Datos es el cubo de ventas, que
muestra el total neto vendido (facturas de cliente) clasificado por fecha, cliente, artículo, familia, agente,
etc.

El navegador de cubos aparece al seleccionar la opción de menú Principal → Navegador.
El primer paso para poder usar el navegador es cargar el cubo de datos por primera vez. Para ello
estableceremos como cubo actual el cubo Ventas y recargaremos el cubo actual con los dos botones de la
parte superior derecha del navegador.

###Formulario de selección de los ejercicios a recargar
AbanQ nos preguntará qué ejercicios queremos cargar. Es muy común, una vez cargados por primera vez
todos los ejercicios a analizar, recargar únicamente el ejercicio actual, dado que es sólo en este último en
el que se registran cambios. Esto permite ahorrar tiempo ya que la carga de datos puede tardar
dependiendo del volumen de los mismos.

Una vez cargado el cubo, vemos que seleccionando una o dos medidas, podemos ver unos valores en la
tabla:

Tabla del navegador mostrando dos medidas
Estos valores, ya que no hemos establecido ninguna restricción, corresponden al total de ventas y de
cantidad de artículos vendidos en todo el cubo, es decir, para todos los datos importados.
Vamos ahora a establecer una clasificación de la medida de Ventas. Para ello quitamos la selección de la
medida Cantidad y pulsamos el botón X. Este Botón permite indicar las dimensiones a incluir en el eje X
(columnas de la tabla).

Formulario de selección de niveles para el eje X
Este formulario de selección nos permite indicar la dimensión o dimensiones que deseamos incluir en
cada uno de los ejes. Seleccionaremos de la tabla de la izquierda el nivel Artículo, haciendo doble clic
sobre él o usando las flechas Izquierda / Derecha. El nivel Artículo pasa a la parte derecha del formulario.
Podemos cambiar el orden de los datos a mostrar haciendo doble clic sobre la columna orden.

Tabla del navegador con 1 nivel en el eje X
Vemos que en la tabla la medida Ventas se reparte ahora entre los tres artículos que se han vendido.
De la misma forma podemos clasificar los resultados en el eje Y, es decir, en las filas de la tabla.

Formulario de selección de niveles para el eje Y
En este caso hemos optado por usar dos niveles, un primer nivel de Año y un segundo nivel de Mes. Esto
hace que los datos aparezcan clasificados por mes y agrupados por su nivel superior (año).

Tabla del navegador con 2 niveles en el eje Y
Los datos acumulados son resaltados con un fondo violeta.
Podemos también establecer restricciones sobre estos datos. Por ejemplo, podemos querer ver
únicamente datos relativos a Febrero y Marzo, y sólo las compras del Cliente 1. Para ello pulsamos en la
tabla de restricciones sobre la dimensión a restringir.

Formularios de selección de restricciones
Las restricciones temporales (años, trimestres, meses) usan un formulario distinto a las demás (clientes,
artículos, etc.). Este segundo formulario permite la selección y no selección de todos los elementos de la
tabla mediante los botones de su cabecera.
Una vez impuestas estas restricciones vemos que por una parte la tabla de datos se ha actualizado en
consecuencia, mientras que la tabla de restricciones refleja igualmente las condiciones impuestas.

Tabla del navegador con restricciones
Finalmente, indicar que mediante los controles del apartado Medidas es posible ordenar los resultados en
función no de las dimensiones sino de los valores de las medidas mostradas, así como limitar su
resultado a un número determinado de registros. Esto permite realizar consultas de tipo Informes ABC
(mis X mejores clientes, mis X artículos más vendidos, etc.).

Los botones de la parte superior izquierda permiten gestionar las distintas posiciones que vamos
obteniendo cuando navegamos por el cubo:
* Anterior: Permite ir a la posición anterior.
* Siguiente: Permite ir a la posición siguiente.
* Abrir posición: Permite abrir una posición previamente guardada.
* Guardar posición y Guardar posición como...: Permiten guardar la posición actual. Esto es
conveniente para posiciones que se van a consultar a menudo o que van a ser usadas en cuadros
de mando, como veremos más adelante.
* Exportar como lista de marketing. Esta opción permite generar una lista de marketing que pasa
de forma automática a dicho módulo. Por ejemplo “Los 10 clientes que más compraron el artículo
Referencia 1 el año pasado”.

###3. Navegador de cubos (Gráficos)
Junto al módulo de Análisis de Datos se entrega el módulo de Gráficos. Este módulo permite la
representación de gráficos de distintos tipos (barras, lineal, tabla, etc).
En la primera pestaña del navegador de cubos vemos los datos mostrados en forma de tabla. Esta es la
forma más genérica de mostrar los datos, pero no la única. Podemos querer ver representados los datos
que consultamos en forma de gráficos de distintos tipos. Para ello usamos la pestaña Gráfico.

Pestaña Gráficos del navegador con gráfico de barras

Por defecto el tipo de gráfico que vemos es la tabla. El gráfico tabla muestra los datos de igual forma que
lo hace la pestaña Tabla del navegador, y se ha creado a efectos de que las tablas puedan ser incluidas
en los cuadros de mando. Podemos modificar la apariencia de la tabla mediante la pulsación en el botón
Editar formato situado a la izquierda del gráfico.

Formulario de edición de formato del gráfico de tabla
Los formularios de edición de formato permiten establecer propiedades de los gráficos, como el estilo y
tamaño de fuente a usar, las medidas de márgenes y otros valores, los colores a usar, etc. Los formulario
varían en función del tipo de gráfico, y siempre permiten ver una muestra del gráfico en su parte inferior.
Vamos ahora a crear un gráfico de barras. Para ello debemos establecer una posición en el cubo de datos
que permita este tipo de representación. Para ello vamos a eliminar del eje X las dimensiones indicadas y
vamos a dejar en el eje Y únicamente la dimensión Mes. Una vez establecida la posición podemos ver el
gráfico de barras pulsando en el correspondiente botón de la cabecera de las pestaña gráfico.
Retocando el formato podemos llegar a un gráfico similar al que muestra la siguiente captura:

Pestaña Gráficos del navegador con gráfico de barras
Dado que el gráfico lineal necesita los mismos tipos de posición que el de barras para ser representado,
podemos cambiar de uno a otro mediante los botones de tipos de gráfico de la parte superior de la
pestaña Gráfico.
Si añadimos un nivel en el eje X podemos obtener gráficos de barras más complejos.

Pestaña Gráficos del navegador con gráfico de barras (varios valores en eje X)

###4. Navegador de cubos (Informes)
Además de visualizar datos por pantalla podemos emitir informes que se generan sobre el mismo visor
que el resto de informes de AbanQ. Al igual que los gráficos, el formato del informe puede ser
personalizado.

Formulario de edición de formato de informe
Tanto los formatos de gráficos como de informe son guardados automáticamente cuando el usuario
guarda la correspondiente posición.

###5. Cuadros de mando
Un cuadro de mandos es un cuaderno digital de una o más páginas en las que se muestra un conjunto de
gráficos correspondientes a posiciones de uno o más cubos de datos. Los datos de todos los gráficos de
un mismo cuadro obedecen a un mismo conjunto de restricciones.

El objetivo de un cuadro de mando es dar una idea global a primer golpe de vista del estado de los datos
(económicos, de producción, etc) de la empresa.

Para gestionar cuadros de mando acudimos a la opción de menú Principal → Cuadros de Mando.

El formulario de cuadros de mando tiene dos modos de operación:
* Diseño: El formulario permite añadir posiciones al cuadro, y establecer las dimensiones y
ubicación de cada posición.
* Visor: El formulario permite ver los gráficos y realizar acotaciones mediante la tabla de
restricciones.

Podemos cambiar de un modo a otro pulsando sobre el botón grande de la esquina superior derecha del
formulario.

Cuadro de mandos en Modo Diseño
Cuando se abre un nuevo cuadro de mandos el modo por defecto es siempre Diseño, mientras que
cuando abrimos uno ya existente, el formulario se abrirá en modo Visor.
Para crear un nuevo cuadro de mandos debemos establecer varios valores:
* Número de páginas. Un cuadro puede tener una o más páginas. El usuario podrá navegar entre
estas páginas en cualquiera de los dos modos.
* Alto y ancho. Definen el tamaño del cuadro, en píxeles.
* Posiciones. Las posiciones son registros que hemos guardado desde el Navegador de cubos, y
que aquí podemos mostrar. Para añadir una nueva posición al cuadro, pulsamos el botón de
insertar y aparecerá el formulario correspondiente:
*

Formulario de posición en cuadro de mandos
Para cada posición indicaremos:
* Su ubicación (coordenadas X e Y)
* Su tamaño (ancho y largo).
* La posición a representar.
* El tipo de gráfico a representar.

Ayudándonos de las desplazadores situados encima y a la izquierda del cuadro podemos ajustar su
posición (desplazadores externos) y su tamaño (desplazadores interiores). Además mediante el botón
Editar gráfico podemos ajustar también su formato.
Nueva posición insertada en el cuadro
Podemos añadir al cuadro tantas posiciones como deseemos.

Cuadro de mandos sencillo de una única página